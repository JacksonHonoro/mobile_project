# Mobile_Project
Estrutura inicial de um projeto Mobile React Native (configurado Reactotron, React-navigation, eslint, prettier).

*Observações:
> No arquivo package.json acrescentar o nome do seu projeto.

> Acrescentar algumas linhas referente ao react-navigation (conforme sua documentação exige) no arquivo MainActivity.java:

https://kmagiera.github.io/react-native-gesture-handler/docs/getting-started.html


package com.SeuProjeto;

import com.facebook.react.ReactActivity;
+ import com.facebook.react.ReactActivityDelegate;
+ import com.facebook.react.ReactRootView;
+ import com.swmansion.gesturehandler.react.RNGestureHandlerEnabledRootView;

public class MainActivity extends ReactActivity {

  /**
   * Returns the name of the main component registered from JavaScript. This is used to schedule
   * rendering of the component.
   */
  @Override
  protected String getMainComponentName() {
    return "mobile_project";
  }
  + @Override
  + protected ReactActivityDelegate createReactActivityDelegate() {
    + return new ReactActivityDelegate(this, getMainComponentName()) {
      + @Override
      + protected ReactRootView createRootView() {
      + return new RNGestureHandlerEnabledRootView(MainActivity.this);
      + }
    + };
  + }
}

> Salve o arquivo.

> Após terminar, executar o comando yarn.

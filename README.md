## use-store

useStore is a simple flux library
- using react hooks
- only depends react
- no redux but you can do like redux

<!--
`$ npm i -S @miyamonz/use-store`
-->

## How to use

prepare your store
```store.js
import createUseStore from '@miyamonz/use-store'

const state = {
  your: 'initial state'
}
const useStore = createUseStore(state);

export useStore
```

wrap your application with Provider
```index.js
import React from "react";
import { render } from "react-dom";
import { Provider } from "@miyamonz/use-store";
import App from "./App";

render(
  <Provider>
    <App />
  </Provider>,
  document.querySelector("#main")
);
```

and useStore in your component
```YourComponent.js
import useStore from './store'

export default function YourComponent() {
  const [state, dispatch] = useStore()

  dispatch( prevState => newState )
}
```

создаём рабочую директорию
git init (при сздании шаблона впервые этот шаг пропустить)
git --version
node --version
npm --version


создаём .editorconfig в корне
на сайте https://editorconfig.org/ пиздим настройки
по итогу в файле это
```.editorconfig
root = true
[*]
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
charset = utf-8
indent_style = tab
indent_size = 4
```

иниициируем реакт приложение
npx create-react-app my-app
переходим в дирректорию приложения
cd my-app
далее ставим
npm i eslint-config-prettier eslint-plugin-prettier prettier

далее в файле package.json добавляем "prettier" и "plugins"
```json
"eslintConfig": {
	"extends": [
		"react-app",
		"react-app/jest",
		"prettier"
	],
	"plugins": [
		"prettier"
	]
},
```
чтобы настроить prettier, нужно в корне приложения создать файл его конфигурации 

prettierrc.json
prettierrc.json
https://prettier.io/docs/en/options
```json
{
"printWidth": 90,
"tabWidth": 4,
"useTabs": true,
"semi": true,
"singleQuote": true,
"trailingComma": "all"
}
```

alt+shift+f проверить форматирование
в глобальных настройках, в файле settings.json указать:
"editor.rulers": [90]


причёсываем App.js
```js
import logo from "./logo.svg";
import styles from "./app.module.css";

export const App = () => {
	return (
		<div className="App">
			<header className={styles["App-header"]}>
			<img src={logo} className={styles["App-logo"]} alt="logo" />
			<p>
				Edit <code>src/App.js</code> and save to reload.
			</p>
			<a
				className="App-link"
				href="https://reactjs.org"
				target="_blank"
				rel="noopener noreferrer">				
				Learn React
			</a>
			</header>
		</div>
	);
};
```

редактируем имя файла App.css, заменив на app.module.css

затем index.js
```js
import React from "react";
import ReactDOM from "react-dom/client";
import "./index.css";
import { App } from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));

root.render(
	<React.StrictMode>
	<App />
	</React.StrictMode>,
);
```

удаляем файлы 
- App.test.js
- reportWebVitals.js
- setupTests.js


настраиваем
Работа с CSS & Динамический рендеринг CSS-классов
https://create-react-app.dev/docs/adding-a-css-modules-stylesheet/

[[JavaScript]]

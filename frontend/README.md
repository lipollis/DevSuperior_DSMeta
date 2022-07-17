
<div align="right"><img src="https://github.com/lipollis/Imagens-Git/blob/main/sun.png" /></div>

<h1 align="center"> DS Meta - Semana Spring React  </h1>
<h2 align="center"> Dev Superior  </h2>

<h4 align="center"> 
	🚀  React Select  🚀  
</h4>
<br>
<div align="center">
    <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original-wordmark.svg"></img>
    <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original-wordmark.svg"></img>
    <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original-wordmark.svg"></img>
    <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" />
          
</div>
<br>


## Objetivos do projeto para esta aula
- Criar projetos backend e frontend
- Salvar os projeto no Github em monorepo
- Montar o visual estático do front end

## Design Figma
https://www.figma.com/file/PehiT8Dw4Lv5ioTSULZeRI/DSMeta3

https://www.figma.com/file/Yu2RHFmirHQ4BIVZM2XxY6/DSMeta2

https://www.figma.com/file/EN1zFtk4eY3Jgmpgi9YaMG/DSMeta1

## Ferramentas
- Nodejs 16 e Yarn (vídeo: https://youtu.be/x5tgFTS-CYA )
- STS (vídeo: https://youtu.be/TGQ0K9QsX88 )
- VS Code
  - `IntelliCode`
  - `ESLint`
  - `JSX HTML <tags/>`

## Passo: criar projeto ReactJS

![DevSuperior no Instagram](https://raw.githubusercontent.com/devsuperior/bds-assets/main/sds/pastas-dsmeta.png)

Criação do projeto:
```npm
yarn create vite frontend --template react-ts
```
Instalação de dependências com o yarn:
```npm
npm install --location=global yarn
```

Abrir a aplicação localhost:
```
yarn dev
```

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-resources-plugin</artifactId>
				<version>3.1.0</version><!--$NO-MVN-MAN-VER$ -->
			</plugin>

## Passo: salvar primeira versão no Github

```bash
git init

git add .

git commit -m "Project created"

git branch -M main

git remote add origin git@github.com:seuusuario/seurepositorio.git

git push -u origin main
```

## Passo: "limpar" o projeto ReactJS

Vamos pegar o CSS que fizemos nas aulas de preparação:

https://github.com/acenelio/dsmeta-css


- **COMMIT: Project clean**


## Passo: Primeiro componente
- Exporte a imagem para a pasta frontend/src/assets/img/notification-icon.svg
- Criar em components o NotificationButton com index e styles

```tsx
import icon from '../../assets/img/notification-icon.svg';
import './styles.css';


function NotificationButton() {
  return (
    <>
      <div className="dsmeta-red-btn">
        <img src={icon} alt="Notificar" />
      </div>
    </>
  );
}

export default NotificationButton;
```
```css
.dsmeta-red-btn {
    height: 45px;
    width: 45px;
    background: rgba(255, 107, 114, 0.1);
    border: 1px solid #ff6b72;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }
  
  .dsmeta-red-btn img {
      width: 19px;
  }
```
- **COMMIT: First component**



## Passo: Outros componentes
- Components / Header
```tsx
import logo from '../../assets/img/logo.svg';
import './styles.css';


function Header() {
  return (
<header>
        <div className="dsmeta-logo-container">
            <img src={logo} alt="DSMeta" />
            <h1>DSMeta</h1>
            <p>
              Desenvolvido por
              <a href="https://www.instagram.com/devsuperior.ig">@devsuperior.ig</a>
            </p>
        </div>
    </header>
  );
}

export default Header;
```
```css
header {
    background: linear-gradient(180deg, #102347 0%, #181818 100%);
    height: 220px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .dsmeta-logo-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .dsmeta-logo-container img {
    width: 235px;
  }
  
  .dsmeta-logo-container h1 {
    margin-top: 15px;
    font-size: 24px;
  }
  
  .dsmeta-logo-container p {
    font-size: 14px;
    font-weight: 300;
  }
```
- SalesCard
```tsx
import NotificationButton from "../NotificationButton";
import "./styles.css";

function SalesCard() {
  return (
    <div className="dsmeta-card">
      <h2 className="dsmeta-sales-title">Vendas</h2>
      <div>
        <div className="dsmeta-form-control-container">
          <input className="dsmeta-form-control" type="text" />
        </div>
        <div className="dsmeta-form-control-container">
          <input className="dsmeta-form-control" type="text" />
        </div>
      </div>

      <div>
        <table className="dsmeta-sales-table">
          <thead>
            <tr>
              <th className="show992">ID</th>
              <th className="show576">Data</th>
              <th>Vendedor</th>
              <th className="show992">Visitas</th>
              <th className="show992">Vendas</th>
              <th>Total</th>
              <th>Notificar</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td className="show992">#341</td>
              <td className="show576">08/07/2022</td>
              <td>Anakin</td>
              <td className="show992">15</td>
              <td className="show992">11</td>
              <td>R$ 55300.00</td>
              <td>
                <div className="dsmeta-red-btn-container">
                  <NotificationButton />
                </div>
              </td>
            </tr>
            <tr>
              <td className="show992">#341</td>
              <td className="show576">08/07/2022</td>
              <td>Anakin</td>
              <td className="show992">15</td>
              <td className="show992">11</td>
              <td>R$ 55300.00</td>
              <td>
                <div className="dsmeta-red-btn-container">
                  <NotificationButton />
                </div>
              </td>
            </tr>
            <tr>
              <td className="show992">#341</td>
              <td className="show576">08/07/2022</td>
              <td>Anakin</td>
              <td className="show992">15</td>
              <td className="show992">11</td>
              <td>R$ 55300.00</td>
              <td>
                <div className="dsmeta-red-btn-container">
                  <NotificationButton />
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  );
}

export default SalesCard;

```
```css
.dsmeta-card {
    background-color: #283142;
    border-radius: 10px;
    padding: 30px 10px;
  }

  .dsmeta-sales-title {
    color: #676fff;
    font-size: 24px;
    margin-bottom: 20px;
  }
  
  .dsmeta-form-control-container {
    margin-bottom: 16px;
    max-width: 300px;
  }
  
  .dsmeta-form-control {
    width: 100%;
    height: 46px;
    background-color: #1b2531;
    border: 1px solid #384459;
    border-radius: 5px;
    color: #9aaabe;
    padding: 0 20px;
    font-size: 18px;
  }
  
  .dsmeta-sales-table {
    width: 100%;
    border-spacing: 0;
    border-collapse: collapse;
  }
  
  .dsmeta-sales-table thead {
    height: 55px;
    font-size: 16px;
    color: #e9e9e9;
    font-weight: 700;
  }
  
  .dsmeta-sales-table tbody {
    font-size: 14px;
    font-weight: 400;
    color: #cfcfcf;
    text-align: center;
  }
  
  .dsmeta-sales-table tbody tr {
    height: 74px;
    border-top: 1px solid #5f6e82;
  }
  
  .dsmeta-sales-table tbody tr:hover > td {
    background-color: #384459;
  }
  
  .dsmeta-sales-table tbody tr:nth-child(odd) {
    background-color: #242c3b;
  }
  
  .dsmeta-red-btn-container {
      display: flex;
      justify-content: center;
  }
  
  .show576 {
      display: none;
  }
  
  .show992 {
      display: none;
  }
  
  @media (min-width: 576px) {
      .show576 {
          display: table-cell;
      }
  
      .dsmeta-card {
          padding: 35px;
      }
  
      .dsmeta-sales-table tbody tr {
          height: 55px;
      }
  
      .dsmeta-sales-table tbody {
          font-size: 18px;
      }
  }
  
  @media (min-width: 992px) {
      .show992 {
          display: table-cell;
      }
  }
```

- **COMMIT: Other components**

## Passo: Datepicker

Documentação: https://github.com/Hacker0x01/react-datepicker

```
yarn add react-datepicker@4.8.0 @types/react-datepicker@4.4.2
```

```javascript
import DatePicker from "react-datepicker";
import "react-datepicker/dist/react-datepicker.css";
```

```javascript
<DatePicker
    selected={new Date()}
    onChange={(date: Date) => {}}
    className="dsmeta-form-control"
    dateFormat="dd/MM/yyyy"
/>
```

- **COMMIT: Datepicker**

## Passo: React Hook useState para manter estado das datas

Macete para criar uma data de X dias atrás:

```javascript
const date = new Date(new Date().setDate(new Date().getDate() - 365));
```

Declaração dos estados (SalesCard):
```javascript
  const min = new Date(new Date().setDate(new Date().getDate() - 365));
  const max = new Date();
  const [minDate, setMinDate] = useState(min);
  const [maxDate, setMaxDate] = useState(max);
```

- **COMMIT: useState**

## Atualizando o App.tsx
```tsx
import NotificationButton from "./components/NotificationButton";
import Header from "./components/Header";
import SalesCard from "./components/SalesCard";

function App() {
  return (
    <>
      <Header />
      
      <main>
      <section id="sales">
        <div className="dsmeta-container">
          <SalesCard />
        </div>
      </section>
      </main>
    </>
  );
}

export default App;
```
```css
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap");

* {
  font-family: "Roboto", sans-serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body,
html {
  background-color: #000;
  color: #fff;
}

a,
a:hover,
a:visited {
  color: unset;
  text-decoration: none;
}

.dsmeta-container {
  width: 100%;
  max-width: 900px;
  margin: 0 auto;
}

#sales {
  padding: 40px 10px;
}
```
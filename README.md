

# Entrega Urbana — Programação Funcional 

> Projeto desenvolvido para a disciplina de **Linguagens de Programação e Paradigmas**.
> Tema: **Cálculo de Custos de Entrega com Programação Funcional (Node.js + React.js)**

---

## 🧠 Descrição do Projeto

O sistema **simula o cálculo de custos de entregas urbanas** com base em múltiplos fatores como peso, volume, zona, pedágios e janelas de entrega.
Ele aplica **conceitos de programação funcional**, como **funções puras**, **funções de ordem superior** e **imutabilidade** dos dados.

A aplicação permite que o usuário insira os dados de uma entrega e receba automaticamente o **valor total**, detalhado pelos componentes de custo:

* Custo base por zona (A, B ou C);
* Sobretaxa por peso e volume;
* Valor de pedágios;
* Custo adicional para janelas críticas de entrega.

O sistema também realiza **validação automática** dos dados inseridos — garantindo que os valores sejam numéricos, positivos e dentro das regras de negócio.

---

## 📁 Estrutura do Projeto

O projeto está dividido em duas partes principais:

```
entrega-urbana/
├── backend/                → Servidor Node.js + Express (regras e cálculos)
│   └── server.js           → Contém as funções puras, validações e rota /calcular
│
└── frontend/               → Interface web desenvolvida em React
    ├── src/
    │   ├── App.js          → Formulário, integração com o backend e exibição dos resultados
    │   ├── App.css         → Estilos específicos da interface do simulador
    │   ├── index.css       → Estilos globais da aplicação
    │   └── index.js        → Ponto de entrada do React
```

---

## ⚙️ Tecnologias Utilizadas

| Categoria      | Ferramenta                                  |
| -------------- | ------------------------------------------- |
| 🖥️ Backend    | Node.js + Express                           |
| 🔗 Comunicação | Axios (requisições HTTP entre front e back) |
| 💻 Frontend    | React.js (via Create React App)             |
| 🎨 Estilo      | CSS puro (App.css e index.css)              |
| 💡 Paradigma   | Programação Funcional                       |

---

## 🚀 Como Executar o Projeto

### 1️⃣ Clonar o Repositório

```bash
git clone https://github.com/PedroMuci/entrega-urbana
cd entrega-urbana
```

---

### 2️⃣ Configurar e Executar o **Backend**

```bash
cd backend
npm install
node server.js
```

O servidor será iniciado em:

```
http://localhost:3001
```

Você verá a mensagem:

```
Servidor rodando na porta 3001
```

---

### 3️⃣ Configurar e Executar o **Frontend**

Em outro terminal:

```bash
cd ../frontend
npm install
npm start
```

Após a inicialização, o sistema abrirá automaticamente em:

```
http://localhost:3000
```

---

### 4️⃣ Utilizar o Simulador de Entrega

Na tela principal, insira as informações da entrega:

| Campo             | Descrição                           |
| ----------------- | ----------------------------------- |
| Peso (kg)         | Peso total da entrega               |
| Volume (m³)       | Volume ocupado                      |
| Zona              | Região de destino (A, B ou C)       |
| Pedágio (R$)      | Valor total de pedágios no percurso |
| Janela de Entrega | Normal ou crítica                   |

Ao clicar em **Calcular**, o sistema exibirá:

* Custo base por zona
* Custo proporcional ao peso
* Custo proporcional ao volume
* Valor total de pedágios
* Sobretaxa por janela crítica
* 💰 **Total final da entrega**



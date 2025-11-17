# 📱 Ciclista Eletrônico
### Sistema de aluguel de bicicletas com QR Code integrado ao Firebase

O **Ciclista Eletrônico** é um aplicativo mobile desenvolvido em **React Native (Expo)** que simula um sistema de bike sharing.  
O usuário pode digitalizar o QR Code da bicicleta, iniciar um passeio, finalizar o uso e registrar todas as transações no **Firebase Firestore**.

---

## ✨ Funcionalidades

- 📷 Leitura de QR Code usando a câmera do dispositivo  
- 🚴 Aluguel de bicicleta (verifica disponibilidade e manutenção)  
- 🔁 Finalização do passeio com registro automático  
- 👤 Validação do usuário (impede múltiplas bikes alugadas)  
- 📊 Registro completo das transações no Firestore  
- 🧭 Navegação inferior com Bottom Tabs  

---

## 🛠 Tecnologias Utilizadas

- **React Native (Expo)**
- **Firebase Firestore**
- **React Navigation**
- **Expo BarCodeScanner**
- **Ionicons**

---

## 📂 Estrutura do Projeto

/
│── screens/
│ ├── Ride.js # Tela de aluguel e scanner
│ ├── RideHistory.js # Tela de histórico
│
│── navigation/
│ └── BottomTabNavigator.js # Navegação inferior
│
│── config/
│ └── config.js # Configuração do Firebase
│
│── assets/
│ ├── background2.png
│ ├── appIcon.png
│
└── App.js
---

## 🔥 Configuração do Firebase

Crie o arquivo `config/config.js`:

```js
import firebase from "firebase";
import "firebase/firestore";

const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "SEU_AUTH_DOMAIN",
  projectId: "SEU_PROJECT_ID",
  storageBucket: "SEU_BUCKET",
  messagingSenderId: "SEU_SENDER_ID",
  appId: "SEU_APP_ID"
};

if (!firebase.apps.length) {
  firebase.initializeApp(firebaseConfig);
}

export default firebase.firestore();
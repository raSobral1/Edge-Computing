<h1 align="center">🍷 Vinheria Agnelo Inteligente com Arduino</h1>
<h2 align="center">🌡️ Monitoramento de Temperatura e Umidade</h2>

<p align="center">
  <img src="https://img.shields.io/badge/Arduino-Project-blue?style=for-the-badge&logo=arduino">
  <img src="https://img.shields.io/badge/FIAP-Checkpoint%202-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Concluído-brightgreen?style=for-the-badge">
</p>

---

📌 Sobre o Projeto


## 🖼️ Montagem do Circuito
---

<p align="center">
  <img src="assets/circuito.png" alt="Circuito Arduino com DHT11 e LCD" width="700">
</p>

<p align="center">
  🔌 Representação do circuito montado no Tinkercad com Arduino Uno, sensor DHT11 e display LCD
</p>

---

### 🔍 Entendendo a ligação (explicação simples)

- 🔌 **Arduino Uno** → funciona como o cérebro do sistema, controlando todos os componentes  
- 🌡️ **Sensor DHT11** → mede a temperatura e a umidade do ambiente em tempo real  
- 📟 **Display LCD** → mostra as informações para o usuário (temperatura, umidade e status)  
- 💡 **LEDs (indicadores visuais)** → ajudam a identificar rapidamente a situação do ambiente:
  - 🔴 **LED vermelho** → indica alerta de temperatura alta  
  - 🟢 **LED verde** → indica condição ideal do ambiente (tudo OK)  
  - 🟡 **LED amarelo** → indica atenção (umidade fora do ideal ou situação intermediária)  
- 🧩 **Protoboard** → usada para organizar as conexões sem precisar soldar  
- 🔗 **Jumpers (fios)** → fazem a comunicação entre todos os componentes  

👉 O Arduino recebe os dados do sensor DHT11, analisa as condições do ambiente e responde de duas formas:

1. Exibindo as informações no display LCD  
2. Acendendo LEDs para indicar rapidamente o estado do sistema  

👉 Assim, mesmo sem olhar o display, é possível entender a situação apenas pelas cores dos LEDs.

---

### 💡 O que está acontecendo na prática?

1. O sensor lê o ambiente (temperatura e umidade)  
2. O Arduino processa essas informações  
3. O sistema decide se está tudo OK ou se há problema  
4. O resultado aparece no display LCD em tempo real  

---

Nosso projeto simula uma adega inteligente, ou seja, um sistema automatizado que monitora o ambiente onde os vinhos estão armazenados.

👉 Mas por que isso é importante?

Vinhos precisam ficar em condições específicas para não perder qualidade. Dois fatores são essenciais:

- 🌡️ Temperatura
- 💧 Umidade

Se esses fatores saem do ideal, o vinho pode estragar.

👉 É aí que entra o Arduino: ele funciona como o “cérebro” do sistema, monitorando tudo automaticamente.

---

🧩 O que cada parte do sistema faz (explicação simples)

---

🔌 Arduino Uno (o cérebro)

Recebe as informações dos sensores, toma decisões e controla o que será exibido.

---

🌡️ Sensor DHT11 (os “olhos” do sistema)

Mede:

- Temperatura do ambiente
- Umidade do ar

👉 Ele envia esses dados para o Arduino o tempo todo.

---

📟 Display LCD (a “tela”)

Mostra as informações para o usuário em tempo real:

- Temperatura
- Umidade
- Status do ambiente

👉 É como um visor de painel de carro.

---

🔧 Potenciômetro

Controla o contraste do display (deixa a tela mais clara ou mais escura).

⚙️ Componentes Utilizados

---

- 🔌 Arduino Uno
- 🌡️ Sensor DHT11
- 📟 Display LCD 16x2
- 🎚️ Potenciômetro
- 🔩 Resistores
- 🧩 Protoboard
- 🔗 Jumpers
- 🟢🔴 Leds

---

🔋 Como o sistema funciona (passo a passo)


🥇 1. Medição do ambiente

O sensor DHT11 mede constantemente:

- Temperatura
- Umidade

 Mesmo sem você fazer nada, ele já está coletando dados.

 ---

🥈 2. Envio das informações

O sensor envia esses dados para o Arduino.

 Aqui acontece a “comunicação” entre os componentes.

 ---

🥉 3. Análise pelo Arduino

O Arduino verifica se os valores estão dentro do ideal.

Exemplo de lógica:

- Temperatura muito alta → problema
- Umidade muito baixa → problema
- Tudo normal → ambiente OK

---

🏁 4. Exibição no LCD

O display mostra tudo em tempo real:

Temp: 25°C  Umid: 60%
Status: OK

Ou, em caso de problema:

Temp: 32°C
ALERTA: TEMP ALTA

---

🧠 Lógica do Sistema (como o Arduino “pensa”)


float temperatura = dht.readTemperature();
float umidade = dht.readHumidity();

if (temperatura > 30) {
  // Temperatura alta
}
else if (umidade < 40) {
  // Umidade baixa
}
else {
  // Ambiente ideal
}

👉 O Arduino usa decisões simples (if/else), como se fosse um “SE isso acontecer → FAÇA aquilo”.

---

📊 Exemplo de funcionamento

| Situação do Ambiente | O que aparece no LCD |
| -------------------- | -------------------- |
| Tudo normal          | ✅ Status OK          |
| Temperatura alta     | ⚠️ Temp Alta         |
| Umidade baixa        | ⚠️ Umidade Baixa     |

---

🔍 Observação Técnica


Os valores de temperatura e umidade considerados ideais podem ser ajustados no código.

👉 Isso permite adaptar o sistema para diferentes tipos de vinho ou ambientes.

---

🎯 Objetivos do Projeto


- ✔ Aprender como funciona o Arduino
- ✔ Trabalhar com sensores reais (DHT11)
- ✔ Exibir dados em um display LCD
- ✔ Criar lógica de decisão (if/else)
- ✔ Simular automação do mundo real

---

🛠️ Tecnologias Utilizadas
<p> <img src="https://img.shields.io/badge/Arduino-00979D?style=flat&logo=arduino&logoColor=white"> <img src="https://img.shields.io/badge/Tinkercad-FF6F00?style=flat"> <img src="https://img.shields.io/badge/Eletrônica-Básica-blue"> </p>

---

🔗 Acesse o Projeto

---

👉 Tinkercad:
https://www.tinkercad.com/things/flx3Ey7xao8-copy-of-lcd-i2c/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=3tH6NNJ3n_HNn-PRwhsgSERpuG9ZKq28XKoREHgrQRU

---

👉 YouTube:
https://www.youtube.com/watch?v=uro7mXzho0c

---

👨‍💻 Integrantes
- Rafael Taboada Sobral
- Guilherme Mazzini Nunes Canno
- Luan Schinello Garbin
- Beatriz de Araujo Périgo

---

🏫 Contexto Acadêmico

Projeto desenvolvido para o Checkpoint 2 da FIAP, sob orientação do professor Lucas Demetrius Augusto.
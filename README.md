# 💬 MiniChat MQTT

Um **mini chat estilo WhatsApp (azul claro)** que roda 100% no navegador, sem backend próprio.  
Ele usa o **broker público HiveMQ** via **WebSockets MQTT** para conectar usuários entre si.  

![preview](https://img.shields.io/badge/MQTT-HiveMQ-blue) ![preview](https://img.shields.io/badge/frontend-GitHub%20Pages-green)

---

## ⚡ Funcionalidades

- 🔹 Interface parecida com o WhatsApp, em **azul claro**  
- 🔹 Cada usuário escolhe seu **nome** no primeiro acesso (salvo em cache no navegador)  
- 🔹 Botão para **trocar usuário** e iniciar uma nova sessão  
- 🔹 Digite o nome de outro usuário para iniciar uma conversa privada  
- 🔹 Mensagens aparecem diferenciadas:  
  - **Azul claro** → mensagens enviadas por você  
  - **Cinza** → mensagens recebidas  
- 🔹 Sem histórico: o chat é apenas em tempo real  

---

## 🛠️ Como funciona

- O chat usa **tópicos MQTT dinâmicos** para criar salas privadas.  
- Cada conversa gera um tópico único no formato:

```
minichat2025/usuarios/<usuarioA_usuarioB>
```

> Os nomes são ordenados automaticamente (`alice_bob` em vez de `bob_alice`) para evitar duplicação de tópicos.

- Todos os usuários precisam apenas abrir o **site estático no GitHub Pages** para usar.  

---

## 🚀 Como rodar localmente

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/minichat-mqtt.git
   cd minichat-mqtt
   ```

2. Abra o arquivo `index.html` no navegador.  
   *(não precisa de servidor, funciona direto no navegador!)*  

---

## 🌍 Publicar no GitHub Pages

1. Suba os arquivos para um repositório público no GitHub.  
2. Vá em **Settings > Pages**.  
3. Escolha a branch `main` e a pasta `/root`.  
4. O GitHub Pages vai gerar um link do tipo:

```
https://seuusuario.github.io/minichat-mqtt/
```

Agora qualquer pessoa pode abrir o link e conversar em tempo real com você. 🎉

---

## 📦 Dependências

- [mqtt.js](https://github.com/mqttjs/MQTT.js) (via CDN)  
- Broker público [HiveMQ](https://www.hivemq.com/public-mqtt-broker/)  


## 📜 Licença

Este projeto é livre para estudo e uso pessoal.  
Se quiser expandir, sinta-se à vontade para forkar e melhorar!  

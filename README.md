🚀 **Explorando Microsserviços e Mensageria com RabbitMQ!** 🐇  

Nos últimos dias, me aprofundei no estudo de **microsserviços** e como implementar **mensageria** de forma eficiente utilizando o RabbitMQ. Foi uma experiência incrível construir um projeto prático para consolidar os conceitos e compartilhar aprendizados! 🎓  

💡 **O que é mensageria?**  
Mensageria é um padrão de comunicação assíncrona entre sistemas, onde os serviços trocam mensagens através de filas e exchanges. Isso desacopla os microsserviços, melhora a escalabilidade e garante maior resiliência.  

### 🛠️ Meu projeto:  
Criei três microsserviços que simulam um fluxo de gerenciamento de pedidos de entrega:  

1️⃣ **Cadastro de envios:**  
Recebe eventos que indicam a conclusão de um envio e atualiza o status no banco de dados.  

2️⃣ **Rastreamento de entregas:**  
Gerencia atualizações no rastreamento de pedidos e publica eventos para outros serviços.  

3️⃣ **Notificações:**  
Consome eventos de rastreamento e simula o envio de notificações aos clientes.  

### 🧩 Como funciona?  
- **RabbitMQ:** Utilizei como intermediário para as mensagens. Cada microsserviço publica e consome eventos de forma independente.  
- **Filas e Routing Keys:** As mensagens são roteadas para os serviços corretos com base nas routing keys configuradas.  
- **Eventos:** Eventos como `ShippingOrderUpdatedEvent` e `ShippingOrderCompletedEvent` carregam as informações necessárias para os serviços se comunicarem.  

### 📈 Aprendizados:  
✅ A importância do desacoplamento em arquiteturas distribuídas.  
✅ Como o RabbitMQ ajuda a organizar e gerenciar a comunicação entre serviços.  
✅ O valor de implementar soluções assíncronas para aumentar a escalabilidade.  

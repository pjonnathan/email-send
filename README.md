# Email Verification System  

Este projeto é um sistema de verificação de e-mails desenvolvido com **Java**, **Spring Boot** e **AWS SES (Simple Email Service)**. O objetivo principal é facilitar o envio e a validação de e-mails em aplicações modernas.  

## 🚀 Tecnologias Utilizadas  

- **Java**: Linguagem principal do projeto.  
- **Spring Boot**: Framework para simplificar o desenvolvimento e a configuração do sistema.  
- **AWS SES**: Serviço utilizado para envio e gerenciamento de e-mails.  

## ✨ Funcionalidades  

- Envio de e-mails utilizando o AWS SES.  
- Validação de e-mails enviados.  
- Registro de logs sobre o status de envio e resposta.  

## 📂 Estrutura do Projeto  

```bash  
src/  
├── main/  
│   ├── java/  
│   │   ├── com.example.emailverification/  
│   │   │   ├── controllers/  # Controladores do sistema  
│   │   │   ├── adapters/  # Regras de negócio e integração com AWS SES  
│   │   │   ├── core/  # Configurações do projeto  
│   │   │   ├── infra/  # Modelos e DTOs  
│   │   │   └── application/  # Utilitários auxiliares  
│   ├── resources/  
│   │   ├── application.properties  # Configurações de ambiente  
│   │   ├── templates/  # Templates de e-mail  
└── test/  
    ├── java/  
    │   ├── com.example.emailverification/  
    │   │   └── tests/  # Testes unitários e de integração  
```  

## 🛠️ Configuração e Execução  

### Pré-requisitos  
- **Java 17** ou superior.  
- **Spring Boot** instalado.  
- Conta configurada no **AWS SES**.  

### Configurando o Projeto  
1. Clone este repositório:  
   ```bash  
   git clone https://github.com/pjonnathan/email-send.git  
   ```  

2. Acesse o diretório do projeto:  
   ```bash  
   cd email-verification-system  
   ```  

3. Configure as credenciais do AWS no arquivo `application.properties`:  
   ```properties  
   aws.access-key=YOUR_AWS_ACCESS_KEY  
   aws.secret-key=YOUR_AWS_SECRET_KEY  
   aws.ses.region=YOUR_AWS_REGION  
   ```  

4. Configure os dados padrão de envio:  
   ```properties  
   email.sender=noreply@yourdomain.com  
   email.subject=Verification Email  
   ```  

### Executando o Sistema  
No terminal, execute o seguinte comando:  
   ```bash  
   ./mvnw spring-boot:run  
   ```  

A aplicação estará disponível em:  
`http://localhost:8080`  

## 🔗 Rotas da API  

| Método | Endpoint              | Descrição                |  
|--------|-----------------------|--------------------------|  
| POST   | `/api/v1/email/send`  | Envia um e-mail          |  
| GET    | `/api/v1/email/status`| Verifica o status do e-mail|  

## 🧪 Testes  
Execute os testes do projeto com:  
   ```bash  
   ./mvnw test  
   ```  

## 💡 Melhorias Futuras  

- Adicionar suporte a outras plataformas de envio de e-mail (ex.: SendGrid).  
- Melhorar o design dos templates de e-mail.  
- Implementar fila de mensagens para maior escalabilidade (ex.: AWS SQS).  

## 📜 Licença  

Este projeto está licenciado sob a [MIT License](LICENSE).  

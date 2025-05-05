# 💱 Conversor de Moedas em Java

Este projeto é um **Conversor de Moedas** desenvolvido em Java, que se conecta a uma API de câmbio em tempo real, processa os dados no formato JSON com a biblioteca **Gson** e oferece uma interface de linha de comando para o usuário realizar conversões entre moedas da América Latina e o Dólar.

## 📌 Funcionalidades

- 🔄 Conversão entre moedas:
    - USD – Dólar Americano
    - ARS – Peso Argentino
    - BOB – Boliviano Boliviano
    - BRL – Real Brasileiro
    - CLP – Peso Chileno
    - COP – Peso Colombiano
- 🌐 Integração com API ExchangeRate-API
- 💾 Cache local dos dados em arquivo JSON (`taxas.json`)
- 📤 Leitura e escrita de JSON com a biblioteca **Gson**
- 🧠 Estrutura modular, separada em classes

## 🛠️ Requisitos

- Java JDK 11 ou superior
- Biblioteca [Gson](https://github.com/google/gson) (`gson-2.x.x.jar`)

## 📁 Estrutura do Projeto

```
ConversorMoedas/
│
├── Main.java              → Ponto de entrada da aplicação
├── Conversor.java         → Lógica de conversão e interface com usuário
├── TaxasService.java      → Conexão com a API de câmbio
├── JsonUtils.java         → Manipulação de arquivos JSON com Gson
├── taxas.json             → (Gerado automaticamente) Cache local das taxas
├── gson.jar               → Biblioteca Gson
└── README.md              → Documentação do projeto
```

## 🚀 Como Executar

### 🔧 Terminal (Linha de Comando)

1. Compile o projeto:
   ```bash
   javac -cp gson.jar *.java
   ```

2. Execute o programa:
    - **Windows**:
      ```bash
      java -cp .;gson.jar Main
      ```
    - **Linux/macOS**:
      ```bash
      java -cp .:gson.jar Main
      ```

### 💻 IntelliJ IDEA / Eclipse

- Crie um projeto Java e adicione todos os arquivos `.java`.
- Adicione o `gson.jar` às dependências.
- Execute a classe `Main.java`.

## 🧪 Exemplo de Uso

```
*** Conversor de Moedas ***
0 - USD
1 - ARS
2 - BOB
3 - BRL
4 - CLP
5 - COP

Escolha a moeda de origem (número): 0
Escolha a moeda de destino (número): 3
Digite o valor a ser convertido: 100

Resultado: 100.00 USD = 508.50 BRL
Deseja converter outro valor? (s/n): s
```

## 🔗 API Utilizada

- [ExchangeRate-API](https://www.exchangerate-api.com/)
- Endpoint:  
  `https://v6.exchangerate-api.com/v6/f812567340f8166a8a2ce177/latest/USD`

## 📚 Licença

Este projeto é de uso educacional e livre para modificações.

## 👨‍💻 Autor

Desenvolvido com fins de aprendizado por Augusto Câmara:
- Requisições HTTP com `HttpClient`
- Processamento de JSON com Gson
- Interação com o usuário no console

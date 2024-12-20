# projeto_requests

## Descrição do Projeto
Este projeto utiliza a API do GitHub para listar repositórios públicos de usuários específicos e extrair informações sobre as linguagens de programação utilizadas. O resultado é exportado como arquivos CSV, permitindo análises posteriores. 

## Funcionalidades
- Listar repositórios públicos de um usuário do GitHub.
- Extrair nomes dos repositórios e suas respectivas linguagens de programação.
- Gerar um DataFrame com os dados processados.
- Exportar os dados para arquivos CSV organizados.

## Tecnologias Utilizadas
- **Python**: Linguagem principal do projeto.
- **Requests**: Para fazer chamadas à API do GitHub.
- **Pandas**: Para manipulação e organização dos dados.
- **dotenv**: Para gerenciar variáveis de ambiente de forma segura.

## Como Configurar e Executar

### Pré-requisitos
1. **Python 3.8 ou superior**
2. Atualize o WSL (Windows Subsystem for Linux):
   ```bash
   sudo apt update && sudo apt upgrade
   ```
3. Instalar as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```
4. Criar um arquivo `.env` na raiz do projeto contendo a chave de autenticação da API do GitHub:
   ```env
   GITHUB_TOKEN=seu_token_de_autenticacao_aqui
   ```

### Estrutura de Diretórios
```plaintext
📂 projeto
├── main.py  # Código principal
├── .env  # Arquivo com token da API
├── requirements.txt  # Lista de dependências do projeto
├── data_processed  # Diretório para armazenar arquivos CSV
```

### Executando o Projeto
1. Certifique-se de que o diretório `data_processed` exista na raiz do projeto. Caso não exista, crie-o:
   ```bash
   mkdir data_processed
   ```
2. Execute o script principal:
   ```bash
   python main.py
   ```
3. Após a execução, os arquivos CSV contendo os dados extraídos estarão disponíveis no diretório `data_processed`.

## Exemplo de Uso
O código atual coleta dados dos repositórios públicos dos seguintes usuários:
- `amzn` (Amazon)
- `netflix` (Netflix)
- `spotify` (Spotify)

Os dados são exportados como:
- `linguagens_amzn.csv`
- `linguagens_netflix.csv`
- `linguagens_spotify.csv`

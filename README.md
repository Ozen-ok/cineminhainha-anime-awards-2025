# CINEMINHAINHA ANIME AWARDS 🏆

Aplicação web desenvolvida para organizar uma votação entre amigos das músicas de abertura (*openings*) e encerramento (*endings*) de animes.

O sistema permite que cada participante assista aos vídeos, atribua notas e acompanhe os resultados consolidados da votação.

## Funcionalidades

- Votação separada por categorias: Openings e Endings.
- Reprodução dos vídeos diretamente na aplicação.
- Seleção do participante que está votando.
- Avaliação de 0 a 10, em intervalos de 0,5 ponto.
- Salvamento dos votos no JSONBin.io.
- Controle dos animes já avaliados por participante e categoria.
- Possibilidade de remover o último voto para alterá-lo.
- Exibição dos votos detalhados e ranking médio por categoria.

## Tecnologias

- Python
- Streamlit
- Pandas
- Requests
- JSONBin.io
- python-dotenv

## Como executar localmente

### 1. Pré-requisitos

- Python 3.9 ou superior.
- Uma conta no [JSONBin.io](https://jsonbin.io/) e um Bin configurado para armazenar os votos.

### 2. Clonar o repositório

```bash
git clone https://github.com/Ozen-ok/animeawards.git
cd animeawards
```

### 3. Criar e ativar um ambiente virtual (opcional, recomendado)

Windows:

```powershell
python -m venv .venv
.venv\Scripts\activate
```

Linux/macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 5. Configurar o JSONBin

Crie uma cópia do arquivo de exemplo:

Windows:

```powershell
Copy-Item .env.example .env
```

Linux/macOS:

```bash
cp .env.example .env
```

Edite o arquivo `.env` e informe os dados do seu JSONBin:

```env
JSONBIN_BIN_ID=seu_bin_id
JSONBIN_MASTER_KEY=sua_chave_master
```

- `JSONBIN_BIN_ID`: identificador do Bin que armazena os votos.
- `JSONBIN_MASTER_KEY`: chave de acesso usada pela aplicação para consultar e atualizar o Bin.

O arquivo `.env` contém credenciais e não deve ser enviado ao GitHub. O `.gitignore` já está configurado para ignorá-lo.

### 6. Iniciar a aplicação

```bash
streamlit run main.py
```

O Streamlit exibirá no terminal o endereço local para acessar a aplicação pelo navegador.

## Armazenamento dos votos

Os votos são armazenados em um Bin do JSONBin.io. A aplicação consulta esse registro ao iniciar e envia as alterações quando um participante salva ou modifica um voto.

Para utilizar a aplicação com outro conjunto de votações, configure o identificador e a chave de acesso de um Bin apropriado no arquivo `.env`.

## Observações

Este é um projeto pessoal desenvolvido para organizar uma votação entre amigos. Ele foi criado como uma aplicação de uso específico e não recebe manutenção contínua.

A disponibilidade da votação depende do serviço JSONBin.io e das credenciais configuradas pelo responsável pela aplicação.

## Autor

**Ozen**

[Repositório no GitHub](https://github.com/Ozen-ok/animeawards)

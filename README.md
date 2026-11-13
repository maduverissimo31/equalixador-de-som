# SONORA — Equalizador de áudio

Um site responsivo de equalização de áudio feito com **Python + Flask**, HTML, CSS e JavaScript.

## Recursos
- Carregamento de áudio local (MP3, WAV, OGG e formatos suportados pelo navegador).
- Reprodução e pausa.
- Seis bandas de frequência: 60 Hz, 170 Hz, 350 Hz, 1 kHz, 3.5 kHz e 10 kHz.
- Predefinições Flat, Graves+, Vocal, Agudos+ e Rock.
- Interface adaptável para celular e computador.

> O processamento do áudio acontece no navegador usando a Web Audio API. O Flask serve a página; o arquivo de áudio escolhido permanece no dispositivo do usuário.

## Executar no computador

1. Instale Python 3.10 ou superior.
2. Abra o terminal na pasta do projeto.
3. Crie e ative um ambiente virtual (opcional, mas recomendado):

   ```bash
   python -m venv .venv
   # Windows:
   .venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate
   ```

4. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

5. Inicie o site:

   ```bash
   python app.py
   ```

6. Abra http://127.0.0.1:5000 no navegador.

## Publicar no GitHub

1. Crie um repositório no GitHub, por exemplo `equalizador-sonora`.
2. Envie todos os arquivos desta pasta para o repositório.
3. O código ficará disponível no GitHub para consulta e colaboração.

### Importante sobre hospedagem

O **GitHub Pages não executa Python/Flask**. Para publicar esta versão Flask na internet, conecte o repositório a um serviço de hospedagem que execute Python, como Render:

- Crie um novo Web Service e conecte seu repositório.
- Build Command: `pip install -r requirements.txt`
- Start Command: `gunicorn app:app`

Se a intenção for hospedar exclusivamente pelo GitHub Pages, será necessário usar uma versão estática (HTML/CSS/JavaScript), sem servidor Flask.

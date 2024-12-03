# Assistente Virtual com Processamento de Linguagem Natural (PLN)

Este projeto implementa um **assistente virtual** baseado em **Processamento de Linguagem Natural (PLN)** utilizando Python. O assistente é capaz de reconhecer comandos de voz, realizar ações automatizadas como buscar no Wikipedia, abrir o YouTube e localizar estabelecimentos próximos, além de converter texto em fala e fala em texto.

---

## 🚀 Funcionalidades

- **Transformação de texto em fala (Text-to-Speech)**: Converte texto em áudio utilizando a biblioteca `gTTS`.
- **Transformação de fala em texto (Speech-to-Text)**: Reconhece comandos de voz utilizando a biblioteca `SpeechRecognition`.
- **Comandos Automatizados**:
  - Busca informações no Wikipedia.
  - Abre o YouTube para pesquisar vídeos.
  - Localiza estabelecimentos próximos, como farmácias, no Google Maps.
- **Interação natural**: O assistente responde de forma dinâmica a comandos como "pesquisar", "abrir YouTube" e "localizar farmácia".

---

## 🛠️ Tecnologias Utilizadas

- **Python**
  - [`gTTS`](https://pypi.org/project/gTTS/): Para converter texto em áudio.
  - [`SpeechRecognition`](https://pypi.org/project/SpeechRecognition/): Para reconhecimento de fala.
  - [`PyAudio`](https://pypi.org/project/PyAudio/): Para capturar áudio do microfone (necessário em ambientes locais).
  - [`Wikipedia`](https://pypi.org/project/wikipedia/): Para buscas no Wikipedia.
  - [`Webbrowser`](https://docs.python.org/3/library/webbrowser.html): Para abrir URLs no navegador.

---

## 📋 Requisitos

Certifique-se de que as seguintes dependências estão instaladas:

- Python 3.7 ou superior
- As bibliotecas necessárias listadas no arquivo `requirements.txt`.

No **Google Colab**, o microfone não é suportado diretamente. Use arquivos de áudio como entrada ou execute o projeto em um ambiente local para capturar áudio ao vivo.

---

## ⚙️ Instalação

### 1. Clone o Repositório
```bash
git clone https://github.com/leticiafcarvalho/AssistenteVirtual.git
cd assistente-virtual
```

### 2. Instale as Dependências
```bash
pip install -r requirements.txt
```

### 3. Configuração Adicional (Para Áudio ao Vivo)
Se estiver usando reconhecimento de fala com microfone:
- **Windows**: Instale o PyAudio usando o `.whl` do site [Gohlke](https://www.lfd.uci.edu/~gohlke/pythonlibs/).
- **Linux/Ubuntu**:
  ```bash
  sudo apt-get install portaudio19-dev
  pip install pyaudio
  ```

---

## 🖥️ Como Usar

### 1. Iniciar o Assistente
No terminal, execute:
```bash
python main.py
```

### 2. Interagir com o Assistente
- Exemplos de comandos:
  - **"Pesquisar sobre inteligência artificial"**: Realiza uma busca no Wikipedia.
  - **"Abrir YouTube"**: Abre o YouTube no navegador.
  - **"Localizar farmácia próxima"**: Busca farmácias no Google Maps.
  - **"Sair"**: Finaliza o assistente.

### 3. Testar no Google Colab
No Google Colab, substitua o reconhecimento de fala pelo método de entrada via texto para simular comandos:
```python
def speech_to_text():
    return input("Digite seu comando: ").lower()
```


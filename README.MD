# 🗣️ TalkingLLM

Uma ferramenta interativa de IA que permite conversar com um agente LLM (Large Language Model) usando comandos de voz, integrando transcrição automática (Whisper), síntese de fala (OpenAI TTS) e análise em tempo real de DataFrames pandas.

---

## 🚀 Funcionalidades

- 🎙️ **Gravação de áudio via hotkey** (Ctrl) para comandos por voz.
- ✍️ **Transcrição automática** do áudio usando [Whisper](https://github.com/openai/whisper).
- 🤖 **Geração de respostas com LLMs** (OpenAI GPT-3.5/GPT-4).
- 🧑‍💻 **Respostas baseadas na análise de DataFrame pandas** (`df_rent.csv`) usando [LangChain Agents](https://python.langchain.com/).
- 🔊 **Síntese de fala**: resposta do LLM é lida em voz alta com [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech).
- 🔄 **Execução assíncrona**: gravação/escuta e reprodução de áudio acontecem simultaneamente.
- 🧪 **Script de agente rápido**: use o `df_agent.py` para testar prompts diretamente no DataFrame sem voz.

---

## 🛠️ Tecnologias Utilizadas

- Python 3.8+
- [openai](https://pypi.org/project/openai/)
- [whisper](https://github.com/openai/whisper)
- [langchain](https://python.langchain.com/)
- [sounddevice](https://python-sounddevice.readthedocs.io/)
- [soundfile](https://pysoundfile.readthedocs.io/)
- [pynput](https://pypi.org/project/pynput/)
- [dotenv](https://pypi.org/project/python-dotenv/)
- [pandas](https://pandas.pydata.org/)

---

## ⚙️ Como Usar

1. **Clone o repositório**
   ```bash
   git clone https://github.com/yagosamu/talking_llm.git
   cd talking_llm
   ```

2. **Instale as dependências**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure as chaves da OpenAI**
   - Crie um arquivo `.env` com sua chave da OpenAI:
     ```
     OPENAI_API_KEY=sk-...
     ```

4. **Garanta o arquivo `df_rent.csv`**
   - Coloque seu DataFrame CSV na raiz do projeto, com o nome `df_rent.csv`.

5. **Execute o projeto por voz**
   ```bash
   python talking_llm.py
   ```

   - Mantenha o terminal aberto.
   - Pressione e solte **Ctrl** para começar/parar a gravação.
   - Fale seu comando ou pergunta.
   - O áudio será transcrito, processado pelo LLM, analisado no DataFrame e a resposta será lida em voz alta.

6. **Teste comandos diretamente no DataFrame (sem voz)**
   ```bash
   python df_agent.py
   ```
   - O prompt enviado no script é um exemplo para testar o agent ("Quantas linhas há no conjunto de dados?"). Edite o arquivo para testar outros comandos/análises.

---

## 📝 Exemplo de Interação

- **Você:** (Aperta Ctrl) "Qual o valor médio dos aluguéis no DataFrame?" (Solta Ctrl)
- **IA:** "O valor médio dos aluguéis é R$ 1.350,00."

---

## 🧩 Estrutura dos Arquivos

- `talking_llm.py` — Código principal, integra áudio, transcrição, LLM e análise do DataFrame.
- `df_agent.py` — Script simples para testar prompts no DataFrame via terminal.
- `df_rent.csv` — Arquivo de dados analisados pelo agente.
- `.env` — Suas chaves e variáveis de ambiente.
- `requirements.txt` — Dependências do projeto.

---

## 🤝 Contribuições

Pull requests são bem-vindos! Sugestões, melhorias e correções são muito apreciadas.

---

Desenvolvido por [yagosamu](https://github.com/yagosamu) 🚀
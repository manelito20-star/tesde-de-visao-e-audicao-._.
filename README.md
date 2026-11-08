# 🩺 Triagem Clínica Avançada: Visão & Audição

Aplicação Android desenvolvida em **Kotlin** e **Jetpack Compose** (Material 3) para triagem pré-clínica e avaliação sensorial de alta precisão de visão e audição.

---

## 🌟 Funcionalidades Principais

### 1. 🎧 Audiometria de Alta Precisão
- **Frequências Clínicas:** Avaliação em 6 frequências padrão (250 Hz, 500 Hz, 1000 Hz, 2000 Hz, 4000 Hz e 8000 Hz) para ambos os ouvidos.
- **Limiares de Intensidade:** 5 níveis de intensidade decrescente (do audível ao limiar ultra-fino de `0.015f`).
- **Medidor de Ruído Ambiente:** Utiliza o microfone do dispositivo (`AudioRecord`) em tempo real para verificar se o ambiente possui menos de 55 dB, garantindo silêncio adequado para o exame.
- **Audiograma Gráfico Profissional:** Plota curvas bidimensionais em `Canvas` (Ouvido Direito vs. Ouvido Esquerdo) idênticas a um laudo médico.

### 2. 👁️ Acuidade Visual (Tabela de Snellen)
- **8 Níveis Clínicos:** Avaliação progressiva desde `20/200` até `20/15`.
- **Múltiplos Optótipos:** Linhas com letras decrescentes para rigor na medição.
- **Filtros por Olho:** Permite testar Ambos os olhos, Olho Esquerdo e Olho Direito separadamente.

### 3. 🌀 Teste de Astigmatismo
- **3 Padrões Geométricos Rigorosos:** Roda Radiada (Sol), Linhas Paralelas Cruzadas e Anéis Concêntricos Finos.
- **Distorção Cilíndrica:** Avalia se o utilizador percebe linhas borradas ou mais escuras em determinados eixos.

### 4. 🎨 Teste de Daltonismo (Pranchas Ishihara)
- **8 Pranchas de Alta Dificuldade:** Mosaicos de pontos coloridos com contrastes subtis e números ocultos.

### 5. 🧠 Exame Duplo Avançado (Visão & Audição Simultâneas com TTS)
- **40 Rodadas Rigorosas:** Exame cruzado combinando estímulo visual e auditivo em simultâneo.
- **Foco em Micro-Fontes:** Escala progressiva que desce até tamanhos microscópicos (`7sp`).
- **Sintetizador de Voz (Text-to-Speech):** Utiliza fonemas e letras claras para testar a coerência multissensorial sem ambiguidades.
- **Feedback Imediato:** Confirmação em tempo real de cada resposta do utilizador.

### 6. 📊 Relatório Clínico Consolidado
- Sumário textual completo com todos os resultados obtidos e respetivo parecer clínico indicando a necessidade de consulta com especialista (Oftalmologista / Otorrinolaringologista).

---

## 🛠️ Tecnologias e Arquitetura

- **Linguagem:** 100% Kotlin
- **UI:** Jetpack Compose & Material 3
- **Processamento de Áudio:** `AudioTrack` (síntese de tons puros estéreo) e `AudioRecord` (análise de ruído dB).
- **Renderização Gráfica:** Custom `Canvas` para Audiogramas, Astigmatismo e Pranchas Ishihara.
- **Acessibilidade & Voz:** `TextToSpeech` (TTS) para comandos auditivos sincronizados.

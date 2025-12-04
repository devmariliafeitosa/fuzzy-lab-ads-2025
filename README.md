# 🌀 **Projeto Fuzzy – Controle Inteligente de Velocidade de Ventilador**
### *Planejamento Inicial do Sistema Fuzzy para Ambientes Fechados*

---

## 👥 **1. Integrantes da Dupla**
- **Marília da Silva Feitosa**  
  🔗 GitHub: [@devmariliafeitosa](https://github.com/devmariliafeitosa)

- **Lorhane Angélica Gonçalves**  
  🔗 GitHub: [@devmariliafeitosa](https://github.com/devmariliafeitosa)

---

## 🎯 **2. Tema Escolhido**
### **Tema C – Controlador Fuzzy para Ventilação em Ambientes Fechados**

---

## 📝 **3. Descrição Inicial do Problema**

Ambientes internos podem variar rapidamente de temperatura e nível de ocupação, exigindo ajustes constantes na ventilação para manter o conforto térmico. Um sistema tradicional (liga/desliga) não é eficiente, pois causa oscilações bruscas e não responde de forma suave às mudanças do ambiente.

O objetivo deste projeto é implementar um **controlador fuzzy**, capaz de:

- Ajustar automaticamente a **velocidade do ventilador (%)**
- Considerar simultaneamente:
  - **Temperatura interna (°C)**
  - **Taxa de ocupação do ambiente (%)**
- Fornecer uma resposta suave, contínua e inteligente para diversas condições reais.

Esse controlador pode ser utilizado em:
- Salas de aula  
- Escritórios  
- Ambientes climatizados  
- Auditórios  
- Laboratórios  

---

## 🧠 **4. Planejamento Inicial do Projeto**

A seguir estão as etapas estruturadas conforme solicitado no enunciado.

---

### ✔️ **4.1 Definição das Variáveis Linguísticas**

### **Entradas**

#### 🌡️ *Temperatura (°C)*
- **Fria**
- **Amena**
- **Quente**

#### 👥 *Ocupação (%)*
- **Vazia**
- **Média**
- **Cheia**

### **Saída**

#### 🌀 *Velocidade do Ventilador (%)*
- **Baixa**
- **Média**
- **Alta**

---

### ✔️ **4.2 Esboço das Funções de Pertinência**

As funções de pertinência serão implementadas utilizando principalmente formatos:

- **Triangular (trimf)**
- **Trapezoidal (trapmf)**

Exemplos planejados:
- Temperatura *fria*: 0–18°C  
- Temperatura *quente*: 25–40°C  
- Ocupação *cheia*: acima de 70%  
- Ventilador *alto*: 60–100%  

Esses formatos serão refinados após testes e gráficos.

---

### ✔️ **4.3 Estrutura Inicial da Base de Regras**

O sistema seguirá a lógica:

SE (Temperatura = X) E (Ocupação = Y)
ENTÃO (Velocidade = Z)

Regras planejadas:

- Quente ∧ Cheia ➝ Ventilador **Alto**
- Fria ∧ Vazia ➝ Ventilador **Baixo**
- Amena ∧ Média ➝ Ventilador **Médio**
- Quente ∧ Vazia ➝ Ventilador **Médio**
- Fria ∧ Cheia ➝ Ventilador **Médio**

Novas regras poderão ser adicionadas durante a calibração.

---

### ✔️ **4.4 Método de Inferência**

O sistema utilizará:

- **Método de Inferência**: Mamdani  
- **Operadores fuzzy**:  
  - Implicação → *mínimo*  
  - Agregação → *máximo*  
  - Operador AND → *mínimo*  

---

### ✔️ **4.5 Método de Defuzzificação**

Será utilizada a técnica:

- **Centroide (centroid)**  
  Por ser a mais estável e amplamente utilizada em controladores contínuos.

---

### ✔️ **4.6 Planejamento dos Cenários de Teste**

Serão realizados pelo menos **5 testes**, incluindo casos típicos e extremos:

1. **Temperatura alta + sala cheia → ventilador alto**  
2. **Temperatura baixa + sala vazia → ventilador baixo**  
3. **Temperatura amena + ocupação média → ventilador médio**  
4. **Temperatura muito alta + ocupação baixa → valor intermediário**  
5. **Temperatura fria + ocupação cheia → ventilador médio**  

Cada resultado será analisado e justificado no relatório final.

---

## 📁 **5. Estrutura Inicial do Repositório**

- **fuzzy-lab-ads-2025/**
  - **codigo/**
    - `codigo_aqui.py` — arquivo que receberá os códigos do controlador fuzzy
  - **relatorio/**
    - `relatorio_fuzzy.pdf` — relatório técnico (adicionado ao final do projeto)
  - **imagens/**
    - arquivos `.png` contendo gráficos de pertinência e saída fuzzy
  - `requirements.txt`
  - `README.md`


---

## 🧩 **6. Observações Finais**

- Este README representa o planejamento inicial do projeto conforme exigido pelo professor.  
- A próxima etapa será implementar o controlador fuzzy em `codigo/codigo_aqui.py`.  
- Todos os gráficos serão exportados automaticamente para a pasta **/imagens**.  
- O relatório técnico será desenvolvido posteriormente com base no código final.  

---



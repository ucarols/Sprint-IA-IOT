# 📍 Projeto de organização e monitoramento de motos no pátio - Mottu

Esse projeto tem o objetivo de otimizar a gestão de motos no pátio da Mottu utilizando **classificação por cores**, **visão computacional** e **monitoramento em tempo real**.

---
##  Introdução

A Mottu enfrenta desafios como:

- Imprecisão na localização das motos.
- Atrasos nos atendimentos e manutenções.
- Baixa eficiência operacional.
---

## 🎯 Objetivos

- Melhorar a organização das motos por prioridade.
- Reduzir atrasos e tempo de resposta.
- Aumentar a eficiência na gestão de veículos.
- Exibir dados em tempo real sobre status e permanência das motos.

---

##  Solução Proposta

### 1. Classificação por Cores

Cada moto recebe um adesivo de cor correspondente ao seu status:

| Cor     | Classificação            | Descrição                            | Tempo Limite        |
|---------|--------------------------|--------------------------------------|---------------------|
| 🟢 Verde   | Pronta para uso           | Moto liberada para entrega           | Sem limite          |
| 🟡 Amarelo | Reparos rápidos           | Pneus, óleo, pequenos reparos        | 15 minutos          |
| 🔴 Vermelho| Reparos graves           | Motor, elétrica                      | Variável            |
| 🟣 Roxo    | Problemas administrativos | Sem placa, pendências no Detran     | Até resolução       |

### 2. Organização do Pátio

- Áreas delimitadas por cores.
- Cada moto deve estar na área da sua classificação.

### 3. Visão Computacional e Alertas

- Câmeras fazem leitura de adesivos e placas.
- Sistema alerta se moto estiver fora de lugar ou tempo.
- Colaborador pode ler a placa e visualizar:
  - Problema reportado
  - Data/hora de entrada
  - Status atual
  - Informações da moto

---

## 🔁 Fluxo de Funcionamento

1. **Triagem** → Moto é avaliada e recebe um adesivo.
2. **Posicionamento** → Moto vai para a área correspondente.
3. **Monitoramento** → Câmeras identificam adesivos e alertam inconsistências.
4. **Consulta de Dados** → Leitura da placa mostra detalhes no dashboard.

---
## 💻 Como usar

Este projeto detecta **adesivos coloridos** e **placas em motos** usando técnicas de **visão computacional com OpenCV, YOLOv8 e EasyOCR**.

---

###  Requisitos

- Python 3.8 ou superior  
- OpenCV  
- EasyOCR  
- Ultralytics YOLOv8  

---

##  Como testar no Google Colab

1. **Abra o notebook no Google Colab**  
   👉 [Clique aqui para abrir o MotoTracker no Google Colab](https://colab.research.google.com/drive/13E9kYtBrqN-Z7Hl6mTTa7llfcvMASD1o?usp=sharing)

2. **Baixe a imagem de teste**  
   A imagem usada nos testes está disponível no Google Drive:  
   📷 [Clique aqui para baixar a imagem](https://drive.google.com/drive/folders/1QA9EaYPAf7aKCOgrYI7he_4Qro-vn2Nr?usp=sharing)

3. **Importe a imagem para o Colab**  
   Após baixar, faça o upload da imagem (`motocomplaca.png`,  `motoadesivo.jpg`, `moto2.png`) no ambiente do Colab.


4. **Execute o código**  
   - Instale as dependências com:
     ```python
     !pip install opencv-python easyocr ultralytics
     ```
   - Execute o notebook seguindo as instruções para carregar e processar a imagem.

---

## 📸 Imagens

-  **Adesivos coloridos detectados**
![testepatio](https://github.com/user-attachments/assets/acc91df2-7105-4bf1-8511-2dcf445129b5)

-  **Leitura automática de placas** com reconhecimento óptico (OCR)
![placaMoto2](https://github.com/user-attachments/assets/041d91aa-4e6b-455f-afab-e6766bdddb69)

![placa](https://github.com/user-attachments/assets/d9c9de02-04e3-40ea-9d0b-b6cfaf19d6f5)

---

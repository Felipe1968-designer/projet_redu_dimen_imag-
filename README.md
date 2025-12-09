# 📘 Projeto Final — Redução de Dimensionalidade (DIO)

## 🖼️ Transformação de Imagens em Python Puro

Este projeto implementa **redução de dimensionalidade** utilizando apenas **Python puro**, sem bibliotecas externas (como OpenCV, PIL ou NumPy).
O objetivo é demonstrar como manipular imagens no formato **BMP 24 bits**, convertendo:

* Imagem colorida → **Tons de Cinza**
* Imagem em tons de cinza → **Preto e Branco (binarização)**

---

## 🚀 Tecnologias Utilizadas

* **Python Puro**
* Manipulação manual de bytes
* Formato BMP (24 bits e 8 bits)

---

## 📂 Estrutura do Projeto

```
📁 projeto-reducao-dimensionalidade
│
├── red_dim_img_python.py          # Código principal (carrega BMP, converte e salva)
├── README.md           # Documentação
└── violao.bmp          # Imagem de exemplo (opcional)
```

---

## 🧠 Como o Projeto Funciona

### ✔️ 1. Leitura de Imagem BMP (24 bits)

O código lê manualmente:

* Cabeçalho do BMP
* Largura / Altura
* Bits por pixel (bpp)
* Dados RGB de cada pixel

### ✔️ 2. Conversão para Tons de Cinza

Usa a fórmula perceptual padrão:

```
gray = 0.299 R + 0.587 G + 0.114 B
```

### ✔️ 3. Binarização (Preto e Branco)

Utiliza um **limiar padrão de 128**:

```
pixel = 255 if gray ≥ 128 else 0
```

### ✔️ 4. Salvamento em BMP 8 Bits

O arquivo gerado contém:

* Cabeçalho BMP
* Paleta de 256 tons de cinza
* Imagem em tons de cinza ou PB

---

## 🧪 Como Executar no Google Colab

### 1️⃣ Faça upload da imagem BMP (24 bits)

No Colab clique em:

```
📁 Arquivos → Upload → escolha "violao.bmp"
```

A imagem será salva em:

```
/content/violao.bmp
```

### 2️⃣ Ajuste o nome da imagem no código

```python
arquivo = "/content/violao.bmp"
```

### 3️⃣ Execute o script

```python
!python projeto.py
```

### 4️⃣ Baixe as imagens geradas:

* `resultado_cinza.bmp`
* `resultado_pb.bmp`

---

## 🐛 Problemas Comuns

### ❌ FileNotFoundError

Motivos possíveis:

* Nome do arquivo diferente (`Violao.bmp` ≠ `violao.bmp`)
* Extensão errada
* Arquivo salvo em `/sample_data`

### ✔️ Solução:

Liste os arquivos do Colab:

```python
import os
os.listdir("/content")
```

Copie o nome exatamente como aparece.

---

## 🌟 Objetivo Educacional

Este projeto foi desenvolvido para a plataforma **DIO — Digital Innovation One**, como parte do módulo de **Redução de Dimensionalidade e Pré-Processamento**.

O foco é aprender:

* Manipulação de arquivos binários
* Estrutura interna do formato BMP
* Conversão manual de pixels
* Fundamentos de visão computacional

---



## ✅ Conclusão

Este projeto consolida os fundamentos de manipulação de imagens e demonstra como operações simples podem reduzir dimensionalidade preservando informações essenciais. É uma aplicação direta dos conceitos estudados no módulo.

---

## 🚀 Autor

**Prof. Felipe Fuentes**
Projeto desenvolvido para conclusão de módulo na plataforma **DIO**.


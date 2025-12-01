# Skin Lesion Classification Using Machine Learning & Deep Learning**

## 🧠 **Overview**

Este repositório contém o projeto desenvolvido para o artigo no formato IEEE, cujo objetivo é **classificar lesões de pele em três categorias clínicas** — **Benigno**, **Suspeito** e **Maligno** — usando tanto **modelos clássicos de Machine Learning** quanto **redes neurais convolucionais (CNN)** com **Transfer Learning**.

O projeto utiliza o dataset **HAM10000** (Skin Cancer MNIST) e inclui:

* Extração de features tradicionais (HOG, LBP, histogramas)
* Treino e avaliação de modelos:

  * **SVM**
  * **Random Forest**
  * **MLP**
* Preparação de dados para CNN (folder structure + augmentation)
* Transfer Learning com **ResNet50**
* Fine-tuning do modelo
* Avaliação completa (métricas + matriz de confusão)

Este repositório também contém o notebook completo utilizado para gerar todos os experimentos.

---

## 📊 **Classes trabalhadas**

As 7 classes originais do HAM10000 foram remapeadas para 3 grupos:

| Original        | Novo Grupo   |
| --------------- | ------------ |
| nv, df, vasc    | **Benigno**  |
| bkl             | **Suspeito** |
| mel, bcc, akiec | **Maligno**  |

Esse agrupamento facilita a tarefa clínica e melhora a robustez do modelo.

---


## 📦 **Dataset**

O dataset principal é:

### **HAM10000 — Skin Cancer MNIST**

Disponível publicamente no Kaggle:
[https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)

O download do dataset no notebook é feito automaticamente via:

```python
import kagglehub
path = kagglehub.dataset_download("kmader/skin-cancer-mnist-ham10000")
```

---

## 🧩 **Requisitos**

### Se rodar *localmente*:

Instale:

```
pip install numpy pandas matplotlib scikit-learn scikit-image tensorflow kagglehub seaborn tqdm
```

Ou crie um ambiente:

```
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

### Se rodar no **Google Colab**:

Nenhuma instalação extra é necessária além das células do notebook — tudo já está automatizado.

---

## 🏗️ **Etapas do Notebook**

### **1. Preparação e download do dataset**

* Download via `kagglehub`
* Carregamento dos metadados
* Remapeamento para 3 classes

### **2. Modelos clássicos (ML tradicional)**

* Extração de features: HOG, LBP, histogramas HSV
* Treino:

  * SVM
  * Random Forest
  * MLP
* Avaliação com métricas (precision/recall/F1)

### **3. CNN (Deep Learning)**

* Criação das pastas (train/valid/test)
* Data augmentation
* Transfer learning com ResNet50
* Fine-tuning
* Class weights para balanceamento
* Avaliação completa

### **4. Resultados**

* Relatórios completos
* Matriz de confusão
* Comparação entre modelos
* Discussão sobre viés, erros e limitações

---

## 📝 **Artigo IEEE**

O artigo completo está disponível no arquivo:

```
IEEE_Trio_Nomes.pdf
```
---

## 👨‍💻 **Autor**

- Davi Leahy

---

## 📜 **Licença**

MIT License

---
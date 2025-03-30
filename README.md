# Processador de Imagens a partir de Arquivos Texto

## 📝 Descrição

Este projeto implementa um processador de imagens em Python que:
- Lê imagens armazenadas em arquivos texto (`.txt`)
- Converte para formato PNG
- Aplica transformações como escala de cinza e substituição de cores
- Oferece interface interativa para experimentação

## 🚀 Funcionalidades

### ✅ Requisitos Obrigatórios
- [x] Leitura de arquivos `.txt` e conversão para PNG
- [x] Conversão RGB para escala de cinza (implementação manual)
- [x] Substituição de pixels brancos por cor customizada

### 🎁 Bônus Implementados
- [x] Interface interativa com Jupyter Widgets
- [x] Tratamento robusto para arquivos mal formatados
- [x] Visualização em tempo real das transformações

## 📦 Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/image-processor.git
cd image-processor
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

## 🛠️ Uso Básico

```python
from image_processor import read_and_save_image, rgb_to_grayscale, replace_white_pixels

# Processamento básico
image_data = read_and_save_image('input.txt', 'output.png')
gray_image = rgb_to_grayscale(image_data)
modified_image = replace_white_pixels(image_data, (255, 0, 0))  # Substitui por vermelho
```

## 🎛️ Modo Interativo

Execute no Jupyter Notebook:
```python
from image_processor import interactive_demo

interactive_demo()
```

![Interface Interativa](docs/interactive-demo.png)

## 🧩 Estrutura do Projeto

```
.
├── src/
│   ├── __init__.py
│   ├── image_processor.py  # Implementação principal
│   └── utils.py            # Funções auxiliares
├── tests/
│   └── test_processor.py   # Testes unitários
├── samples/
│   ├── image.txt           # Exemplo de entrada
│   └── output.png          # Exemplo de saída
├── requirements.txt
└── README.md
```

## 🔍 Tratamento de Arquivos

O processador aceita arquivos texto com:
- Formato irregular (número variável de colunas)
- Cabeçalhos não numéricos
- Dados faltantes (preenche automaticamente com zeros)

**Exemplo de arquivo válido:**
```
255 0 0 128 128 128
0 255 0 64 64 64  # Comentários são ignorados
0 0 255
```

## ⚙️ Personalização

Para arquivos com cabeçalhos complexos:
```python
from image_processor import load_with_header

# Pula as 2 primeiras linhas (cabeçalhos)
image_data = load_with_header('dados.txt', skip_lines=2) 
```

## 🤝 Contribuição

Contribuições são bem-vindas! Siga estes passos:
1. Faça um fork do projeto
2. Crie sua branch (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## 📄 Licença

Distribuído sob licença MIT. Veja `LICENSE` para mais informações.

## ✉️ Contato

Seu Nome - Lucas Augusto da Silva - lucasaugusto.simoes@gmail.com

Link do Projeto: https://github.com/Lucassilva1010/ProcessamentoDeImagensPhyton.git

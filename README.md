# Renomear PDFs com OCR e OC

Script Python para renomear arquivos PDF automaticamente usando a **primeira linha de texto** encontrada.  
O script também tenta identificar **números de OC (Ordem de Compra)** e inclui no nome do arquivo. Ideal para PDFs de chamados, notas fiscais ou documentos corporativos.

---

## Funcionalidades

- Renomeia PDFs usando a primeira linha de texto encontrada.  
- Inclui o número de OC no nome do arquivo, se identificado.  
- Trata PDFs com caracteres inválidos para Windows.  
- Evita colisões de nomes (_1, _2...).  
- Detecta PDFs sem OCR ou protegidos por senha.  

---

## Requisitos

- Python 3.10 ou superior  
- Biblioteca `PyPDF2`

Instalação da biblioteca:

```bash
pip install PyPDF2


## Como usar

Coloque todos os PDFs que deseja renomear em uma pasta (ex.: C:\Users\[USUÁRIO LOCAL]\Desktop\[PASTA ALTERAÇÃO]).

Ajuste o caminho da pasta no script:

CAMINHO_PASTA = r"C:\Users\[USUÁRIO LOCAL]\Desktop\[PASTA ALTERAÇÃO]"

**OBS: Retirar os "[]"


Execute o script:

python renomear_pdfs.py


O script exibirá no terminal quais arquivos foram renomeados e alertas sobre PDFs sem texto ou protegidos.

PDFs escaneados (sem texto)

Se algum PDF não tiver texto pesquisável:

Abra o PDF no Adobe Acrobat Pro.

Vá em Ferramentas → Digitalizar e OCR → Reconhecer Texto → Neste Arquivo.

Configure:

Idioma: Português (Brasil)

Páginas: Todas

Saída: Imagem pesquisável

Clique em Reconhecer Texto e salve o arquivo.

Rode novamente o script Python.

Para múltiplos arquivos: Ferramentas → Digitalizar e OCR → Em Vários Arquivos.

Extra: Números de OC

O script tenta identificar números de OC nos padrões:

OC 12345

O.C.: 12345

Ordem de Compra: 12345

Nº da OC: 12345

Se encontrado, o nome do arquivo será algo como:

OC_12345__Primeira_Linha_do_PDF.pdf



## Observações

PDFs abertos no Adobe ou visualizador não podem ser renomeados. Feche-os antes de rodar o script.

PDFs protegidos por senha serão ignorados.

Caracteres inválidos (<>:"/\|?*) são automaticamente removidos.

Se o nome do arquivo já existir, o script adiciona _1, _2 para evitar sobrescrever.

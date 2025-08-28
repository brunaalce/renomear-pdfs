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

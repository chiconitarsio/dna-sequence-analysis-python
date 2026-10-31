# 🧬 DNA Sequence Analysis

Analisador de sequências de DNA em arquivos **multi-FASTA**, escrito em Python com Biopython.
Lê todos os registros do arquivo e responde quatro perguntas sobre o conjunto de dados.

> 🇺🇸 Python tool that parses multi-FASTA files with Biopython and reports record counts,
> sequence lengths, the longest Open Reading Frame per reading frame and the most frequent repeats.

## O que ele calcula

| # | Análise | Função |
|---|---|---|
| 1 | Número total de registros no arquivo | `question1_record_count` |
| 2 | Sequências mais longa e mais curta (com tratamento de empates) | `question2_sequence_lengths` |
| 3 | Maior ORF (ATG → TAA/TAG/TGA) em cada um dos 3 quadros de leitura | `question3_orfs` |
| 4 | Subsequência repetida mais frequente de tamanho *n* | `question4_repeats` |

## Como usar

```bash
pip install biopython
```

Coloque o arquivo FASTA na mesma pasta, ajuste `fasta_file` no fim do script (padrão:
`dna.example.fasta`) e o tamanho da repetição em `repeat_length_to_check` (padrão: 12). Depois:

```bash
python dna_sequence_analyzer.py
```

## Stack

Python 3 · Biopython (`SeqIO`) · `collections.defaultdict`

---
Desenvolvido por [Társio Chiconi](https://github.com/chiconitarsio) · Licença MIT

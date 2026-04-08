# 📊 Algoritmos de Ordenação — Análise Comparativa em Java

Projeto acadêmico desenvolvido em Java com o objetivo de implementar, testar e comparar o desempenho de diversos algoritmos de ordenação aplicados tanto em **arquivos de acesso randômico** (`RandomAccessFile`) quanto em **listas duplamente encadeadas**.

## 📁 Estrutura do Projeto

| Arquivo | Responsabilidade |
|---|---|
| `Arquivo.java` | Classe principal de manipulação de arquivos binários e implementação dos algoritmos de ordenação sobre arquivo |
| `Lista.java` | Implementação dos algoritmos de ordenação sobre lista duplamente encadeada |
| `noLista.java` | Nó da lista duplamente encadeada (campos: `info`, `ant`, `prox`) |
| `Registro.java` | Modelo do registro gravado em arquivo (número inteiro + padding de 2044 bytes) |
| `Principal.java` | Classe orquestradora que executa todos os algoritmos e gera a tabela comparativa em `tabela.txt` |
| `Exercicios.java` | Exercícios complementares de implementação de algoritmos sobre lista |

---

## 🗃️ Estruturas Utilizadas

### Arquivo Binário (`RandomAccessFile`)
Os registros são armazenados em arquivo binário com tamanho fixo (~2048 bytes cada), permitindo acesso posicional direto (`seek`). Três cenários de entrada são gerados automaticamente:
- **Ordenado** — sequência crescente
- **Reverso** — sequência decrescente
- **Randômico** — valores aleatórios (0–1023)

### Lista Duplamente Encadeada
Estrutura dinâmica com navegação bidirecional, implementada com a classe `noLista` (campos `ant` e `prox`).

---

## 🔢 Algoritmos Implementados

### Sobre Arquivo
| Algoritmo | Classe |
|---|---|
| Insertion Sort (Inserção Direta) | `Arquivo` |
| Inserção Binária | `Arquivo` |
| Selection Sort (Seleção Direta) | `Arquivo` |
| Bubble Sort (Bolha) | `Arquivo` |
| Shake Sort (Bolha Bidirecional) | `Arquivo` |
| Shell Sort | `Arquivo` |
| Heap Sort | `Arquivo` |
| Quick Sort com Pivô | `Arquivo` |
| Quick Sort sem Pivô | `Arquivo` |
| Gnome Sort | `Arquivo` |
| Comb Sort | `Arquivo` |
| Bucket Sort | `Arquivo` |
| Counting Sort | `Arquivo` |
| Radix Sort | `Arquivo` |
| Tim Sort | `Arquivo` |

### Sobre Lista Duplamente Encadeada
| Algoritmo | Classe |
|---|---|
| Insertion Sort | `Lista` |
| Inserção Binária | `Lista` |
| Selection Sort | `Lista` |
| Bubble Sort | `Lista` |
| Shake Sort | `Lista` |
| Shell Sort | `Lista` |
| Heap Sort | `Lista` |
| Quick Sort com Pivô | `Lista` |
| Quick Sort sem Pivô | `Lista` |
| Gnome Sort | `Lista` |
| Comb Sort | `Lista` |
| Bucket Sort | `Lista` |
| Counting Sort | `Lista` |
| Radix Sort | `Lista` |
| Merge Sort (duas versões) | `Lista` |
| Tim Sort | `Lista` |

---

## 📈 Análise de Desempenho

A classe `Principal` executa automaticamente cada algoritmo nas três configurações de entrada (ordenado, reverso e randômico) com **1024 registros** e registra os resultados em `src/tabela.txt`. Para cada método, são coletados:

- **Comparações realizadas** pelo programa (`Prog*`)
- **Comparações esperadas** pela equação teórica (`equa#`)
- **Movimentações realizadas** pelo programa (`Prog*`)


## ▶️ Como Executar

**Pré-requisitos:** Java 17+ e Maven (ou sua IDE favorita, ex: IntelliJ IDEA / Eclipse).

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git

# Compile e execute
cd seu-repositorio
javac -d out src/com/example/Entity/*.java
java -cp out com.example.Entity.Principal
```

Após a execução, o arquivo `src/tabela.txt` será criado com a tabela comparativa completa.

---

## 🛠️ Tecnologias

- **Java 17+**
- `java.io.RandomAccessFile` — manipulação de arquivos binários de acesso randômico
- `java.nio.file` — operações de sistema de arquivos
- Estruturas de dados customizadas (lista duplamente encadeada)

---

## 📚 Contexto Acadêmico

Projeto desenvolvido para a disciplina de **Estruturas de Dados / Algoritmos de Ordenação** do curso de Ciência da Computação. O objetivo é validar empiricamente a complexidade teórica dos algoritmos e comparar sua eficiência em diferentes estruturas de armazenamento (arquivo vs. lista encadeada).- **Movimentações esperadas** pela equação teórica (`equa#`)
- **Tempo de execução** (em segundos)

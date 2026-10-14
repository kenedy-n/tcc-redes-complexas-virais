# 🧬 Redes Complexas de Proteínas Virais Via Mecanismos de Atenção

Repositório oficial do Trabalho de Conclusão de Curso (TCC) do Bacharelado em Sistemas de Informação da Universidade Federal de Uberlândia (UFU).

* **Aluna:** Natália Kenedy Custódio Santos
* **Orientador:** Prof. Dr. Gilberto Nakamura
* **Área de Concentração:** Sistemas de Informação / Biologia Computacional

---

## 🎯 Sobre o Projeto
A compreensão das propriedades estruturais de proteínas virais é fundamental para antecipar mutações de escape e auxiliar no desenvolvimento de vacinas. Este projeto propõe uma metodologia inovadora para converter **matrizes de autoatenção** (extraídas de modelos de linguagem de proteínas baseados em *Transformers*, como o ESM-IF1) em **redes complexas ponderadas**, permitindo identificar regiões de alta plasticidade mutacional e vulnerabilidade em capsídeos virais (com foco inicial no vírus Influenza A)

---

## 📅 Cronograma e Entregas Semanais

O projeto está dividido em micro-metas semanais para garantir constância, foco e rastreabilidade do progresso:

### ✅ Semana 1: Estruturação do Ambiente e Ingestão de Dados
* [x] Criação da estrutura do repositório no GitHub.
* [x] Configuração do ambiente de desenvolvimento (Google Colab com suporte a GPU).
* [x] Implementação do script inicial de conexão com a API do RCSB PDB.
* [x] Baixar e processar estruturas 3D de proteínas do vírus Influenza A (ex: arquivo mmCIF/PDB) utilizando Biopython.
* **Entregável:** Script funcional de extração de sequências de aminoácidos a partir de códigos PDB reais.

### ⏳ Semana 2: Extração de Embeddings
* [ ] Configuração e carregamento do modelo pré-treinado ESM-IF1 via PyTorch.
* [ ] Extração de vetores de representação latente e matrizes de atenção das sequências virais.
* [ ] Salvamento estruturado dos tensores de atenção em disco.

### ⏳ Semana 3: Construção da Rede Complexa (Grafos)
* [ ] Mapeamento dos resíduos de aminoácidos como nós de um grafo.
* [ ] Conversão dinâmica dos pesos de autoatenção em arestas ponderadas utilizando NetworkX.
* [ ] Cálculo inicial de métricas topológicas de centralidade (Grau e Intermediação).

### ⏳ Semana 4: Validação e Organização do Pipeline
* [ ] Modularização completa do código em um pipeline automatizado (*Entrada PDB -> Embeddings -> Rede -> Métricas*).
* [ ] Documentação final do código-fonte para acesso aberto.

---

## 🚀 Como Executar o Projeto

Atualmente, os códigos experimentais rodam diretamente no **Google Colab** para aproveitar o suporte a GPU de forma gratuita. 

1. Acesse o Google Colab: [colab.research.google.com](https://colab.research.google.com)
2. Importe o notebook deste repositório via aba **GitHub**.
3. Instale as dependências essenciais executando o comando:
   ```bash
   pip install biopython requests networkx matplotlib torch

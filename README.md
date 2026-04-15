# 📄 Template TCC — Projeto de Pesquisa (PS I)
**Faculdade UNINTA · Bacharelado em Sistemas de Informação · 2026.1**

---

## 🚀 Como usar este template no Overleaf

### Passo 1 — Copiar o projeto
1. Acesse **overleaf.com** e crie uma conta gratuita (use seu e-mail)
2. O professor vai compartilhar o link deste template
3. Clique em **"Copy Project"** para criar sua cópia pessoal
4. Renomeie o projeto com seu nome: `TCC_SeuNome_2026`

---

### Passo 2 — Preencher seus dados (comece aqui!)
Abra o arquivo **`dados.tex`** e preencha:
- Seu nome completo
- Nome do orientador (com título correto: Prof. Dr. / Prof. Me.)
- Título do seu trabalho
- Palavras-chave

> ⚠️ **Não mexa nos outros arquivos ainda.** Comece sempre pelo `dados.tex`.

---

### Passo 3 — Escrever cada seção
Abra os arquivos na pasta `/secoes/` e escreva nos espaços indicados:

| Arquivo | O que escrever |
|---|---|
| `1-introducao.tex` | Contextualização, problema, objetivos, justificativa |
| `2-referencial-teorico.tex` | Fundamentação teórica e trabalhos relacionados |
| `3-metodologia.tex` | Como você vai conduzir a pesquisa |
| `4-cronograma.tex` | Planejamento de PS I até a defesa |

> 💡 Cada arquivo tem comentários explicando o que escrever em cada parte.
> Leia os comentários (linhas com `%`) — eles são o seu guia!

---

### Passo 4 — Adicionar referências com Zotero
1. Instale o [Zotero](https://zotero.org) + plugin **Better BibTeX**
2. Salve seus artigos no Zotero
3. Exporte a coleção: `Arquivo > Exportar > Better BibTeX`
4. Cole o conteúdo exportado no arquivo **`referencias.bib`**
5. Para citar no texto use `\cite{chave}` ou `\textcite{chave}`

---

### Passo 5 — Gerar o PDF
- Clique em **"Recompile"** (ou `Ctrl+Enter`) no Overleaf
- O PDF aparece no painel da direita
- Se der erro, veja a aba **"Logs"** — geralmente é um `\cite{}` com chave errada

---

## 📁 Estrutura do projeto

```
template_tcc/
│
├── main.tex                    ← Arquivo principal (não edite)
├── dados.tex                   ← ✏️ PREENCHA AQUI seus dados
├── referencias.bib             ← ✏️ Cole suas referências aqui
│
├── pretextual/
│   ├── capa.tex                ← Gerada automaticamente
│   ├── folha-rosto.tex         ← Gerada automaticamente
│   ├── folha-aprovacao.tex     ← Preencha após a defesa
│   ├── resumo.tex              ← ✏️ Escreva seu resumo
│   └── abstract.tex            ← ✏️ Traduza para o inglês
│
└── secoes/
    ├── 1-introducao.tex        ← ✏️ Contextualização e objetivos
    ├── 2-referencial-teorico.tex ← ✏️ Fundamentação teórica
    ├── 3-metodologia.tex       ← ✏️ Como você vai pesquisar
    └── 4-cronograma.tex        ← ✏️ Planejamento PS I → PS II
```

---

## ✍️ Comandos LaTeX essenciais

| O que fazer | Comando | Resultado |
|---|---|---|
| Citação indireta | `\cite{chave}` | (AUTOR, ano) |
| Citação no texto | `\textcite{chave}` | Autor (ano) |
| Citação com página | `\cite[p.~15]{chave}` | (AUTOR, ano, p. 15) |
| Negrito | `\textbf{texto}` | **texto** |
| Itálico | `\textit{texto}` | *texto* |
| Nova seção | `\section{Título}` | 1.1 Título |
| Nova subseção | `\subsection{Título}` | 1.1.1 Título |
| Lista numerada | `\begin{enumerate}...\end{enumerate}` | 1. 2. 3. |
| Lista com bullets | `\begin{itemize}...\end{itemize}` | • • • |
| Item de lista | `\item Texto do item` | item |
| Figura | veja seção abaixo | — |
| Tabela | veja seção abaixo | — |

---

## 🖼️ Como inserir uma figura

```latex
\begin{figure}[htb]
  \centering
  \caption{Legenda da figura (ACIMA da imagem — ABNT)}
  \label{fig:minha-figura}
  \includegraphics[width=0.8\textwidth]{nome-do-arquivo.png}
  \fonte{Autor (2026).}   % ou: Adaptado de Silva (2022).
\end{figure}
```

> 💡 Faça upload da imagem no Overleaf (botão de upload) e use o nome do arquivo.
> Para referenciar no texto: `conforme a Figura~\ref{fig:minha-figura}`

---

## 📊 Como inserir uma tabela simples

```latex
\begin{table}[htb]
  \caption{Legenda da tabela (ACIMA da tabela — ABNT)}
  \label{tab:minha-tabela}
  \begin{tabularx}{\textwidth}{lXr}
    \toprule
    \textbf{Coluna 1} & \textbf{Coluna 2} & \textbf{Coluna 3} \\
    \midrule
    Dado 1  & Descrição do dado 1  & 100 \\
    Dado 2  & Descrição do dado 2  & 200 \\
    \bottomrule
  \end{tabularx}
  \fonte{Elaborado pelo autor (2026).}
\end{table}
```

---

## 💻 Como inserir código-fonte

```latex
\begin{lstlisting}[language=Python, caption={Exemplo de código Python}]
def calcular_media(lista):
    """Calcula a média de uma lista de números"""
    return sum(lista) / len(lista)

numeros = [8, 7, 9, 6, 10]
print(f"Média: {calcular_media(numeros)}")
\end{lstlisting}
```

Linguagens disponíveis: `Python`, `Java`, `JavaScript`, `SQL`, `C`, `C++`, `PHP`, `HTML`, `CSS`, `Bash`

---

## ❓ Dúvidas frequentes

**P: O Overleaf deu erro, o que faço?**
R: Clique em "Logs" (aba vermelha) e leia a primeira linha de erro. O erro mais comum é uma chave de citação inexistente — verifique se a chave no `\cite{}` existe no `referencias.bib`.

**P: Como compartilho o projeto com o orientador?**
R: No Overleaf, clique em "Share" → "Turn on link sharing" → copie e envie o link.

**P: Posso usar o template offline?**
R: Sim, você pode baixar e usar com uma instalação local do LaTeX (TeX Live ou MiKTeX + VS Code com extensão LaTeX Workshop).

**P: Como vejo o número de palavras?**
R: No Overleaf: menu esquerdo → "Word Count" (pode demorar alguns segundos).

---

## 📞 Suporte

- **Material da disciplina:** Link do GitHub (disponibilizado em aula)
- **Tutorial Zotero + BibTeX:** Disponível no repositório da disciplina
- **Dúvidas:** trazer para as aulas de quarta-feira ou sábados letivos

---

*Faculdade UNINTA · Bacharelado em Sistemas de Informação · 2026.1*

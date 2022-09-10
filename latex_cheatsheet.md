# How to?

..and some suggestions.

### Add a list

Useful when listing things.
You can do unnumbered lists, numbered lists and lists in lists.
Use the last ones sparingly.

```
\begin{itemize}
	\item Data requirements;
	\item Data collection;
	\item Data processing.
\end{itemize}

\begin{enumerate}
	\item Data requirements;
	\item Data collection;
	\item Data processing.
\end{enumerate}

\begin{enumerate}
	\item Data requirements;
	\begin{itemize}
    	\item Data;
    	\item Data.
    \end{itemize}
	\item Data collection;
	\item Data processing.
\end{enumerate}

```

### Add an image

Useful for getting to that minimal amount of pages.
Use parameters such as `width` and others to control figure dimensions.
Refer to figure by using `\autoref{fig:utmlogo}`.

```
\begin{figure}[H]
    \centering
    \includegraphics[width=14cm]{"Chapter1/Logo"}
    \caption{UTM Logo \cite{ref:zoo}}
    \label{fig:utmlogo}
\end{figure}

```

### Add an equation

Useful if math.
Refer to figure by using `\autoref{eq:energymass}`.

```
\begin{equation}
    E = m \cdot c^2
    \label{eq:energymass}
\end{equation}

```

### Add a table

In Latex, tables can be a bit hard to master.
There are many ways to make a table.
Just make sure it's easily readable (otherwise why are you using a table?) and consistent with other tables.

```
\begin{table}[h]
    \centering
    \caption{Training epochs of the unfrozen model.}
    \begin{tabular}{p{.2\columnwidth}p{.2\columnwidth}p{.2\columnwidth}p{.2\columnwidth}}
        \toprule
        epoch & train\_loss & valid\_loss & error\_rate \\
        \midrule
        1 & 0.097319 & 0.155017 & 0.048038 \\
        2 & 0.074885 & 0.144853 & 0.044655 \\
        3 & 0.063509 & 0.144917 & 0.043978 \\
        \bottomrule
    \end{tabular}
    \label{tbl:epochs}
\end{table}

```

### Add a code listing

The only way of listing code (seriously, no code print screens).
You can even color code if you specify the right programming language as a parameter.

```
\begin{lstlisting}[label=lst:nparray, language=Python, caption=Problem Conditions in Python]
# Cost array
cost = np.array([
	[4, 1, 3],
	[2, 0, 5],
	[3, 2, 2]
])
\end{lstlisting}

```

### Attach a pdf file

Useful for attaching "Declaratii" and "Avizuri".
Put them in the `PDF` folder.

```
\includepdf[pages={1,2}]{PDF/Titlul}
\includepdf[]{PDF/Declar}
\includepdf[]{PDF/Aviz}

```

### Add a reference

Useful when writing a thesis.
Add an entry in the `Additional/References.tex` file.
Refer to reference by using `\cite{ref:Zoo}`.
Choose a style of referencing and stick to it.

```
\bibitem{ref:Zoo}
    Zooniverse,
    \textit{What is the Zooniverse}, \url{https://www.zooniverse.org/about}
    (March 16, 2017)

```

### Define a custom variable

Useful if you are repeatedly using something.
Some important stuff is already defined.
Check the abstract for example use.

```
\newcommand{\thesistitlero}{Titlu generic}
\newcommand{\thesistitleeng}{Generic Title}
\newcommand{\studentname}{Nume Prenume}
\newcommand{\teachername}{Nume Prenume}
\newcommand{\teachertitle}{X X}

```

### Add bold, italics..

Use sparingly.

```
\textbf{Just}
\textit{Just}
\texttt{Just}
\textsc{Just}

```

### Suggestions

- Keep your filenames, reference labels, figure names etc. tidy and organised. You'll spend less time searching and more time writing the thesis;
- The more you leave Latex format for you, the better (format by hand sparingly);
- If possible, use constructs that exist in Latex, instead of formatting something by yourself;
- Headings you should use are: `\section{}`, `\subsection{}`, `\subsubsection{}`, `\paragraph{}`.

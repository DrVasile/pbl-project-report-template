# LaTeX Cheat-sheet


## If you want to:

### ...add an unordered list:

```
\begin{itemize}
	\item Data requirements;
	\item Data collection;
	\item Data processing.
\end{itemize}
```

### ...add an ordered list:
```
\begin{enumerate}
	\item Data requirements;
	\item Data collection;
	\item Data processing.
\end{enumerate}
```

Also, if needed, the lists can be nested.


## Add a code listing

The only way of listing code (seriously, no code print screens). You can even style the printed code by using specific parameters.

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


## Add an equation

Useful if math.
Refer to figure by using `\autoref{eq:energymass}`.

```
\begin{equation}
    E = m \cdot c^2
    \label{eq:energymass}
\end{equation}
```


## Add an image

There is a custom command for showing figures declared in the .cls file. Use the following syntax to include your figures.
```
\showfigure{scale}{path_to_the_image}{caption_text}{figure_label}
```


## Add a table

In Latex, tables can be a bit hard to master. There are many ways to make a table. Just make sure it's easily readable (otherwise why are you using a table?) and consistent with other tables. Also, sometimes it is convenient to use the online LaTeX table generator.

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


## Attach a pdf file

Useful for attaching "Declaratii" and "Avizuri".
Put them in the `PDF` folder.

```
\includepdf[pages={1,2}]{PDF/Titlul}
\includepdf[]{PDF/Declar}
\includepdf[]{PDF/Aviz}

```

## Add a reference

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

## Define a custom variable

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

## Add bold, italics..

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

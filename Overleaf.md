# Overleaf
> credit to Yiwen Huang @ University of Sydney

## Preparation

```latex
\documentclass[fleqn,12pt]{olplainarticle}
% Use option lineno for line numbers, font size 12pt 
\usepackage{textcomp} % for latex
\usepackage{gensymb} % Provides generic commands \degree, \celsius, \perthousand, \micro and \ohm which work both in text and maths mode.
\usepackage{amsmath} % Math typing
\usepackage[utf8]{inputenc} %
\usepackage{subcaption} %when writing captions for subfigures and the like.
\usepackage{lscape} % Modifies the margins and rotates the page contents but not the page number. Useful, for example, with large multipage tables, as it is compatible with longtable and supertabular.
\usepackage{chngcntr} % Defines commands \counterwithin (which sets up a counter to be reset when another is incremented) and \counterwithout (which unsets such a relationship).
\counterwithin{figure}{subsection}
\counterwithin{table}{subsection}
\pagestyle{plain}

\usepackage{graphicx} %Loading the package
\graphicspath{{Figures/}} %Setting the graphicspath


\linespread{1.5} %define the spacing as 1.5

\linespread{1.5} %define the spacing as 1.5

\title{TITLE\\
\large title
}
\author{AUTHOR \space \space NAME \space \space Supervisor: NAME}

\begin{document}

%\flushbottom
\maketitle


```

------

CONTENTS GO HERE

```latex
\clearpage %%%%%%%%%%% Page break


\bibliographystyle{apalike} %% Dont forget references
\bibliography{ref-zotero}

\end{document}
```



## Make section such as 1. Introduction

``` latex
\section{Introduction}
```

### Subsections

```latex
\subsection{}
\subsubsection{}
```

## Figures

### Single figure

```Latex
\begin{figure}[ht] %% Here I dont know Ask Even
\centering %% Centre ?
\includegraphics[width=0.8 \textwidth]{D_REV.png} %% Insert image
\caption{REV conceptual explanation \citep{helmig_multiphase_1997}} %% What to display
\label{fig:intermodal} %% I dont know Ask Even
\end{figure} 
```

### Multiple figures

``` latex
\begin{figure}[h] %% Ask Even h
\begin{subfigure}{0.5\textwidth} %% Start sub figure
\includegraphics[width=0.95\linewidth, height=6cm]{DL.png} 
\caption{Fluid pressure and streamlines}
\label{fig:subim1}
\end{subfigure}
\begin{subfigure}{0.5\textwidth}
\includegraphics[width=0.95\linewidth, height=6cm]{T.png}
\caption{ Temperature profile}
\label{fig:subim2}
\end{subfigure}
\caption{ Preliminary results from COMSOL simulation}
\label{fig:image2}
\end{figure}
```

![Xnip2021-07-05_15-48-04](https://tva1.sinaimg.cn/large/008i3skNgy1gs60yi50k1j31w00r6q9a.jpg)

## Equations

```Latex
\begin{equation}
   \mbox{Mass conservation: \qquad }  \frac{\partial(\phi \rho)}{\partial t}+\nabla*( \rho v) = q  
\end{equation}
```

Where `\mbox` is no Italics, `\qquad` is spaces, `frac{numerater}{denominator}` ,![Xnip2021-07-05_15-50-04](https://tva1.sinaimg.cn/large/008i3skNgy1gs610g2cesj31qm05i0ta.jpg)

## Tables

```latex
\begin{table}[h!] %% Ask Even about h!
\begin{center} % Centre
\setlength{\arrayrulewidth}{0.4mm} %% No idea Ask Even
 \begin{tabular}{ p{6cm} p{4cm} p{3cm}  }%% Set how many cols, width cols
\hline %Line at Top
Parameters  & Value & Unit\\ %% First row
\hline %% Second Line
Fracture Permeability & $1.0*10^{-11}$ & $m^2$ \\ %% Second row
Porosity & 0.2 \\
Poisson ratio & 0.4 \\
Heat conductivity & 0.836 & $W/m/K$\\
Heat capacity & 167.2 & $J/kg/K$\\
Density of soil & 2000 & $kg/{m^3}$\\
 \hline %% Line at bot
\end{tabular}
\caption{Habanero site rock properties, \citep{sun_numerical_2017}} % what to dsiplay
\label{table:1} %% Ask Even
\end{center} % Finish centre
\end{table}
```

![Xnip2021-07-05_15-49-08](https://tva1.sinaimg.cn/large/008i3skNgy1gs60zmdownj31k60pugpq.jpg)

# 欢迎Welcome

您好，这里是我的笔记网站。能够帮到您是我的荣幸，若您有任何bug、建议或错误需要汇报，请您与我联系。



### 这是一个 LaTeX/TikZ 绘图示例
```kroki-tikz
\begin{document}
\begin{tikzpicture}
  \draw[->, thick, blue] (0,0) -- (2,2) node[above right] {Vector v};
  \draw[red, fill=red!20] (2,0) circle (0.5) node[black] {Node};
\end{tikzpicture}
\end{document}
```

### 这是一个架构图示例
```kroki-plantuml
@startuml
Alice -> Bob: Authentication Request
Bob --> Alice: Authentication Response
@enduml
```


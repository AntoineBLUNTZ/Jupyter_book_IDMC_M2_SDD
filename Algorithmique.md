---
title: Algorithmique ⚙️
date: 2024-06-12
authors:
  - name: Antoine TABBONE
    email: antoine.tabbone@univ-lorraine.fr
    affiliations:
      - name: Université de Lorraine
        ror: 04vfs2w97
---


# Introduction à l'Algorithmique

[![Made with MyST](https://img.shields.io/badge/made%20with-myst-orange)](https://myst.tools)

:::{prf:algorithm} Ford–Fulkerson
:label: my-algorithm

**Inputs** Given a Network $G=(V,E)$ with flow capacity $c$, a source node $s$, and a sink node $t$

**Output** Compute a flow $f$ from $s$ to $t$ of maximum value

1. $f(u, v) \leftarrow 0$ for all edges $(u,v)$
2. While there is a path $p$ from $s$ to $t$ in $G_{f}$ such that $c_{f}(u,v)>0$ for all edges $(u,v) \in p$:

	1. Find $c_{f}(p)= \min \{c_{f}(u,v):(u,v)\in p\}$
	2. For each edge $(u,v) \in p$

		1. $f(u,v) \leftarrow f(u,v) + c_{f}(p)$ *(Send flow along the path)*
		2. $f(u,v) \leftarrow f(u,v) - c_{f}(p)$ *(The flow might be "returned" later)*
:::

This repository contains the files used in the [quickstart guide](https://mystmd.org/guide/quickstart), and can be used to follow that guide, before trying MyST with your own content.

> **Note** This is **not** a good example of an actual MyST project! The repositories purpose is to be a simple markdown + notebook repository that can be transformed throughout a tutorial.

The goals of the [quickstart guide](https://myst.tools/docs/mystjs/quickstart) are:

1. Create a `myst` site, using the standard template
2. Improve the frontmatter, to add authors, affiliations and other metadata
3. Export the paper as a PDF, Word document, and LaTeX files
4. Integrate a Jupyter Notebook output into our paper, to improve reproducibility
5. Publish a website of with our work 🚀

## Improving Frontmatter and MyST Site

![](./images/frontmatter-after.png)

## Export as a PDF

![](./images/export-pdf.png)

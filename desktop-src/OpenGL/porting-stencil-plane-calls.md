---
title: Porting di chiamate del piano stencil
description: In OpenGL è possibile allocare i piani dello stencil richiedendo il formato pixel appropriato con OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Porting di IRIS GL, piani stencil
- porting da IRIS GL, piani stencil
- porting in OpenGL da IRIS GL, piani stencil
- Porting OpenGL da IRIS GL, piani stencil
- piani stencil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330999"
---
# <a name="porting-stencil-plane-calls"></a>Porting di chiamate del piano stencil

In OpenGL è possibile allocare i piani dello stencil richiedendo il formato pixel appropriato con OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat). funzioni. La tabella seguente elenca le funzioni di IRIS GL che interessano i piani degli stencil e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL             | OpenGL (funzione)                                         | Significato                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **stencil**( **true**,...) | [**glEnable**](glenable.md) ( \_ test di stencil GL \_ )      | Abilita i test di stencil.                                 |
| **stencil**                  | [**glStencilOp**](glstencilop.md)                      | Imposta le azioni di test dello stencil.                             |
| **stencil**(... Func,...)  | [**glStencilFunc**](glstencilfunc.md)                  | Imposta la funzione e il valore di riferimento per il test di stencil. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Specifica quali bit di stencil è possibile scrivere.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Specifica il valore Clear per il buffer dello stencil.      |
| **sclear**                   | [**glClear**](glclear.md) ( \_ bit del buffer dello stencil GL \_ \_ ) |                                                        |



 

Le funzioni di confronto stencil e le operazioni di passaggio/errore stencil sono quasi equivalenti in OpenGL e IRIS GL. I flag di funzione dello stencil GL di IRIS sono preceduti da SF; flag OpenGL con GL. I flag di operazione di superamento/errore di IRIS GL sono preceduti da ST; flag OpenGL con GL.

 

 





---
title: Porting di viewport, Screenmasks e Scrboxes
description: Le funzioni viewport GL seguenti non hanno un equivalente OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Porting di IRIS GL, funzioni viewport
- porting da IRIS GL, funzioni viewport
- porting in OpenGL da IRIS GL, funzioni viewport
- Porting OpenGL da IRIS GL, funzioni viewport
- funzioni viewport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297985"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Porting di viewport, Screenmasks e Scrboxes

Le funzioni viewport GL seguenti non hanno un equivalente OpenGL:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Con la funzione del **viewport** di Iris GL, è necessario specificare le coordinate x (in pixel) per la sinistra e la destra di un rettangolo del viewport e le coordinate y per la parte superiore e inferiore. Con la funzione OpenGL [**glViewport**](glviewport.md) , tuttavia, si specificano le coordinate x e y (in pixel) dell'angolo inferiore sinistro del rettangolo del viewport insieme alla relativa larghezza e altezza.

La tabella seguente elenca le funzioni viewport GL di IRIS e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                          | OpenGL (funzione)                                                                                         | Significato                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **viewport** (a sinistra, a destra, in basso, in alto) | [**glViewport**](glviewport.md) (x, y, larghezza, altezza)                                                | Imposta il viewport.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) (bit del viewport per GL \_ \_ )<br/> | Inserisce e estrae lo stack.   |
| **getViewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ riquadro di visualizzazione GL)               | Restituisce le dimensioni del viewport. |



 

??

 

 






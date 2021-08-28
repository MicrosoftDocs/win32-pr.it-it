---
title: Porting viewports, Screenmasks e Scrboxes
description: Le funzioni del viewport IRIS GL seguenti non hanno un equivalente OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Porting IRIS GL, funzioni del viewport
- porting da IRIS GL, funzioni viewport
- porting in OpenGL da IRIS GL, funzioni del viewport
- Porting OpenGL da IRIS GL, funzioni del viewport
- funzioni viewport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb1a01cfb038faf87e48381856fe281bf2c935d13fedb78b79266e2af4fe15e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776911"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Porting viewports, Screenmasks e Scrboxes

Le funzioni del viewport IRIS GL seguenti non hanno un equivalente OpenGL:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Con la funzione del **viewport** IRIS GL si specificano le coordinate x (in pixel) per la parte sinistra e destra di un rettangolo del viewport e le coordinate y per la parte superiore e inferiore. Con la funzione OpenGL [**glViewport,**](glviewport.md) tuttavia, si specificano le coordinate x e y (in pixel) dell'angolo inferiore sinistro del rettangolo del viewport insieme alla larghezza e all'altezza.

Nella tabella seguente sono elencate le funzioni del viewport IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                          | Funzione OpenGL                                                                                         | Significato                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **viewport** ( left, right, bottom, top ) | [**glViewport**](glviewport.md) ( x, y, width, height )                                                | Imposta il viewport.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL \_ VIEWPORT BIT \_ )<br/> | Inserisce e popola lo stack.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ VIEWPORT )               | Restituisce le dimensioni del viewport. |



 

??

 

 






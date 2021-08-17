---
title: Uso delle funzioni di anti-aliasing
description: La tabella seguente elenca le funzioni di anti-aliasing IRIS GL e le funzioni OpenGL equivalenti.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Portabilità, antialiasing IRIS GL
- porting da IRIS GL, antialiasing
- porting to OpenGL from IRIS GL,antialiasing
- Portabilità OpenGL da IRIS GL, antialiasing
- anti-aliasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab36f41e3b639447b4f246d706e11c134d8f920528cde1e946d26af057a95951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980347"
---
# <a name="using-antialiasing-functions"></a>Uso delle funzioni di anti-aliasing

La tabella seguente elenca le funzioni di anti-aliasing IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS | Funzione OpenGL                                      | Significato                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )   | Abilita l'anti-aliasing dei punti.   |
| **linesmooth**   | **glEnable**( GL \_ LINE \_ SMOOTH )                     | Abilita l'antialiasing delle righe.    |
| **polysmooth**   | [**glEnable**](glenable.md) ( GL \_ POLYGON \_ SMOOTH ) | Abilita l'antialiasing dei poligoni. |



 

Usare le chiamate [**glDisable**](gldisable.md) equivalenti per disattivare l'anti-aliasing.

In IRIS GL è possibile controllare la qualità dell'antialiasing chiamando:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL offre un controllo simileuse [**glHint:**](glhint.md)


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



dove *hintMode* è uno dei seguenti:

-   GL \_ NICEST (usare la smussamento della massima qualità).
-   GL \_ FASTEST (usare la smussamento più efficiente).
-   GL \_ DONT \_ CARE

IRIS GL consente anche la correzione finale chiamando:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL non ha equivalenti per questa funzione.

 

 





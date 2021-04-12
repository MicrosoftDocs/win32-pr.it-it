---
title: Uso di funzioni di anti-aliasing
description: La tabella seguente elenca le funzioni di anti-aliasing di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Porting di IRIS GL, anti-aliasing
- porting da IRIS GL, anti-aliasing
- porting in OpenGL da IRIS GL, anti-aliasing
- Porting OpenGL da IRIS GL, anti-aliasing
- anti-aliasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221233"
---
# <a name="using-antialiasing-functions"></a>Uso di funzioni di anti-aliasing

La tabella seguente elenca le funzioni di anti-aliasing di IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                                      | Significato                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( \_ punto GL \_ smussato)   | Abilita l'anti-aliasing dei punti.   |
| **linesmooth**   | **glEnable**( \_ linea GL \_ smussata)                     | Abilita l'anti-aliasing delle righe.    |
| **con uniformità**   | [**glEnable**](glenable.md) ( \_ arrotondamento del poligono GL \_ ) | Abilita l'anti-aliasing dei poligoni. |



 

Usare le chiamate [**glDisable**](gldisable.md) equivalenti per disattivare l'anti-aliasing.

In IRIS GL è possibile controllare la qualità dell'anti-aliasing chiamando:


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL fornisce un [**glHint**](glhint.md)controluse simile:


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



dove *hintMode* è uno dei seguenti:

-   GL \_ più gradevole (usare la migliore smussatura della qualità).
-   GL \_ più veloce (usare la smussatura più efficiente).
-   GL \_ dont \_ care

IRIS GL consente anche la correzione finale chiamando:


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL non ha un equivalente per questa funzione.

 

 





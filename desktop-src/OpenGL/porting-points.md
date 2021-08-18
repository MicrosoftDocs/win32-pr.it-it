---
title: Punti di portabilità
description: OpenGL non ha alcun comando per disegnare un singolo punto. In caso contrario, le funzioni del punto di portabilità sono semplici. La tabella seguente elenca le funzioni IRIS GL per il disegno dei punti e le funzioni OpenGL equivalenti.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Portabilità IRIS GL, punti
- porting from IRIS GL,points
- porting to OpenGL from IRIS GL,points
- Portabilità OpenGL da IRIS GL, punti
- funzioni di disegno, punti
- punti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ef24ad81942681b3d70a303a22e89e9573aa609d3f08f52a92583ae88e0e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012069"
---
# <a name="porting-points"></a>Punti di portabilità

OpenGL non ha alcun comando per disegnare un singolo punto. In caso contrario, le funzioni del punto di portabilità sono semplici. La tabella seguente elenca le funzioni IRIS GL per il disegno dei punti e le funzioni OpenGL equivalenti.



| Funzione GL IRIS           | Funzione OpenGL                                                   | Significato                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pnt**                    |                                                                   | Disegna un singolo punto.                                                                                                                                |
| **bgnpoint**, **endpoint** | [**glBegin**](glbegin.md) ( GL \_ POINTS ), [ **glEnd**](glend.md) | Interpreta i vertici come punti.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Imposta le dimensioni in punti in pixel.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )                | Attiva l'anti-aliasing dei punti. Per altre informazioni sull'antialiasing dei punti, vedere [Porting Antialiasing Functions](porting-antialiasing-functions.md).) |



 

Per informazioni sulle funzioni get correlate, vedere [**glPointSize.**](glpointsize.md)

??

 

 





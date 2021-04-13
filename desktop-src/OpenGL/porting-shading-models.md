---
title: Porting di modelli di ombreggiatura
description: Analogamente a IRIS GL, OpenGL consente di passare da un'ombreggiatura Smooth (Gouraud) a un'ombreggiatura semplice e viceversa. La tabella seguente elenca le funzioni di ombreggiatura e dithering di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Porting di IRIS GL, ombreggiatura
- porting da IRIS GL, ombreggiatura
- porting in OpenGL da IRIS GL, ombreggiatura
- Porting OpenGL da IRIS GL, ombreggiatura
- ombreggiatura uniforme
- Ombreggiatura Gouraud
- ombreggiatura flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331004"
---
# <a name="porting-shading-models"></a>Porting di modelli di ombreggiatura

Analogamente a IRIS GL, OpenGL consente di passare da un'ombreggiatura Smooth (Gouraud) a un'ombreggiatura semplice e viceversa. La tabella seguente elenca le funzioni di ombreggiatura e dithering di IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                                   | OpenGL (funzione)                                                                                    | Significato                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(Flat)                               | [**glShadeModel**](glshademodel.md) (GL \_ Flat)                                                  | Esegue l'ombreggiatura piatta.           |
| **shademodel**(Gouraud)                            | **glShadeModel**(GL \_ Smooth)                                                                     | Esegue un'ombreggiatura uniforme.         |
| **Ottiene**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modello di ombreggiatura GL \_ )      | Restituisce il modello di ombreggiatura corrente. |
| **dithering (DT** \_ on) **dithering**(DT \_ disattivato) <br/> | [**glEnable**](glenable.md) ( \_ dithering GL)[**glDisable**](gldisable.md)( \_ dithering GL)<br/> | Attiva/disattiva la dithering.      |



 

??

 

 






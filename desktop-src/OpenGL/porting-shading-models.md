---
title: Porting Shading Models
description: Come IRIS GL, OpenGL consente di passare dall'ombreggiatura uniforme (Gouraud) all'ombreggiatura flat. Nella tabella seguente sono elencate le funzioni di ombreggiatura e dithering IRIS GL e le funzioni OpenGL equivalenti.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Porting IRIS GL, ombreggiatura
- porting da IRIS GL, ombreggiatura
- porting in OpenGL da IRIS GL, ombreggiatura
- Porting OpenGL da IRIS GL, ombreggiatura
- ombreggiatura uniforme
- Ombreggiatura gouraud
- ombreggiatura piatta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee4265341e17843dbe4752bb51e5728aa54914ec5670c08b6b7921537050a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012039"
---
# <a name="porting-shading-models"></a>Porting Shading Models

Come IRIS GL, OpenGL consente di passare dall'ombreggiatura uniforme (Gouraud) all'ombreggiatura flat. Nella tabella seguente sono elencate le funzioni di ombreggiatura e dithering IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                                   | Funzione OpenGL                                                                                    | Significato                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(FLAT)                               | [**glShadeModel**](glshademodel.md) ( GL \_ FLAT )                                                  | Esegue l'ombreggiatura flat.           |
| **shademodel**(GOURAUD)                            | **glShadeModel**( GL \_ SMOOTH )                                                                     | Esegue un'ombreggiatura uniforme.         |
| **getsm**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ SHADE \_ MODEL )      | Restituisce il modello di ombreggiatura corrente. |
| **dithering**(DT \_ ON) **dither**(DT \_ OFF) <br/> | [**glEnable**](glenable.md) ( GL \_ DITHER )[**glDisable**](gldisable.md)( GL \_ DITHER )<br/> | Attiva/disattiva il dithering.      |



 

??

 

 






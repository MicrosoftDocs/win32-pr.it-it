---
title: Porting delle funzioni di selezione
description: Tutte le funzioni di selezione IRIS GL hanno equivalenti OpenGL, ad eccezione di clearhitcode. Nella tabella seguente sono elencate le funzioni di selezione IRIS GL e le funzioni OpenGL equivalenti.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Porting IRIS GL, selezione
- porting da IRIS GL, selezione
- porting in OpenGL da IRIS GL, selezione
- Porting OpenGL da IRIS GL, selezione
- Raccolta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2cbeed54a18e7f1d3f26ec01dca2ad352aa4e190fbdc667ed75a60badec29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034811"
---
# <a name="porting-picking-functions"></a>Porting delle funzioni di selezione

Tutte le funzioni di selezione IRIS GL hanno equivalenti OpenGL, ad eccezione di **clearhitcode**. Nella tabella seguente sono elencate le funzioni di selezione IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                | Funzione OpenGL                                                                           | Significato                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Non supportata.                                                                            | Cancella la variabile globale e l'hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) ( GL \_ SELECT )                                       | Passa alla modalità di selezione o di selezione. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )                                       | Passa alla modalità di rendering.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Imposta la matrice restituita.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Per altre informazioni sulla selezione, vedere [**gluPickMatrix**](glupickmatrix.md).

 

 






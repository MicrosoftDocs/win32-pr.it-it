---
title: Funzioni di selezione del porting
description: Tutte le funzioni di selezione di IRIS GL hanno equivalenti OpenGL, ad eccezione di clearhitcode. La tabella seguente elenca le funzioni di selezione di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Porting di IRIS GL, selezione
- porting da IRIS GL, selezione
- porting in OpenGL da IRIS GL, selezione
- Porting OpenGL da IRIS GL, selezione
- selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298541"
---
# <a name="porting-picking-functions"></a>Funzioni di selezione del porting

Tutte le funzioni di selezione di IRIS GL hanno equivalenti OpenGL, ad eccezione di **clearhitcode**. La tabella seguente elenca le funzioni di selezione di IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                | OpenGL (funzione)                                                                           | Significato                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Non supportata.                                                                            | Cancella la variabile globale e hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) ( \_ selezione GL)                                       | Passa alla modalità selezione o selezione. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( \_ rendering GL)                                       | Passa alla modalità di rendering.            |
| **picksize**                    | [](glupickmatrix.md)[**glSelectBuffer** gluPickMatrix](glselectbuffer.md)<br/> | Imposta la matrice restituita.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [](glpushname.md)[**glPopName** glPushName](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Per ulteriori informazioni sulla selezione, vedere [**gluPickMatrix**](glupickmatrix.md).

 

 






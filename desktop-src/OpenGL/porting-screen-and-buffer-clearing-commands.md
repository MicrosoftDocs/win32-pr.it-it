---
title: Comandi di cancellazione dello schermo e del buffer
description: OpenGL sostituisce un'ampia gamma di funzioni non crittografate IRIS GL (ad esempio zclear, aclear, sclear e così via) con una singola funzione, glClear. Specificare esattamente ciò che si vuole cancellare passando le maschere a glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Porting IRIS GL, funzioni clear
- porting da IRIS GL, funzioni clear
- porting a OpenGL da IRIS GL, funzioni clear
- Porting OpenGL da IRIS GL, funzioni clear
- funzioni clear
- Porting IRIS GL, comandi di cancellazione dello schermo
- porting da IRIS GL, comandi di cancellazione dello schermo
- porting a OpenGL da IRIS GL, comandi di cancellazione dello schermo
- Porting OpenGL da IRIS GL, comandi di cancellazione dello schermo
- comandi di cancellazione dello schermo
- Porting IRIS GL, comandi di cancellazione del buffer
- porting da IRIS GL, comandi di cancellazione del buffer
- porting in OpenGL da IRIS GL, comandi di cancellazione del buffer
- Porting OpenGL da IRIS GL, comandi di cancellazione del buffer
- comandi di cancellazione del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbff0fed3472fd4374605cb96dbae845998c0ba2d8ce488420f9b4c6895a07c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794876"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Comandi di cancellazione dello schermo e del buffer

OpenGL sostituisce un'ampia gamma di funzioni non crittografate IRIS **GL** (ad esempio **zclear,** **aclear,** **sclear** e così via) con una singola funzione, [**glClear**](glclear.md). Specificare esattamente ciò che si vuole cancellare passando le maschere a **glClear**.

Quando si esegue il porting di comandi dello schermo e del buffer, tenere presente quanto segue:

-   OpenGL mantiene i colori di cancellazione separatamente dai colori di disegno, con chiamate come [**glClearColor**](glclearcolor.md) [**e glClearIndex**](glclearindex.md). Assicurarsi di impostare il colore non crittografato per ogni buffer prima della cancellazione.
-   Invece di usare una delle diverse chiamate clear denominate in modo diverso, è ora possibile cancellare diversi buffer con una sola chiamata, [**glClear**](glclear.md), tramite **l'ing** insieme di maschere di buffer. Ad esempio, **czclear** viene sostituito da:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL fa riferimento allo stipple del poligono e alla maschera di scrittura del colore. OpenGL ignora lo stipple del poligono, ma fa riferimento alla maschera di scrittura del colore. La **funzione czclear** ignora sia lo stipple poligonale che la maschera di scrittura del colore.

Nella tabella seguente sono elencate le varie funzioni non crittografate IRIS GL con le funzioni OpenGL equivalenti.



| Chiamata GL IRIS         | Chiamata OpenGL                                                               | Significato                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ CLEAR) | **glClear**( GL \_ ACCUM \_ BUFFER BIT \_ )                                     | Cancellare il buffer di accumulo.                    |
|                      | **glClearColor**                                                          | Impostare il colore non crittografato RGBA.                         |
|                      | **glClearIndex**                                                          | Impostare l'indice dei colori non crittografati.                        |
| **deselezionare**            | **glClear**( GL \_ COLOR BUFFER BIT \_ \_ )                                     | Cancellare il buffer dei colori.                           |
|                      | **glClearDepth**                                                          | Specificare il valore non crittografato per il buffer di profondità.     |
| **zclear**           | **glClear**( GL \_ DEPTH BUFFER BIT \_ \_ )                                     | Cancellare il buffer di profondità.                           |
| **czclear**          | **glClear**( GL \_ COLOR BUFFER BIT GL DEPTH BUFFER BIT \_ \_ \| \_ \_ \_ )<br/> | Cancellare il buffer dei colori e il buffer di profondità.      |
|                      | **glClearAccum**                                                          | Specificare valori non crittografati per il buffer di accumulo. |
|                      | **glClearStencil**                                                        | Specificare il valore non crittografato per il buffer di stencil.   |
| **sclear**           | **glClear**( GL \_ STENCIL BUFFER BIT \_ \_ )                                   | Cancellare il buffer dello stencil.                         |



 

Quando il codice gl IRIS usa **sia gclear** che **sclear,** è possibile combinarli in una singola **chiamata glClear.** può migliorare le prestazioni del programma.

 

 






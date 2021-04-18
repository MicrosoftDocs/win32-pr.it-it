---
title: Porting dei comandi di cancellazione dello schermo e del buffer
description: OpenGL sostituisce un'ampia gamma di funzioni Clear di IRIS GL, ad esempio zclear, aClear, sClear e così via, con una singola funzione, glClear. Specificare esattamente ciò che si vuole cancellare passando le maschere a glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Porting di IRIS GL, funzioni Clear
- porting da IRIS GL, funzioni Clear
- porting in OpenGL da IRIS GL, funzioni Clear
- Porting OpenGL da IRIS GL, funzioni Clear
- funzioni Clear
- Porting di IRIS GL, comandi di cancellazione dello schermo
- porting da IRIS GL, comandi di cancellazione dello schermo
- porting in OpenGL da IRIS GL, comandi di cancellazione dello schermo
- Porting OpenGL da IRIS GL, comandi di cancellazione dello schermo
- comandi di cancellazione dello schermo
- Porting di IRIS GL, comandi di cancellazione del buffer
- porting da IRIS GL, comandi di cancellazione del buffer
- porting in OpenGL da IRIS GL, comandi di cancellazione del buffer
- Porting OpenGL da IRIS GL, comandi di cancellazione del buffer
- comandi di cancellazione del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298537"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Porting dei comandi di cancellazione dello schermo e del buffer

OpenGL sostituisce un'ampia gamma di funzioni **Clear** di Iris GL, ad esempio **zclear**, **aClear**, **sClear** e così via, con una singola funzione, [**glClear**](glclear.md). Specificare esattamente ciò che si vuole cancellare passando le maschere a **glClear**.

Quando si portano i comandi dello schermo e del buffer, tenere presente quanto segue:

-   OpenGL mantiene la cancellazione dei colori separatamente dai colori di disegno, con chiamate come [**glClearColor**](glclearcolor.md) e [**glClearIndex**](glclearindex.md). Assicurarsi di impostare il colore chiaro per ogni buffer prima della cancellazione.
-   Anziché utilizzare una delle diverse chiamate Clear denominate in modo diverso, è ora possibile cancellare diversi buffer con una sola chiamata, [**glClear**](glclear.md), **o** insieme a maschere del buffer. **Czclear** , ad esempio, viene sostituito da:

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL fa riferimento al poligono stipple e al colore writemask. OpenGL ignora il poligono stipple, ma fa riferimento al colore writemask. La funzione **czclear** ignora sia il poligono stipple che il colore writemask.

La tabella seguente elenca le varie funzioni Clear di IRIS GL con le funzioni OpenGL equivalenti.



| Chiamata a IRIS GL         | Chiamata OpenGL                                                               | Significato                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**( \_ Clear AC) | **glClear**( \_ bit del buffer di accut GL \_ \_ )                                     | Cancellare il buffer di accumulo.                    |
|                      | **glClearColor**                                                          | Impostare il colore di RGBA Clear.                         |
|                      | **glClearIndex**                                                          | Impostare l'indice Clear-Color.                        |
| **deselezionare**            | **glClear**( \_ bit del buffer dei colori GL \_ \_ )                                     | Cancellare il buffer dei colori.                           |
|                      | **glClearDepth**                                                          | Specificare il valore Clear per il buffer di profondità.     |
| **zclear**           | **glClear**( \_ bit del buffer di profondità GL \_ \_ )                                     | Cancellare il buffer di profondità.                           |
| **czclear**          | **glClear**(bit del buffer di \_ bit GL del buffer dei colori GL \_ \_ \| \_ \_ \_ )<br/> | Cancellare il buffer dei colori e il buffer di profondità.      |
|                      | **glClearAccum**                                                          | Specificare valori non crittografati per il buffer di accumulo. |
|                      | **glClearStencil**                                                        | Specificare il valore Clear per il buffer dello stencil.   |
| **sclear**           | **glClear**( \_ bit del buffer dello stencil GL \_ \_ )                                   | Cancellare il buffer dello stencil.                         |



 

Quando il codice di IRIS GL USA sia **gclear** che **sClear**, è possibile combinarli in una singola chiamata **glClear** ; può migliorare le prestazioni del programma.

 

 






---
title: Porting di funzioni di trama
description: Porting di funzioni di trama
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044940"
---
# <a name="porting-texture-functions"></a>Porting di funzioni di trama

Quando si esegue il porting delle funzioni di trama di IRIS GL in OpenGL, tenere presente quanto segue:

-   OpenGL non mantiene le tabelle di trame; USA solo la trama a una D e la trama 2D. Per riutilizzare le trame dal codice di IRIS GL, inserirle in un elenco di visualizzazione.
-   OpenGL non genera automaticamente mipmap. Se si usa mipmap, è necessario chiamare prima la funzione [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .
-   In OpenGL si usano [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) per attivare e disattivare le funzionalità di texturing.
-   In OpenGL, le dimensioni della trama sono più rigorosamente regolate rispetto a IRIS GL. Le dimensioni di una trama OpenGL devono essere le seguenti:

    2 *n* + 2 *b*

    dove *n* è un numero intero e *b* è:

    -   0, se la trama non ha bordo
    -   1, se la trama ha un pixel del bordo, le trame OpenGL possono avere bordi di 1 pixel.

La tabella seguente elenca le funzioni di trama di IRIS GL e i rispettivi equivalenti OpenGL generali.



| Funzione IRIS GL | OpenGL (funzione)                                                                                                                                                                                                                                                       | Significato                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [](glteximage2d.md)[**glTexParameter** glTexImage2D](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Specifica un'immagine di trama 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Seleziona una funzione di trama.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Definisce un ambiente di mapping di trame.                                                      |
| **tevbind**      | [**glTexImage1D** glTexEnv](glteximage1d.md)<br/>                                                                                                                                                                                                           | Seleziona un ambiente di trama.                                                              |
| **T2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Imposta le coordinate di trama correnti.                                                       |
| **texgen**       | [](gltexgen-functions.md)[**glGetTexParameter** glTexGen](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Controlla la generazione delle coordinate di trama. Ridimensiona un'immagine a una dimensione arbitraria.<br/> |



 

Per ulteriori informazioni sul texturing, vedere la *Guida alla programmazione di OpenGL*.

Questo argomento include informazioni sui seguenti elementi.

-   [Conversione di tevdef](translating-tevdef.md)
-   [Conversione di texdef](translating-texdef.md)
-   [Conversione di texgen](translating-texgen.md)

 

 






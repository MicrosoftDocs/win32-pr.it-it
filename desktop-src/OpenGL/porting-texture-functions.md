---
title: Funzioni di trame di porting
description: Funzioni di trame di porting
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Porting IRIS GL, trama
- porting da IRIS GL, trama
- porting a OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17cd79aaf8e7e5b90d0f171ddcec4b49b6d15b3615ccc1f5e44a04b3e16fae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339241"
---
# <a name="porting-texture-functions"></a>Funzioni di trame di porting

Quando si esegue il porting delle funzioni di trama IRIS GL in OpenGL, tenere presente quanto segue:

-   OpenGL non gestisce tabelle di trame; usa solo una trama 1D e una trama 2D. Per riutilizzare le trame dal codice IRIS GL, inserire le trame in un elenco di visualizzazione.
-   OpenGL non genera automaticamente mipmap. Se si usano mipmap, è necessario chiamare prima la [**funzione gluBuild2DMipmaps.**](glubuild2dmipmaps.md)
-   In OpenGL si usano [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) per attivare e disattivare le funzionalità di texturing.
-   In OpenGL le dimensioni delle trame sono più rigorosamente regolamentate rispetto a IRIS GL. Le dimensioni di una trama OpenGL devono essere:

    2 *n* + 2 *b*

    dove *n* è un numero intero e *b* è:

    -   0, se la trama non ha un bordo
    -   1, se la trama ha un pixel del bordo (le trame OpenGL possono avere bordi di 1 pixel).

Nella tabella seguente sono elencate le funzioni di trama IRIS GL e i relativi equivalenti OpenGL generali.



| Funzione GL IRIS | Funzione OpenGL                                                                                                                                                                                                                                                       | Significato                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Specifica un'immagine di trama 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Seleziona una funzione di trama.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Definisce un ambiente di mapping trame.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Seleziona un ambiente di trama.                                                              |
| **t2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Imposta le coordinate della trama corrente.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Controlla la generazione delle coordinate della trama. Ridimensiona un'immagine a dimensioni arbitrarie.<br/> |



 

Per altre informazioni sulla creazione di testo, vedere la *Guida per programmatori OpenGL.*

Questo argomento include informazioni sugli argomenti seguenti.

-   [Traduzione di tevdef](translating-tevdef.md)
-   [Traduzione di texdef](translating-texdef.md)
-   [Traduzione di texgen](translating-texgen.md)

 

 






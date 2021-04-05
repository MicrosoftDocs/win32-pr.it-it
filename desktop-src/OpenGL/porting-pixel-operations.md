---
title: Porting di operazioni pixel
description: Porting di operazioni pixel
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Porting di IRIS GL, pixel
- porting da IRIS GL, pixel
- porting in OpenGL da IRIS GL, pixel
- Porting OpenGL da IRIS GL, pixel
- pixel, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712508"
---
# <a name="porting-pixel-operations"></a>Porting di operazioni pixel

Quando si esegue il porting di codice che coinvolge operazioni in pixel, tenere presente quanto segue:

-   Le operazioni di pixel logici non vengono applicate ai buffer dei colori RGBA. Per ulteriori informazioni, vedere [**glLogicOp**](gllogicop.md).
-   In generale, IRIS GL usa il formato ABGR per pixel, mentre OpenGL USA RGBA. È possibile modificare il formato con [**glPixelStore**](glpixelstore-functions.md).
-   Quando si esegue il porting delle funzioni **lrectwrite** , prestare attenzione a prendere nota del percorso di scrittura di **lrectwrite** (ad esempio, potrebbe scrivere nel buffer di profondità).

OpenGL offre una maggiore flessibilità nelle operazioni pixel. La tabella seguente elenca le funzioni di IRIS GL per le operazioni pixel e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                                   | OpenGL (funzione)                                                                           | Significato                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**, **rectread**,**readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Legge un blocco di pixel dal framebuffer.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Scrive un blocco di pixel nel framebuffer.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Copia i pixel nel framebuffer.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Specifica i fattori di zoom pixel per **glDrawPixels** e **glCopyPixels**. |
| **CMOV**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Specifica la posizione raster per le operazioni pixel.                         |
| **readsource**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Consente di selezionare un'origine del buffer dei colori per i pixel.                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Imposta le modalità di archiviazione pixel. Impostare le modalità di trasferimento pixel.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Specifica un'operazione logica per le Scritture in pixel.                         |
|                                                    | [**glEnable**](glenable.md) ( \_ op logica GL \_ )                                            | Attiva le operazioni della logica pixel.                                        |



 

Per un elenco completo delle possibili operazioni logiche, vedere [**glLogicOp**](gllogicop.md).

Questo esempio di codice IRIS GL Mostra una tipica scrittura in pixel:

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

Il codice precedente ha un aspetto simile al seguente quando viene convertito in OpenGL:

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 






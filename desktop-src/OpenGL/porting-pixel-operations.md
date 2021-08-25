---
title: Porting di operazioni pixel
description: Porting di operazioni pixel
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Porting IRIS GL, pixel
- porting da IRIS GL,pixel
- porting a OpenGL da IRIS GL,pixel
- Porting OpenGL da IRIS GL, pixel
- pixel, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc67a4c9224dbe6544c60cb205f8a192517af7f3ab16ba64134b4d55d1c8676f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132380"
---
# <a name="porting-pixel-operations"></a>Porting di operazioni pixel

Quando si esegue la porting di codice che comporta operazioni sui pixel, tenere presenti i punti seguenti:

-   Le operazioni dei pixel logici non vengono applicate ai buffer di colore RGBA. Per altre informazioni, vedere [**glLogicOp**](gllogicop.md).
-   In generale, IRIS GL usa il formato ABGR per i pixel, mentre OpenGL usa RGBA. È possibile modificare il formato con [**glPixelStore**](glpixelstore-functions.md).
-   Quando si esegue la porting delle funzioni **lrectwrite,** prestare attenzione a notare dove **lrectwrite** sta scrivendo (ad esempio, potrebbe essere scritto nel buffer di profondità).

OpenGL offre una maggiore flessibilità nelle operazioni sui pixel. La tabella seguente elenca le funzioni IRIS GL per le operazioni sui pixel e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                                   | Funzione OpenGL                                                                           | Significato                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread,** **rectread,****readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Legge un blocco di pixel dal framebuffer.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Scrive un blocco di pixel nel framebuffer.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Copia i pixel nel framebuffer.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Specifica i fattori di zoom dei pixel **per glDrawPixels** e **glCopyPixels**. |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Specifica la posizione raster per le operazioni in pixel.                         |
| **readsource**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Seleziona un'origine del buffer dei colori per i pixel.                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Imposta le modalità di archiviazione pixel. Impostare le modalità di trasferimento dei pixel.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Specifica un'operazione logica per le scritture in pixel.                         |
|                                                    | [**glEnable**](glenable.md) ( GL \_ LOGIC \_ OP )                                            | Attiva le operazioni di logica dei pixel.                                        |



 

Per un elenco completo delle possibili operazioni logiche, vedere [**glLogicOp**](gllogicop.md).

Questo esempio di codice IRIS GL mostra una tipica scrittura in pixel:

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

Il codice precedente è simile al seguente quando viene convertito in OpenGL:

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 






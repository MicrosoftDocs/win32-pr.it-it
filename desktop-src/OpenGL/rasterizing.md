---
title: Rasterizzazione
description: La rasterizzazione è il processo tramite il quale una primitiva viene convertita in un'immagine bidimensionale.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Pipeline di elaborazione OpenGL, rasterizzazione
- rasterizzazione di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192f8fdd919c14be4bd47688abf911b363e13f2e8ca9606f1943eb2956378ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776881"
---
# <a name="rasterizing"></a>Rasterizzazione

*La rasterizzazione* è il processo tramite il quale una primitiva viene convertita in un'immagine bidimensionale. Ogni punto di questa immagine contiene informazioni quali i dati relativi a colore, profondità e trama. Un punto e le informazioni associate sono detti *frammenti.* La posizione raster corrente, come specificato con [**glRasterPos \***](glrasterpos-functions.md), viene usata in vari modi durante questa fase per disegnare pixel e bitmap. Si verificano diversi problemi durante la rasterizzazione di punti, segmenti di linea e poligoni. Inoltre, i rettangoli pixel e le bitmap devono essere rasterizzati.

Con OpenGL è possibile controllare la rasterizzazione usando le funzioni seguenti:

-   Primitive. Controllare il modo in cui le primitive vengono rasterizzate usando funzioni che determinano le dimensioni e i modelli di stipple: [**glPointSize,**](glpointsize.md) [**glLineWidth,**](gllinewidth.md) [**glLineStipple**](gllinestipple.md)e [**glPolygonStipple**](glpolygonstipple.md). Controllare il modo in cui i visi anteriore e posteriore dei poligoni vengono rasterizzati con [**glCullFace**](glcullface.md), [**glFrontFace**](glfrontface.md)e [**glPolygonMode**](glpolygonmode.md).
-   Pixel. Diverse funzioni controllano le modalità di archiviazione e trasferimento dei pixel. La funzione [ * *glPixelStore \** _](glpixelstore-functions.md) controlla la codifica dei pixel nella memoria client e [_*glPixelTransfer \**_](glpixeltransfer.md) e [_*glPixelMap \**_](glpixelmap.md) controllano la modalità di elaborazione dei pixel prima di essere inseriti nel framebuffer. Specificare un rettangolo in pixel [con _ *glDrawPixels;* *](gldrawpixels.md)controllarne la rasterizzazione [**con glPixelZoom**](glpixelzoom.md).
-   Bitmap. Le bitmap sono rettangoli di zeri e quelli che specificano un particolare modello di frammenti da produrre. Ognuno di questi frammenti ha gli stessi dati associati. La [**funzione glBitmap**](glbitmap.md) specifica una bitmap.
-   Memoria trame. Quando la texturing è abilitata, la trama esegue il mapping di una parte di un'immagine di trama specificata a ogni primitiva. Questo mapping viene ottenuto usando il colore dell'immagine della trama nella posizione indicata dalle coordinate di trama di un frammento per modificare il colore RGBA del frammento. Specificare un'immagine di trama [**con glTexImage2D**](glteximage2d.md) [**o glTexImage1D.**](glteximage1d.md) Le [ * *funzioni \* glTexParameter* _](gltexparameter-functions.md) e [_ *glTexEnv \** *](gltexenv-functions.md) controllano il modo in cui i valori di trama vengono interpretati e applicati a un frammento.
-   Nebbia. Per sfumare un colore della nebbia con il colore post-texturing di un frammento rasterizzato, usare un fattore di fusione che dipende dalla distanza tra il punto dell'occhio e il frammento. Usare [**glFog \* per**](glfog.md) specificare il colore della nebbia e il fattore di fusione.

 

 





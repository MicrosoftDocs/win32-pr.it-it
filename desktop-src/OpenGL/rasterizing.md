---
title: Rasterizzazione
description: La rasterizzazione è il processo mediante il quale una primitiva viene convertita in un'immagine bidimensionale.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Pipeline di elaborazione OpenGL, rasterizzazione
- rasterizzazione di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0d8e7ece3bead408b8d056356593879edc638c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515643"
---
# <a name="rasterizing"></a>Rasterizzazione

La *rasterizzazione* è il processo mediante il quale una primitiva viene convertita in un'immagine bidimensionale. Ogni punto di questa immagine contiene informazioni quali i dati di colore, profondità e trama. Un punto e le relative informazioni associate sono detti *frammenti*. La posizione raster corrente, come specificato con [**glRasterPos \***](glrasterpos-functions.md), viene usata in diversi modi durante questa fase per disegnare pixel e bitmap. Si verificano problemi diversi durante la rasterizzazione di punti, segmenti di linea e poligoni. Inoltre, è necessario rasterizzare i rettangoli e le bitmap pixel.

Con OpenGL è possibile controllare la rasterizzazione usando le funzioni seguenti:

-   Primitives. Controllare il modo in cui vengono rasterizzate le primitive usando le funzioni che determinano le dimensioni e i modelli di Stipple: [**glPointSize**](glpointsize.md), [**glLineWidth**](gllinewidth.md), [**glLineStipple**](gllinestipple.md)e [**glPolygonStipple**](glpolygonstipple.md). Controllare il modo in cui i volti anteriore e posteriore dei poligoni vengono rasterizzati con [**glCullFace**](glcullface.md), [**glFrontFace**](glfrontface.md)e [**glPolygonMode**](glpolygonmode.md).
-   Pixel. Diverse funzioni controllano le modalità di trasferimento e archiviazione in pixel. La funzione [**glPixelStore \***](glpixelstore-functions.md) controlla la codifica dei pixel nella memoria client e [**glPixelTransfer \***](glpixeltransfer.md) e [**glPixelMap \***](glpixelmap.md) controllano il modo in cui vengono elaborati i pixel prima di essere inseriti nel framebuffer. Specificare un rettangolo pixel con [**glDrawPixels**](gldrawpixels.md); controllare la rasterizzazione con [**glPixelZoom**](glpixelzoom.md).
-   Bitmap. Le bitmap sono rettangoli di zeri e quelli che specificano un particolare modello di frammenti da produrre. Ognuno di questi frammenti ha gli stessi dati associati. La funzione [**glBitmap**](glbitmap.md) specifica una bitmap.
-   Memoria trama. Quando è abilitata la funzionalità di texturing, il texturing esegue il mapping di una parte di un'immagine di trama specificata su ogni primitiva. Questo mapping viene eseguito usando il colore dell'immagine della trama nella posizione indicata dalle coordinate di trama di un frammento per modificare il colore RGBA del frammento. Specificare un'immagine di trama con [**glTexImage2D**](glteximage2d.md) o [**glTexImage1D**](glteximage1d.md). Le [**funzioni \* GlTexParameter**](gltexparameter-functions.md) e [**glTexEnv \***](gltexenv-functions.md) controllano il modo in cui i valori di trama vengono interpretati e applicati a un frammento.
-   Nebbia. Per fondere un colore di nebbia con un colore di post-texturing del frammento rasterizzato, usare un fattore di fusione che dipende dalla distanza tra il osservazione e il frammento. Usare [**glFog \***](glfog.md) per specificare il colore di nebbia e il fattore di fusione.

 

 





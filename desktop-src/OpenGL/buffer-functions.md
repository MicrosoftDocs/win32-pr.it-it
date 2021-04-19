---
title: Funzioni buffer
description: Per copiare il contenuto di un buffer fuori schermo in un buffer a schermo, chiamare SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funzioni WGL, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320316"
---
# <a name="buffer-functions"></a>Funzioni buffer

Per copiare il contenuto di un buffer fuori schermo in un buffer a schermo, chiamare [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). La funzione **SwapBuffers** accetta un handle per un contesto di dispositivo. Il formato pixel corrente per il contesto di dispositivo specificato deve includere un buffer nascosto. Per impostazione predefinita, il buffer nascosto è fuori schermo e il buffer anteriore è visualizzato sullo schermo.

> [!Note]  
> La funzione **SwapBuffers** non scambia effettivamente il contenuto dei due buffer, bensì copia il contenuto di un buffer in un altro. Il contenuto del buffer fuori schermo non è definito dopo una chiamata a **SwapBuffers**. Pertanto, il risultato di due chiamate consecutive a **SwapBuffers** non è definito.

 

Nella figura seguente viene illustrato il modo in cui il contenuto dei buffer viene copiato quando si chiama **SwapBuffers**.

![Diagramma che mostra i risultati non definiti di chiamate consecutive alla funzione SwapBuffers.](images/opengl00.png)

Diverse funzioni di base di OpenGL gestiscono anche i buffer. La funzione [**glDrawBuffer**](gldrawbuffer.md) è l'unica più rilevante per il doppio buffer; Specifica il framebuffer o i buffer in cui viene disegnato OpenGL.

Anche le funzioni seguenti influiscono sui buffer:

-   [**glReadBuffer**](glreadbuffer.md)
-   [**glReadPixels**](glreadpixels.md)
-   [**glCopyPixels**](glcopypixels.md)
-   [**glAccum**](glaccum.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glIndexMask**](glindexmask.md)
-   [**glStencilMask**](glstencilmask.md)
-   [**glClearAccum**](glclearaccum.md)
-   [**glClearColor**](glclearcolor.md)
-   [**glClearDepth**](glcleardepth.md)
-   [**glClearIndex**](glclearindex.md)
-   [**glClearStencil**](glclearstencil.md)

 

 





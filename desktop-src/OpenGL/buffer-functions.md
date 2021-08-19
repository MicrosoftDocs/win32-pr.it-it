---
title: Funzioni buffer
description: Per copiare il contenuto di un buffer fuori schermo in un buffer su schermo, chiamare SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Funzioni WGL, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b03a12cd07b76d1329f51cc982508c707e011701b072a42b099df05327842d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618597"
---
# <a name="buffer-functions"></a>Funzioni buffer

Per copiare il contenuto di un buffer fuori schermo in un buffer su schermo, chiamare [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). La **funzione SwapBuffers** accetta un handle per un contesto di dispositivo. Il formato pixel corrente per il contesto di dispositivo specificato deve includere un buffer nascosto. Per impostazione predefinita, il buffer nascosto è fuori schermo e il front buffer è sullo schermo.

> [!Note]  
> La **funzione SwapBuffers** non scambia effettivamente il contenuto dei due buffer, ma copia il contenuto di un buffer in un altro. Il contenuto del buffer fuori schermo non è definito dopo una chiamata a **SwapBuffers**. Di conseguenza, il risultato di due chiamate consecutive a **SwapBuffers** non è definito.

 

La figura seguente mostra come viene copiato il contenuto dei buffer quando si **chiama SwapBuffers**.

![Diagramma che mostra i risultati non definiti delle chiamate consecutive alla funzione SwapBuffers.](images/opengl00.png)

Anche diverse funzioni di base OpenGL gestiscono i buffer. La [**funzione glDrawBuffer**](gldrawbuffer.md) è quella più rilevante per il doppio buffering. specifica il framebuffer o i buffer in cui OpenGL disegna.

Le funzioni seguenti influiscono anche sui buffer:

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

 

 





---
title: Disegno con buffer doppi
description: I doppi buffer smussano la transizione tra un'immagine e l'altra sullo schermo.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL per Windows, buffer doppi
- doppio buffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332068"
---
# <a name="drawing-with-double-buffers"></a><span data-ttu-id="eb783-105">Disegno con buffer doppi</span><span class="sxs-lookup"><span data-stu-id="eb783-105">Drawing with Double Buffers</span></span>

<span data-ttu-id="eb783-106">I doppi buffer smussano la transizione tra un'immagine e l'altra sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="eb783-106">Double buffers smooth the transition between one image and another on the screen.</span></span> <span data-ttu-id="eb783-107">Lo scambio di buffer in genere viene visualizzato alla fine di una sequenza di comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="eb783-107">Swapping buffers typically comes at the end of a sequence of drawing commands.</span></span> <span data-ttu-id="eb783-108">Per impostazione predefinita, l'implementazione Microsoft di OpenGL in Windows disegna il buffer fuori schermo; al termine del disegno, chiamare la funzione [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) per copiare il buffer fuori schermo nel buffer su schermo.</span><span class="sxs-lookup"><span data-stu-id="eb783-108">By default, the Microsoft implementation of OpenGL in Windows draws to the off-screen buffer; when drawing is complete, you call the [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) function to copy the off-screen buffer to the on-screen buffer.</span></span> <span data-ttu-id="eb783-109">L'esempio di codice seguente si prepara a disegnare, chiama una funzione di disegno e quindi copia l'immagine completata sullo schermo se è disponibile il doppio buffering.</span><span class="sxs-lookup"><span data-stu-id="eb783-109">The following code sample prepares to draw, calls a drawing function, and then copies the completed image on to the screen if double buffering is available.</span></span>


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



<span data-ttu-id="eb783-110">Nell'esempio di codice seguente viene ottenuto un contesto di dispositivo della finestra, viene eseguito il rendering di una scena, viene copiata l'immagine sullo schermo (per visualizzare il rendering), quindi viene rilasciato il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb783-110">The following code sample obtains a window device context, renders a scene, copies the image to the screen (to show the rendering), and then releases the device context.</span></span>


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 





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
# <a name="drawing-with-double-buffers"></a>Disegno con buffer doppi

I doppi buffer smussano la transizione tra un'immagine e l'altra sullo schermo. Lo scambio di buffer in genere viene visualizzato alla fine di una sequenza di comandi di disegno. Per impostazione predefinita, l'implementazione Microsoft di OpenGL in Windows disegna il buffer fuori schermo; al termine del disegno, chiamare la funzione [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) per copiare il buffer fuori schermo nel buffer su schermo. L'esempio di codice seguente si prepara a disegnare, chiama una funzione di disegno e quindi copia l'immagine completata sullo schermo se è disponibile il doppio buffering.


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



Nell'esempio di codice seguente viene ottenuto un contesto di dispositivo della finestra, viene eseguito il rendering di una scena, viene copiata l'immagine sullo schermo (per visualizzare il rendering), quindi viene rilasciato il contesto di dispositivo.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 





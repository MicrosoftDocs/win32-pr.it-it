---
title: Disegno con buffer doppi
description: I buffer doppi smussano la transizione tra un'immagine e un'altra sullo schermo.
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- OpenGL su Windows,doppio buffer
- doppio buffer OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133a6e0794eb903215411016aeff14e3426854dcddc3a60bcfb2ba318481bee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361391"
---
# <a name="drawing-with-double-buffers"></a>Disegno con buffer doppi

I buffer doppi smussano la transizione tra un'immagine e un'altra sullo schermo. Lo scambio dei buffer si verifica in genere alla fine di una sequenza di comandi di disegno. Per impostazione predefinita, l'implementazione Microsoft di OpenGL in Windows disegna sul buffer fuori schermo; Al termine del disegno, chiamare la [**funzione SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) per copiare il buffer fuori schermo nel buffer su schermo. L'esempio di codice seguente si prepara a disegnare, chiama una funzione di disegno e quindi copia l'immagine completata sullo schermo se è disponibile il doppio buffer.


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



L'esempio di codice seguente ottiene un contesto di dispositivo della finestra, esegue il rendering di una scena, copia l'immagine sullo schermo (per visualizzare il rendering) e quindi rilascia il contesto di dispositivo.


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 





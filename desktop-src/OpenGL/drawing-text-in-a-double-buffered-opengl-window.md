---
title: Disegno di testo in una Double-Buffered OpenGL
description: È possibile disegnare testo in una finestra OpenGL a doppio buffer creando elenchi di visualizzazione per i caratteri selezionati in un tipo di carattere e quindi eseguendo l'elenco di visualizzazione appropriato per ogni carattere che si vuole disegnare.
ms.assetid: 59ac0414-a845-4f40-be9c-9962fd1585f6
keywords:
- OpenGL su Windows,text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84202f59ca1a232bae37603b2ff657cb5c61ae0a1d3961b960b624d061ab20cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618546"
---
# <a name="drawing-text-in-a-double-buffered-opengl-window"></a>Disegno di testo in una Double-Buffered OpenGL

È possibile disegnare testo in una finestra OpenGL a doppio buffer creando elenchi di visualizzazione per i caratteri selezionati in un tipo di carattere e quindi eseguendo l'elenco di visualizzazione appropriato per ogni carattere che si vuole disegnare. L'esempio di codice seguente crea un contesto di rendering, disegna un triangolo rosso e quindi lo etichetta con testo. Per questo codice di esempio si presuppone che sia presente un contesto di dispositivo, con un tipo di carattere e un formato pixel.


```C++
// create an OpenGL rendering context  
hglrc = wglCreateContext(hdc); 
 
// make it this thread's current rendering context  
wglMakeCurrent(hdc, hglrc); 
 
// make the color a deep blue hue  
glClearColor(0.0F, 0.0F, 0.4F, 1.0F); 
 
// make the shading smooth 
glShadeModel(GL_SMOOTH); 
 
// clear the color buffers  
glClear(GL_COLOR_BUFFER_BIT); 
 
// specify a red triangle  
glBegin(GL_TRIANGLES); 
    glColor3f(1.0F, 0.0F, 0.0F); 
    glVertex2f(10.0F, 10.0F); 
    glVertex2f(250.0F, 50.0F); 
    glVertex2f(105.0F, 280.0F); 
glEnd(); 
 
// create bitmaps for the device context font's first 256 glyphs  
wglUseFontBitmaps(hdc, 0, 256, 1000); 
 
// move bottom left, southwest of the red triangle  
glRasterPos2f(30.0F, 300.0F); 
 
// set up for a string-drawing display list call  
glListBase(1000); 
 
// draw a string using font display lists  
glCallLists(12, GL_UNSIGNED_BYTE, "Red Triangle"); 
 
// get all those commands to execute  
glFlush(); 
 
// delete our 256 glyph display lists  
glDeleteLists(1000, 256) ; 
 
// make the rendering context not current  
wglMakeCurrent (NULL, NULL) ; 
 
// release the device context  
ReleaseDC(hdc) ; 
 
// delete the rendering context  
wglDeleteContext(hglrc);
```



 

 





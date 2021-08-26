---
title: Una porta di esempio di un elenco di visualizzazione
description: In questo argomento viene fornito un esempio di codice IRIS GL che definisce tre elenchi di visualizzazione. uno degli elenchi di visualizzazione fa riferimento agli altri nella relativa definizione. L'esempio IRIS GL seguente è un esempio dell'aspetto del codice quando viene portato in OpenGL.
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- Porting IRIS GL, elenchi di visualizzazione
- porting da IRIS GL,visualizzare elenchi
- porting a OpenGL da IRIS GL, visualizzazione di elenchi
- Porting OpenGL da IRIS GL, visualizzazione di elenchi
- elenchi di visualizzazione, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbb696673da7f4dc83abd625bb616b67449de64a40df1cfc99bd429a2a980e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962431"
---
# <a name="a-sample-port-of-a-display-list"></a>Una porta di esempio di un elenco di visualizzazione

In questo argomento viene fornito un esempio di codice IRIS GL che definisce tre elenchi di visualizzazione. uno degli elenchi di visualizzazione fa riferimento agli altri nella relativa definizione. L'esempio IRIS GL seguente è un esempio dell'aspetto del codice quando viene portato in OpenGL.

## <a name="iris-gl-sample-display-list-code"></a>Codice elenco di visualizzazione di esempio IRIS GL


```C++
makeobj(10);  // 10 object  
    cpack(0x0000FF); 
    recti(164, 33, 364, 600);   // Hollow rectangle  
closeobj(); 
 
makeobj(20);  // 20 object  
    cpack(0xFFFF00); 
    circle(0, 0, 25);           // Unfilled circle  
    recti(100, 100, 200, 200);  // Filled rectangle  
closeobj(); 
 
makeobj(30);  // 30 object  
    callobj(10); 
    cpack(0xFFFFFF); 
    recti(400, 100, 500, 300);  // Draw filled rectangle  
    callobj(20); 
closeobj(); 
 
// Now draw by calling the lists  
call(30);
```



## <a name="opengl-sample-display-list-code"></a>Codice elenco di visualizzazione di esempio OpenGL

Ecco il codice GL IRIS precedente tradotto in OpenGL:


```C++
glNewList(10, GL_COMPILE);            // List #10  
    glColor3f(1, 0, 0); 
    glRecti(164, 33, 364, 600); 
glEndList(); 
 
glNewList(20, GL_COMPILE);            //List #20  
    glColor3f(1, 1, 0);               // Set color to YELLOW  
    glPolygonMode(GL_BOTH, GL_LINE);  // Unfilled mode  
    glBegin(GL_POLYGON);  // Use polygon to approximate a circle  
        for(i=0; i<100; i++) { 
            cosine = 25 * cos(i * 2 * PI/100.0); 
            sine =   25 * sin(i * 2 * PI/100.0); 
            glVertex2f(cosine, sine); 
        } 
    glEnd(); 
    glBegin(GL_QUADS); 
        glColorf(0, 1, 1);            // Set color to CYAN  
        glVertex2i(100, 100); 
        glVertex2i(100, 200); 
        glVertex2i(200, 200); 
        glVertex2i(100, 200); 
    glEnd(); 
glEndList(); 
 
glNewList(30, GL_COMPILE);            // List #30  
    glCallList(10); 
        glColorf(1, 1, 1);            // Set color to WHITE  
        glRecti(400, 100, 500, 300); 
    glCallList(20); 
glEndList(); 
 
// Execute the display lists  
glCallList(30);
```



 

 





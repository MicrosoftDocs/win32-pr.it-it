---
title: Porting di profondità e comandi di nebbia
description: Porting di profondità e comandi di nebbia
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Porting di IRIS GL, CUE Depth
- porting da IRIS GL, incue Depth
- porting in OpenGL da IRIS GL, incue Depth
- Porting OpenGL da IRIS GL, incue di profondità
- Porting di IRIS GL, nebbia
- porting da IRIS GL, Fog
- porting in OpenGL da IRIS GL, Fog
- Porting OpenGL da IRIS GL, nebbia
- Cue di profondità
- nebbia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221824"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Porting di profondità e comandi di nebbia

Quando si esegue il porting dei comandi Depth-cue e Fog, tenere presente quanto segue:

-   La chiamata a IRIS GL, **fogvertex**, imposta una modalità e i parametri che interessano tale modalità. In OpenGL è possibile chiamare [**glFog**](glfog.md) una volta per impostare la modalità e quindi di nuovo due volte o più per impostare vari parametri.
-   In OpenGL il ripasso della profondità non è una funzionalità separata. Utilizzare la nebbia lineare anziché il ripasso della profondità. Questa sezione fornisce un esempio di come eseguire questa operazione. Le seguenti funzioni di IRIS GL non hanno un equivalente OpenGL diretto:

    **depthcue**

    **lRGBrange**

    **lshaderange**

    **getdcm**

-   Per modificare la qualità di nebbia, usare [**glHint**](glhint.md)( \_ hint di nebbia GL \_ ).

La tabella seguente elenca le funzioni di IRIS GL per la gestione della nebbia e delle funzioni OpenGL equivalenti.



| Funzione IRIS GL         | OpenGL (funzione)                                     | Significato                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **fogvertex**            | [**glFog**](glfog.md)                              | Imposta vari parametri di nebbia.      |
| **fogvertex**(FG \_ su)  | [**glEnable**](glenable.md) (GL \_ Fog)            | Attiva la nebbia.                     |
| **fogvertex**(FG \_ disattivato) | [**glDisable**](gldisable.md) (GL \_ Fog)          | Disattiva la nebbia.                    |
| **depthcue**             | [**glFog**](glfog.md) (GL \_ Fog \_ mod, GL \_ lineare) | Usa la nebbia lineare per il ripasso della profondità. |



 

La tabella seguente elenca i parametri che è possibile passare a **glFog**.



| Parametro Fog    | Significato                       | Predefinito                  |
|------------------|-------------------------------|--------------------------|
| \_densità di nebbia GL \_ | Densità di nebbia.                  | 1.0                      |
| \_inizio di nebbia GL \_   | Near distance per la nebbia lineare. | 0,0                      |
| \_fine nebbia \_ GL     | Distanza per la nebbia lineare.  | 1.0                      |
| \_indice di nebbia GL \_   | Indice colori nebbia.              | 0,0                      |
| \_colore di nebbia GL \_   | Colore RGBA nebbia.               | (0, 0, 0, 0)             |
| \_modalità di nebbia GL \_    | Modalità nebbia.                     | Vedere la tabella seguente. |



 

Il parametro di densità della nebbia di OpenGL è diverso da quello in IRIS GL. Sono correlate come segue:

-   Se *fogMode* = exp2
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **Sqrt** ( **log** (1/255)))
-   Se *fogMode* = exp
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))

dove **Sqrt** è l'operazione radice quadrata, **log** è il logaritmo naturale, *irisGLfogDensity* è la densità di nebbia di Iris GL e *OpenGLfogDensity* è la densità di nebbia di OpenGL.

Per passare da una modalità all'altra in modalità per pixel e per ogni vertice, utilizzare [**glHint**](glhint.md)(GL \_ Fog \_ hint, *hintMode*). Sono disponibili due modalità di suggerimento:

-   \_Calcolo della nebbia per pixel più gradevole
-   \_Calcolo della nebbia più veloce per vertice di GL

La tabella seguente elenca le modalità di nebbia di IRIS GL e i rispettivi equivalenti di OpenGL.



| Modalità di nebbia di IRIS GL                       | Modalità nebbia di OpenGL | Modalità hint                         | Significato                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ VTX \_ Exp, FG \_ pix \_ Exp<br/>   | \_Exp GL         | GL più \_ veloce, GL più \_ bello<br/> | Modalità di nebbia intensa (impostazione predefinita).                |
| FG \_ VTX \_ exp2, FG \_ pix \_ exp2<br/> | \_Exp2 GL        | GL più \_ veloce, GL più \_ bello<br/> | Modalità Haze.                               |
| FG \_ VTX \_ Lin, FG \_ pix \_ Lin<br/>   | \_linea GL      | GL più \_ veloce, GL più \_ bello<br/> | Modalità nebbia lineare. (Usare per il ripasso della profondità). |



 

Nell'esempio di codice riportato di seguito viene illustrata la profondità in OpenGL:


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 






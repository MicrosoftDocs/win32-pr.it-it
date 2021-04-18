---
title: Libreria IRIS GL Sphere
description: OpenGL non supporta la libreria IRIS GL Sphere. È possibile sostituire le chiamate della libreria Sphere con le routine quadriche dalla libreria GLU. Per ulteriori informazioni sulla libreria GLU, vedere la guida per programmatori Open GL e la libreria di utilità OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Porting di IRIS GL, libreria Sphere
- porting da IRIS GL, Sphere Library
- porting in OpenGL da IRIS GL, Sphere Library
- Porting OpenGL da IRIS GL, Sphere Library
- funzioni di disegno, libreria Sphere
- libreria Sphere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330639"
---
# <a name="the-iris-gl-sphere-library"></a>Libreria IRIS GL Sphere

OpenGL non supporta la libreria IRIS GL Sphere. È possibile sostituire le chiamate della libreria Sphere con le routine quadriche dalla libreria GLU. Per ulteriori informazioni sulla libreria GLU, vedere la *Guida per programmatori Open GL* e la [libreria di utilità OpenGL](opengl-utility-library.md).

La tabella seguente elenca le funzioni OpenGL quadriche.



| OpenGL (funzione)                                        | Significato                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**gluNewQuadric**](glunewquadric.md)                 | Crea un nuovo oggetto quadrica.                                    |
| [**gluDeleteQuadric**](gludeletequadric.md)           | Elimina un oggetto quadrica.                                        |
| [*gluQuadricCallback*](gluquadric.md)                 | Associa un callback a un oggetto quadrica per la gestione degli errori. |
| [**gluQuadricNormals**](gluquadricnormals.md)         | Specifica i normali: nessun normale, uno per volto o uno per vertice.  |
| [**gluQuadricOrientation**](gluquadricorientation.md) | Specifica la direzione dei normali: verso l'esterno o verso l'interno.               |
| [**gluQuadricTexture**](gluquadrictexture.md)         | Attiva o disattiva la generazione della coordinata della trama.                   |
| [**gluQuadricDrawstyle**](gluquadricdrawstyle.md)     | Specifica lo stile di disegno: poligoni, linee, punti e così via.     |
| [**gluSphere**](glusphere.md)                         | Disegna una sfera.                                                  |
| [**gluCylinder**](glucylinder.md)                     | Disegna un cilindro o un cono.                                        |
| [**gluPartialDisk**](glupartialdisk.md)               | Disegna un arco.                                                    |
| [**gluDisk**](gludisk.md)                             | Disegna un cerchio o un disco.                                          |



 

È possibile usare un oggetto quadrica per tutti quadriche di cui si vuole eseguire il rendering in modo analogo. Nell'esempio di codice seguente vengono usati due oggetti quadrica per creare quattro quadriche, due dei quali con trama.


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 





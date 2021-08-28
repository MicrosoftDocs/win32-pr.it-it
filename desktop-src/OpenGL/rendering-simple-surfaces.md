---
title: Rendering di superfici semplici
description: La libreria GLU include un set di funzioni per il disegno di varie superfici semplici (sphere, cilindri, dischi e parti di dischi) in un'ampia gamma di stili e orientamenti. Queste funzioni sono descritte in dettaglio nel manuale di riferimento di OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilità OpenGL (GLU), superfici semplici
- GLU (Utilità OpenGL), superfici semplici
- superfici semplici OpenGL
- Utilità OpenGL (GLU), spheres
- GLU (utilità OpenGL), spheres
- Spheres OpenGL
- Utilità OpenGL (GLU), cilindri
- GLU (Utilità OpenGL), cilindri
- cilindri OpenGL
- Utilità OpenGL (GLU), dischi
- GLU (utilità OpenGL),dischi
- dischi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4010a9cc1c0cfac58f1a99572ebae43233dce552237c17f42d66cc1c50013986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776831"
---
# <a name="rendering-simple-surfaces"></a>Rendering di superfici semplici

La libreria GLU include un set di funzioni per il disegno di varie superfici semplici (sphere, cilindri, dischi e parti di dischi) in un'ampia gamma di stili e orientamenti. Queste funzioni sono descritte in dettaglio nel manuale *di riferimento di OpenGL.*

**Per eseguire il rendering di superfici semplici**

1.  Creare un oggetto quadric con [**gluNewQuadric**](glunewquadric.md).

    Per eliminare questo oggetto al termine, usare [**gluDeleteQuadric**](gludeletequadric.md).

2.  Specificare lo stile di rendering desiderato, come elencato di seguito, con la funzione appropriata (a meno che non si sia soddisfatti dei valori predefiniti):
    -   Se devono essere generate normali di superficie e, in tal caso, se deve essere presente una normale per vertice o una normale per ogni [ **viso: gluQuadricNormals**](gluquadricnormals.md)
    -   Se devono essere generate le coordinate della trama: [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Quale lato del quadric deve essere considerato esterno e quale all'interno: [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Indica se il quadric deve essere disegnato come un set di poligoni, linee o punti: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Dopo aver specificato lo stile di rendering, richiamare la funzione di rendering per il tipo desiderato di oggetto quadric: [**gluSphere,**](glusphere.md) [**gluCylinder,**](glucylinder.md) [**gluDisk**](gludisk.md)o [**gluPartialDisk.**](glupartialdisk.md)

    Se si verifica un errore durante il rendering, viene richiamata la funzione di gestione degli errori specificata con [*gluQuadricCallBack.*](gluquadric.md)

Usare gli argomenti *\* Radius*, *height* e simili, anziché la funzione [**glScale,**](glscale.md) per ridimensionare i quadric, in modo che non sia necessario rinormalizzare le normali di lunghezza unità generate. Per forzare i calcoli di illuminazione a una granularità più fine,  soprattutto  se la specularità del materiale è elevata, impostare i cicli e impilare gli argomenti su valori diversi da 1.

 

 





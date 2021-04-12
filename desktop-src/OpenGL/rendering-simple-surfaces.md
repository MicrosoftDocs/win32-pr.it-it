---
title: Rendering di superfici semplici
description: La libreria GLU include un set di funzioni per il disegno di varie superfici semplici (sfere, cilindri, dischi e parti dei dischi) in diversi stili e orientamenti. Queste funzioni sono descritte in dettaglio nel manuale di riferimento di OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilità OpenGL (GLU), superfici semplici
- GLU (utilità OpenGL), superfici semplici
- OpenGL con superfici semplici
- Utilità OpenGL (GLU), sfere
- GLU (utilità OpenGL), sfere
- sfere OpenGL
- Utilità OpenGL (GLU), cilindri
- GLU (utilità OpenGL), cilindri
- cilindri OpenGL
- Utilità OpenGL (GLU), dischi
- GLU (utilità OpenGL), dischi
- dischi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396934"
---
# <a name="rendering-simple-surfaces"></a>Rendering di superfici semplici

La libreria GLU include un set di funzioni per il disegno di varie superfici semplici (sfere, cilindri, dischi e parti dei dischi) in diversi stili e orientamenti. Queste funzioni sono descritte in dettaglio nel *Manuale di riferimento di OpenGL*.

**Per eseguire il rendering di superfici semplici**

1.  Creare un oggetto quadrica con [**gluNewQuadric**](glunewquadric.md).

    Per eliminare definitivamente l'oggetto al termine dell'operazione, usare [**gluDeleteQuadric**](gludeletequadric.md).

2.  Specificare lo stile di rendering desiderato, come elencato di seguito, con la funzione appropriata (a meno che non si siano soddisfatti i valori predefiniti):
    -   Indica se devono essere generate le normalità della superficie e, in tal caso, se deve essere presente una normale per ogni vertice o una normale per ogni volto: [ **gluQuadricNormals**](gluquadricnormals.md)
    -   Indica se devono essere generate le coordinate di trama: [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Quale lato di quadrica deve essere considerato l'esterno e il quale l'interno: [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Indica se il quadrica deve essere disegnato come un set di poligoni, linee o punti: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Dopo aver specificato lo stile di rendering, richiamare la funzione di rendering per il tipo desiderato di oggetto quadrica: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)o [**gluPartialDisk**](glupartialdisk.md).

    Se si verifica un errore durante il rendering, viene richiamata la funzione di gestione degli errori specificata con [*gluQuadricCallBack*](gluquadric.md) .

Usare gli argomenti *\* RADIUS*, *Height* e simili, anziché la funzione [**glScale**](glscale.md) , per ridimensionare il quadriche, in modo da non dover rinormalizzare le normali di lunghezza dell'unità generate. Per forzare i calcoli di illuminazione a una granularità più fine, soprattutto se la specularità del materiale è elevata, impostare gli argomenti *Loops* e *Stacks* su valori diversi da 1.

 

 





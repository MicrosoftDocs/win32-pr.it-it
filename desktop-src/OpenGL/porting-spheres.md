---
title: Portabilità di sphere
description: Quando si esegue il porting di sphere in OpenGL, tenere presente quanto segue
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Portabilità IRIS GL, spheres
- porting from IRIS GL,spheres
- porting to OpenGL from IRIS GL,spheres
- Portabilità OpenGL da IRIS GL, spheres
- funzioni di disegno, sphere
- Sfere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1e0666393e923767d342d215622e0ed58bfa7b1b620e045a0054b31918a7a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358310"
---
# <a name="porting-spheres"></a>Portabilità di sphere

Quando si esegue il porting di sphere in OpenGL, tenere presente quanto segue:

-   Non è possibile controllare il tipo di primitive usate per disegnare la sfera. È possibile controllare la precisione del disegno in un altro modo: usare i parametri slices e stacks. Le sezioni sono longitudinali; Gli stack sono di tipo latitudiale.
-   Le sphere vengono disegnate al centro dell'origine. Invece di specificare la posizione, come si fa con la funzione **Sphdraw** IRIS GL, precedere una chiamata alla funzione GLU [**gluSphere**](glusphere.md) con una traslazione.
-   La libreria sphere non è ancora disponibile per OpenGL.

La tabella seguente elenca le funzioni IRIS GL per disegnare le sphere e le funzioni GLU equivalenti, se disponibili.



| Funzione GL IRIS | Funzione GLU                                 | Significato                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Crea un nuovo oggetto sphere.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Elimina l'oggetto sphere e la memoria libera usata.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Disegna una sfera.                               |
| **sphmode**      |                                              | Imposta gli attributi della sfera.                       |
| **sphrotmatrix** |                                              | Controlla l'orientamento della sfera.                  |
| **sphgnpolys**   |                                              | Restituisce il numero di poligoni nella sfera corrente. |



 

??

 

 





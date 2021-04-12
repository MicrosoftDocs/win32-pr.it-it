---
title: Porting di sfere
description: Quando si trasferiscono le sfere a OpenGL, tenere presenti i punti seguenti
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Porting di IRIS GL, sfere
- porting da IRIS GL, sfere
- porting in OpenGL da IRIS GL, sfere
- Porting OpenGL da IRIS GL, sfere
- funzioni di disegno, sfere
- sfere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396326"
---
# <a name="porting-spheres"></a>Porting di sfere

Quando si trasferiscono le sfere a OpenGL, tenere presente quanto segue:

-   Non è possibile controllare il tipo di primitive usato per creare la sfera. È possibile controllare la precisione del disegno in un altro modo: usare i parametri slices e stacks. Le sezioni sono longitudinali; gli stack sono latitudinali.
-   Le sfere vengono disegnate al centro dell'origine. Anziché specificare il percorso, come avviene con la funzione **sphdraw** di Iris GL, prima di una chiamata alla funzione Glu [**gluSphere**](glusphere.md) con una traduzione.
-   La libreria Sphere non è ancora disponibile per OpenGL.

La tabella seguente elenca le funzioni di IRIS GL per la creazione di sfere e le relative funzioni GLU equivalenti, ove disponibili.



| Funzione IRIS GL | GLU (funzione)                                 | Significato                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Crea un nuovo oggetto Sphere.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Elimina l'oggetto Sphere e la memoria libera utilizzata.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Disegna una sfera.                               |
| **sphmode**      |                                              | Imposta gli attributi della sfera.                       |
| **sphrotmatrix** |                                              | Controlla l'orientamento della sfera.                  |
| **sphgnpolys**   |                                              | Restituisce il numero di poligoni nella sfera corrente. |



 

??

 

 





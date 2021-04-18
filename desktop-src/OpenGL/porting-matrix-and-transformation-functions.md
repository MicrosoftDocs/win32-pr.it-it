---
title: Porting di matrici e funzioni di trasformazione
description: IRIS GL e OpenGL gestiscono matrici e trasformazioni in modo analogo.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Porting di IRIS GL, matrici
- porting da IRIS GL, matrici
- porting in OpenGL da IRIS GL, matrici
- Porting OpenGL da IRIS GL, matrici
- matrici
- Porting, trasformazioni di IRIS GL
- porting da IRIS GL, trasformazioni
- porting in OpenGL da IRIS GL, trasformazioni
- Porting OpenGL da IRIS GL, trasformazioni
- trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331015"
---
# <a name="porting-matrix-and-transformation-functions"></a>Porting di matrici e funzioni di trasformazione

IRIS GL e OpenGL gestiscono matrici e trasformazioni in modo analogo. Esistono tuttavia diverse differenze da tenere presenti quando si porta il codice da IRIS GL:

-   In OpenGL si è sempre in modalità a doppia matrice; non esiste alcuna modalità a matrice singola.
-   Gli angoli sono misurati in gradi, anziché decimi di gradi.
-   Le chiamate della matrice di proiezione, ad esempio [**glFrustum**](glfrustum.md) e [**glOrtho**](glortho.md), ora si moltiplicano per la matrice corrente anziché essere caricate nella matrice corrente.
-   La funzione OpenGL, [**glRotate**](glrotate.md), è molto diversa da **ruotare**. È possibile ruotare intorno a qualsiasi asse arbitrario, anziché essere limitato agli assi x, y e z. Ad esempio, è possibile tradurre:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    in:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Quando si esegue la conversione da **ruota** a **glRotate** , si passa a gradi da decimi di gradi e si sostituisce "z" con un vettore per l'asse z.

-   OpenGL non è equivalente alla funzione **PolarView** . È possibile sostituirlo facilmente con una traduzione e tre rotazioni. Ad esempio, è possibile tradurre:

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    in:

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

La tabella seguente elenca le funzioni di matrice OpenGL e le rispettive funzioni di IRIS GL equivalenti.



| Funzione IRIS GL              | OpenGL (funzione)                                                                        | Significato                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mMode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Imposta la modalità della matrice corrente.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Sostituisce la matrice corrente con la matrice di identità.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Sostituisce la matrice corrente con la matrice specificata.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Post-moltiplica la matrice corrente con la matrice specificata (si noti che **multmatrix** è pre-moltiplicato).                                                                            |
| **MAPW**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Proietta le coordinate dello spazio globale nello spazio degli oggetti (vedere anche [**gluProject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glOrtho**](glortho.md)                                                             | Moltiplica la matrice corrente per una matrice di proiezione ortogonale.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Definisce una matrice di proiezione ortogonale bidimensionale.                                                                                                                      |
| **prospettiva**               | [**gluPerspective**](gluperspective.md)                                               | Definisce una matrice di proiezione prospettica.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Definisce un'area di selezione.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Estrae lo stack della matrice corrente, sostituendo la matrice corrente con quello sottostante.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Esegue il push dello stack di matrici corrente di uno, duplicando la matrice corrente.                                                                                                       |
| **ruota**,**Rot**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Ruota il sistema di coordinate corrente in base all'angolo specificato sul vettore dall'origine fino al punto specificato. Si noti che la **rotazione** ruotata riguarda solo gli assi x, y e z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Moltiplica la matrice corrente per una matrice di scala.                                                                                                                                 |
| **Traduci**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Sposta l'origine del sistema di coordinate nel punto specificato, moltiplicando la matrice corrente con una matrice di traslazione.                                                              |
| **finestra**                    | [**glFrustum**](glfrustum.md)                                                         | Date le coordinate per i piani di ritaglio, moltiplica la matrice corrente in base a una matrice di prospettive.                                                                                  |



 

OpenGL dispone di tre modalità Matrix, che vengono impostate con [**glMatrixMode**](glmatrixmode.md). Nella tabella seguente sono elencate le modalità disponibili come parametri per **glMatrixMode**.



| Modalità matrice GL IRIS | Modalità OpenGL    | Significato                                  | Profondità dello stack minima |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | \_trama GL    | Opera sullo stack della matrice di trame.    | 2               |
| **MVIEWING**        | \_MODELVIEW GL  | Opera nello stack della matrice della vista del modello. | 32              |
| **MPROJECTION**     | \_proiezione GL | Opera sullo stack della matrice di proiezione. | 2               |



 

 

 






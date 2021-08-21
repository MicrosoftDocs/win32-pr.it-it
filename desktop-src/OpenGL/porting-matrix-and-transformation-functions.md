---
title: Funzioni di trasformazione e matrice di porting
description: IRIS GL e OpenGL gestiscono matrici e trasformazioni in modo simile.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- porting IRIS GL, matrici
- porting da IRIS GL, matrici
- porting in OpenGL da IRIS GL, matrici
- Porting OpenGL da IRIS GL, matrici
- matrici
- porting IRIS GL, trasformazioni
- porting da IRIS GL, trasformazioni
- porting in OpenGL da IRIS GL, trasformazioni
- Porting OpenGL da IRIS GL, trasformazioni
- trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e2dc0ed6b53f3a2ee5ef5310369b734a58cba27481b8b478eef63fdfe5722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132603"
---
# <a name="porting-matrix-and-transformation-functions"></a>Funzioni di trasformazione e matrice di porting

IRIS GL e OpenGL gestiscono matrici e trasformazioni in modo simile. Esistono tuttavia diverse differenze da tenere presenti quando si esegue il porting del codice da IRIS GL:

-   In OpenGL si è sempre in modalità a matrice doppia. non esiste alcuna modalità a matrice singola.
-   Gli angoli vengono misurati in gradi, anziché decimi di gradi.
-   Le chiamate alla matrice di proiezione, ad esempio [**glFrustum**](glfrustum.md) e [**glOrtho**](glortho.md), ora si moltiplicano nella matrice corrente, anziché essere caricate nella matrice corrente.
-   La funzione OpenGL, [**glRotate,**](glrotate.md)è molto diversa da **rotate**. È possibile ruotare intorno a qualsiasi asse arbitrario, anziché limitarsi agli assi x, y e z. Ad esempio, è possibile tradurre:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    in:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Quando si traduce da **rotate** a **glRotate** si passa a gradi da decimi di gradi e si sostituisce 'z' con un vettore per l'asse z.

-   OpenGL non ha alcun equivalente alla **funzione polarview.** È possibile sostituirlo facilmente con una traslazione e tre rotazioni. Ad esempio, è possibile tradurre:

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

    

Nella tabella seguente sono elencate le funzioni di matrice OpenGL e le funzioni IRIS GL equivalenti.



| Funzione GL IRIS              | Funzione OpenGL                                                                        | Significato                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Imposta la modalità matrice corrente.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Sostituisce la matrice corrente con la matrice di identità.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Sostituisce la matrice corrente con la matrice specificata.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Moltiplica la matrice corrente con la matrice specificata (si noti che **multmatrix** è pre-moltiplicata).                                                                            |
| **mapw**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Proietta le coordinate dello spazio del mondo nello spazio oggetti (vedere anche [**gluProject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glOrtho**](glortho.md)                                                             | Moltiplica la matrice corrente per una matrice di proiezione ortografica.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Definisce una matrice di proiezione ortografica bidimensionale.                                                                                                                      |
| **Prospettiva**               | [**gluPerspective**](gluperspective.md)                                               | Definisce una matrice di proiezione prospettica.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Definisce un'area di selezione.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Popola lo stack di matrici corrente, sostituendo la matrice corrente con quella sottostante.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Inserisce lo stack della matrice corrente verso il basso di uno, duplicando la matrice corrente.                                                                                                       |
| **ruotare**,**marcire**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Ruota il sistema di coordinate corrente in base all'angolo specificato intorno al vettore dall'origine al punto specificato. Si noti **che** la rotazione è stata ruotata solo sugli assi x, y e z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Moltiplica la matrice corrente per una matrice di ridimensionamento.                                                                                                                                 |
| **Traduci**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Sposta l'origine del sistema di coordinate nel punto specificato moltiplicando la matrice corrente per una matrice di traslazione.                                                              |
| **Finestra**                    | [**glFrustum**](glfrustum.md)                                                         | Date le coordinate per i piani di ritaglio, moltiplica la matrice corrente per una matrice prospettica.                                                                                  |



 

OpenGL ha tre modalità matrice, impostate con [**glMatrixMode**](glmatrixmode.md). Nella tabella seguente sono elencate le modalità disponibili come parametri **per glMatrixMode**.



| Modalità matrice GL IRIS | Modalità OpenGL    | Significato                                  | Profondità minima dello stack |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | TRAMA \_ GL    | Opera sullo stack della matrice di trame.    | 2               |
| **VISUALIZZAZIONE MVIEWING**        | GL \_ MODELVIEW  | Opera sullo stack della matrice di visualizzazione del modello. | 32              |
| **MPROJECTION**     | PROIEZIONE GL \_ | Opera sullo stack della matrice di proiezione. | 2               |



 

 

 






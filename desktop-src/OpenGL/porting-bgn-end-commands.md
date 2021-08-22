---
title: Porting di comandi bgn/end
description: IRIS GL usa il paradigma begin/end, ma ha una funzione diversa per ogni primitiva grafica.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Porting IRIS GL, comandi bgn/end
- porting da IRIS GL, comandi bgn/end
- porting a OpenGL da IRIS GL, comandi bgn/end
- Porting OpenGL da IRIS GL, comandi bgn/end
- funzioni di disegno, comandi bgn/end
- Comandi bgn/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63084b1f05d984fdc19254edaadaca9098d13f974a433f5c6ff7c5d370ec223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485971"
---
# <a name="porting-bgnend-commands"></a>Porting di comandi bgn/end

IRIS GL usa il paradigma begin/end, ma ha una funzione diversa per ogni primitiva grafica. Ad esempio, è probabile che si **usino bgnpolygon** e **endpolygon** per disegnare poligoni e **bgnline** e **endline** per disegnare linee. In OpenGL si usa la struttura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) per entrambi. In OpenGL si disegna la maggior parte degli oggetti geometrici racchiudendo una serie di funzioni che specificano vertici, normali, trame e colori tra coppie di **chiamate glBegin** e **glEnd.** Esempio:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

La **funzione glBegin** accetta un singolo parametro che specifica la modalità di disegno e quindi la primitiva. Ecco un esempio di codice OpenGL che disegna un poligono e quindi una linea:

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

Con OpenGL si disegnano oggetti geometrici diversi specificando parametri diversi per [**glBegin**](glbegin.md). Nella tabella seguente sono elencati i parametri **glBegin** di OpenGL che corrispondono alle funzioni gl IRIS equivalenti.



| Funzione GL IRIS  | Valore della modalità glBegin | Significato                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | PUNTI DI \_ RIFERIMENTO            | Singoli punti.                                                                       |
| **bgnline**       | GL \_ LINE \_ STRIP       | Serie di segmenti di linea connessi.                                                       |
| **bgnclosedline** | CICLO GL \_ LINE \_        | Serie di segmenti di linea connessi, con un segmento aggiunto tra il primo e l'ultimo vertice. |
|                   | RIGHE DI \_ CONTABILITÀ GENERALE             | Coppie di vertici interpretate come singoli segmenti di linea.                               |
| **bgnpolygon**    | POLIGONO GL \_           | Limite di un poligono convesso semplice.                                                     |
|                   | TRIANGOLI \_ GL         | Triple di vertici interpretate come triangoli.                                            |
| **bgntmesh**      | TRIANGOLO GL \_ \_ STRIP   | Strisce collegate di triangoli.                                                              |
|                   | VENTOLA \_ TRIANGOLO \_ GL     | Ventole collegate di triangoli.                                                                |
|                   | QUAD \_ GL             | Quadruple di vertici interpretati come quadrilaterali.                                    |
| **bgnqstrip**     | GL \_ QUAD \_ STRIP       | Strisce collegate di quadrilaterali.                                                         |



 

Per una descrizione dettagliata delle differenze tra mesh triangolo, strisce e ventole, vedere [Porting Triangles](porting-triangles.md).

Non esiste alcun limite al numero di vertici che è possibile specificare tra una coppia [**glBegin**](glbegin.md)  /  [**glEnd.**](glend.md)

Oltre a specificare i vertici all'interno di una coppia **glBegin**  /  **glEnd,** è possibile specificare una normale corrente, le coordinate di trama correnti e un colore corrente. Nella tabella seguente sono elencati i comandi validi all'interno di una coppia **glBegin**  /  **glEnd.**



| Funzione GL IRIS        | Funzione OpenGL                                                      | Significato                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2**, **v3**, **v4**  | [glVertex](glvertex-functions.md)                                   | Imposta le coordinate dei vertici.                         |
| **RGBcolor**, **cpack** | [glColor](glcolor-functions.md)                                     | Imposta il colore corrente.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Imposta l'indice dei colori corrente.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Imposta le coordinate normali del vettore.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Valuta le mappe una e bidimensionali abilitate. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Esegue gli elenchi di visualizzazione.                        |
| **t2**                  | [glTexCoord](gltexcoord-functions.md)                               | Imposta le coordinate della trama.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Controlla i bordi di disegno.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Imposta le proprietà del materiale.                        |



 

> [!Note]
>
> Se si usa una funzione OpenGL diversa da quelle elencate nella tabella precedente all'interno di una coppia [**glBegin**](glbegin.md)  /  [**glEnd,**](glend.md) si otterrà risultati imprevedibili o probabilmente un errore.

 

 

 





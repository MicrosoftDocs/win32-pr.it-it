---
title: Porting di comandi BGN/end
description: IRIS GL usa il paradigma begin/end ma ha una funzione diversa per ogni primitiva grafica.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Porting di IRIS GL, comandi BGN/end
- porting da comandi IRIS GL, BGN/end
- porting in OpenGL da IRIS GL, BGN/end Commands
- Porting OpenGL da IRIS GL, comandi BGN/end
- funzioni di disegno, comandi BGN/end
- comandi BGN/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396627"
---
# <a name="porting-bgnend-commands"></a>Porting di comandi BGN/end

IRIS GL usa il paradigma begin/end ma ha una funzione diversa per ogni primitiva grafica. È possibile, ad esempio, usare **bgnpolygon** e **endpolygon** per creare poligoni, **bgnline** e **EndLine** per creare linee. In OpenGL si usa la struttura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) per entrambi. In OpenGL è possibile creare la maggior parte degli oggetti geometrici racchiudendo una serie di funzioni che specificano i vertici, le normali, le trame e i colori tra le coppie di **glBegin** e le chiamate **glEnd** . Ad esempio:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

La funzione **glBegin** accetta un singolo parametro che specifica la modalità di disegno e quindi la primitiva. Ecco un esempio di codice OpenGL che disegna un poligono e una riga:

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

Con OpenGL è possibile creare oggetti geometrici diversi specificando parametri diversi per [**glBegin**](glbegin.md). La tabella seguente elenca i parametri OpenGL **glBegin** che corrispondono alle funzioni di Iris GL equivalenti.



| Funzione IRIS GL  | Valore della modalità glBegin | Significato                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | \_punti GL            | Punti singoli.                                                                       |
| **bgnline**       | \_striscia linea \_ GL       | Serie di segmenti di linea collegati.                                                       |
| **bgnclosedline** | \_ciclo linea \_ GL        | Serie di segmenti di linea collegati, con un segmento aggiunto tra il primo e l'ultimo vertice. |
|                   | \_righe GL             | Coppie di vertici interpretate come singoli segmenti di linea.                               |
| **bgnpolygon**    | \_poligono GL           | Limite di un poligono convesso semplice.                                                     |
|                   | triangoli GL \_         | Triple di vertici interpretati come triangoli.                                            |
| **bgntmesh**      | \_striscia del triangolo GL \_   | Strisce collegate di triangoli.                                                              |
|                   | \_ventola del triangolo GL \_     | Fan collegati di triangoli.                                                                |
|                   | \_Quad GL             | Quadruple di vertici interpretate come quadrilateri.                                    |
| **bgnqstrip**     | \_ \_ striping GL quad       | Strisce collegate di quadrilateri.                                                         |



 

Per una descrizione dettagliata delle differenze tra le mesh, le strisce e le ventole del triangolo, vedere la sezione relativa ai [triangoli di porting](porting-triangles.md).

Non esiste alcun limite al numero di vertici che è possibile specificare tra una coppia [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) .

Oltre a specificare i vertici all'interno di una coppia **glBegin**  /  **glEnd** , è possibile specificare un normale corrente, coordinate di trama correnti e un colore corrente. La tabella seguente elenca i comandi validi all'interno di una coppia **glBegin**  /  **glEnd** .



| Funzione IRIS GL        | OpenGL (funzione)                                                      | Significato                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2**, **v3**, **V4**  | [glVertex](glvertex-functions.md)                                   | Imposta le coordinate del vertice.                         |
| **RGBcolor**, **CPack** | [glColor](glcolor-functions.md)                                     | Imposta il colore corrente.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Imposta l'indice del colore corrente.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Imposta le normali coordinate del vettore.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Valuta le mappe con una e due dimensioni abilitate. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Esegue gli elenchi di visualizzazione.                        |
| **T2**                  | [glTexCoord](gltexcoord-functions.md)                               | Imposta le coordinate di trama.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Controlla i bordi del disegno.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Imposta le proprietà del materiale.                        |



 

> [!Note]
>
> Se si usa una funzione OpenGL diversa da quelle elencate nella tabella precedente all'interno di una coppia [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) , si otterranno risultati imprevedibili o probabilmente un errore.

 

 

 





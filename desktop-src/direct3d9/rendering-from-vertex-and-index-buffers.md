---
description: Sia i metodi di disegno indicizzati che i metodi di disegno non indicizzati sono supportati da Direct3D.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendering da vertex e buffer di indice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4290dc2ff40e1ec0448e3948342aa3b02ac62bf9866a44958ea53bee9658d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092628"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Rendering da vertex e buffer di indice (Direct3D 9)

Sia i metodi di disegno indicizzati che i metodi di disegno non indicizzati sono supportati da Direct3D. I metodi indicizzati usano un singolo set di indici per tutti i componenti dei vertici. I dati dei vertici vengono archiviati nei vertex buffer e i dati dell'indice vengono archiviati nei buffer di indice. Di seguito sono elencati alcuni scenari comuni per il disegno di primitive tramite vertex e buffer di indice.

Questi esempi confrontano l'uso di [**IDirect3DDevice9::D rawPrimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Scenario 1: Disegno di due triangoli senza indicizzazione

Si immagini di voler disegnare il quad mostrato nella figura seguente.

![illustrazione di un quadrato costituito da due triangoli](images/dip-fig1.png)

Se si usa il tipo primitivo Elenco triangoli per eseguire il rendering dei due triangoli, ogni triangolo verrà archiviato come 3 singoli vertici, con un buffer dei vertici simile a quello illustrato nella figura seguente.

![diagramma di un vertex buffer che definisce tre vertici per due triangoli](images/dip-fig2.png)

La chiamata di disegno è molto semplice. a partire dalla posizione 0 all'interno del vertex buffer, disegnare due triangoli. Se l'culling è abilitato, l'ordine dei vertici sarà importante. Questo esempio presuppone lo stato di culling in senso antiorario predefinito, quindi i triangoli visibili devono essere disegnati in senso orario. Il tipo primitivo Triangle List legge semplicemente tre vertici in ordine lineare dal buffer per ogni triangolo, quindi questa chiamata disegna triangoli (0, 1, 2) e (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Scenario 2: Disegno di due triangoli con indicizzazione

Come si noterà, il vertex buffer contiene dati duplicati nelle posizioni 0 e 4, 2 e 5. Ciò ha senso perché i due triangoli condividono due vertici comuni. Questi dati duplicati sono uno spreco e il buffer dei vertici può essere compresso usando un index buffer. Un buffer dei vertici più piccolo riduce la quantità di dati dei vertici che devono essere inviati all'adattatore grafico. Ancora più importante, l'uso di un index buffer consente all'adapter di archiviare i vertici in una cache dei vertici; se la primitiva disegnata contiene un vertice usato di recente, tale vertice può essere recuperato dalla cache anziché leggerlo dal vertex buffer, con un significativo aumento delle prestazioni.

Un index buffer 'indici' nel vertex buffer, quindi ogni vertice univoco deve essere archiviato una sola volta nel vertex buffer. Il diagramma seguente illustra un approccio indicizzato allo scenario di disegno precedente.

![diagramma di un index buffer per il vertex buffer precedente](images/dip-fig3.png)

Il index buffer archivia VB di indice, che fanno riferimento a un vertice specifico all'interno del vertex buffer. Un vertex buffer può essere pensato come una matrice di vertici, quindi VB Index è semplicemente l'indice nel vertex buffer per il vertice di destinazione. Analogamente, un indice IB è un indice nel index buffer. Ciò può generare molto confusione molto rapidamente se non si è attento, quindi assicurarsi di avere chiaro il vocabolario usato: indice dei valori di indice VB nel vertex buffer, indice dei valori di indice IB nel index buffer e index buffer stesso archivia i valori di indice VB.

La chiamata di disegno è illustrata di seguito. I significati di tutti gli argomenti vengono discussi a lungo per lo scenario di disegno successivo. Per il momento, è sufficiente notare che questa chiamata indica nuovamente a Direct3D di eseguire il rendering di un elenco di triangoli contenente due triangoli, a partire dalla posizione 0 all'interno del index buffer. Questa chiamata disegna gli stessi due triangoli nello stesso ordine di prima, assicurando un orientamento in senso orario appropriato:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Scenario 3: Disegno di un triangolo con indicizzazione

Fingere ora di voler disegnare solo il secondo triangolo, ma di voler usare lo stesso vertex buffer e lo stesso index buffer usati per disegnare l'intero quad, come illustrato nel diagramma seguente.

![diagramma del buffer index buffer e dei vertici per il secondo triangolo](images/dip-fig4.png)

Per questa chiamata di disegno, il primo indice IB usato è 3; questo valore è denominato StartIndex. L'indice VB usato è 0. Questo valore è denominato MinIndex. Anche se sono necessari solo tre vertici per disegnare il triangolo, questi tre vertici vengono distribuiti in quattro posizioni adiacenti nel buffer dei vertici. Il numero di posizioni all'interno del blocco contiguo di memoria del vertex buffer richiesto per la chiamata di disegno è denominato NumVertices e verrà impostato su 4 in questa chiamata. I valori MinIndex e NumVertices sono in realtà solo suggerimenti per consentire a Direct3D di ottimizzare l'accesso alla memoria durante l'elaborazione dei vertici software e possono essere semplicemente impostati per includere l'intero vertex buffer al prezzo delle prestazioni.

Ecco la chiamata di disegno per il caso a triangolo singolo. Il significato dell'argomento BaseVertexIndex verrà spiegato successivamente:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Scenario 4: Disegno di un triangolo con indicizzazione offset

BaseVertexIndex è un valore che viene aggiunto in modo efficace a ogni indice VB archiviato nel index buffer. Ad esempio, se fosse stato passato un valore pari a 50 per BaseVertexIndex durante la chiamata precedente, funzionalmente sarebbe uguale all'uso del index buffer nel diagramma seguente per la durata della chiamata DrawIndexedPrimitive:

![diagramma di un index buffer con valore 50 per basevertexindex](images/dip-fig5.png)

Questo valore viene raramente impostato su un valore diverso da 0, ma può essere utile se si vuole separare il index buffer dal vertex buffer: se quando si compila il index buffer per una mesh specifica la posizione della mesh all'interno del buffer dei vertici non è ancora nota, è sufficiente far finta che i vertici della mesh si trovino all'inizio del buffer dei vertici. Quando arriva il momento di effettuare la chiamata di disegno, è sufficiente passare la posizione iniziale effettiva come BaseVertexIndex.

Questa tecnica può essere usata anche quando si disegnano più istanze di una mesh usando una singola index buffer; Ad esempio, se il vertex buffer conteneva due mesh con un ordine di disegno identico ma vertici leggermente diversi (ad esempio colori diffusi o coordinate di trama diversi), entrambe le mesh potrebbero essere disegnate usando valori diversi per BaseVertexIndex. Per approfondire questo concetto, è possibile usare un index buffer per disegnare più istanze di una mesh, ognuna contenuta in un buffer dei vertici diverso, semplicemente ciclicando il buffer dei vertici attivo e modificando BaseVertexIndex in base alle esigenze. Si noti che anche il valore BaseVertexIndex viene aggiunto automaticamente all'argomento MinIndex, che ha senso quando si vede come viene usato:

Fingere ora che si voglia disegnare di nuovo solo il secondo triangolo del quad usando lo stesso index buffer precedente; Tuttavia, viene usato un altro vertex buffer in cui il quad si trova in corrispondenza VB Index 50. L'ordine relativo dei quattro vertici rimane invariato, ma solo la posizione iniziale all'interno del vertex buffer è diversa. Il index buffer e il vertex buffer sono simili al diagramma seguente.

![diagramma dell'index buffer e del vertex buffer con indice vb di 50](images/dip-fig6.png)

Ecco la chiamata di disegno appropriata. Si noti che BaseVertexIndex è l'unico valore modificato rispetto allo scenario precedente:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di rendering](rendering-primitives.md)
</dt> </dl>

 

 

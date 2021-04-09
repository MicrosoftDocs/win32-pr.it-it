---
description: I metodi di disegno indicizzati e non indicizzati sono supportati da Direct3D.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendering dai buffer di Vertex e index (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876189"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Rendering dai buffer di Vertex e index (Direct3D 9)

I metodi di disegno indicizzati e non indicizzati sono supportati da Direct3D. I metodi indicizzati utilizzano un singolo set di indici per tutti i componenti dei vertici. I dati dei vertici vengono archiviati nei buffer dei vertici e i dati dell'indice vengono archiviati nei buffer di indice. Di seguito sono elencati alcuni scenari comuni per la creazione di primitive mediante i buffer di Vertex e di indice.

In questi esempi viene confrontato l'uso di [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Scenario 1: disegno di due triangoli senza indicizzazione

Si immagini di voler creare il quad illustrato nella figura seguente.

![illustrazione di un quadrato costituito da due triangoli](images/dip-fig1.png)

Se si usa il tipo primitivo elenco di triangolo per eseguire il rendering dei due triangoli, ogni triangolo verrà archiviato come 3 singoli vertici, ottenendo così un buffer di vertice simile a quello riportato nella figura seguente.

![diagramma di un buffer vertex che definisce tre vertici per due triangoli](images/dip-fig2.png)

La chiamata di disegno è molto semplice; a partire dalla posizione 0 all'interno del buffer dei vertici, creare due triangoli. Se l'eliminazione è abilitata, l'ordine dei vertici sarà importante. Questo esempio presuppone lo stato di eliminazione in senso antiorario predefinito, quindi i triangoli visibili devono essere disegnati in ordine orario. Il tipo primitivo dell'elenco di triangolo legge solo tre vertici in ordine lineare dal buffer per ogni triangolo, quindi questa chiamata trarrà triangoli (0, 1, 2) e (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Scenario 2: disegno di due triangoli con indicizzazione

Come si noterà, il buffer dei vertici contiene dati duplicati in posizioni 0 e 4, 2 e 5. Questo ha senso perché i due triangoli condividono due vertici comuni. Questi dati duplicati sono inutili e il buffer dei vertici può essere compresso usando un buffer di indice. Un buffer di vertice più piccolo riduce la quantità di dati dei vertici da inviare alla scheda grafica. Ancora più importante, l'uso di un buffer di indice consente all'adapter di archiviare i vertici in una cache dei vertici; Se la primitiva disegnata contiene un vertice usato di recente, è possibile recuperare tale vertice dalla cache anziché leggerlo dal buffer dei vertici, il che comporta un notevole aumento delle prestazioni.

Un buffer di indice ' Indexes ' nel buffer dei vertici, in modo che ogni vertice univoco debba essere archiviato una sola volta nel buffer dei vertici. Il diagramma seguente illustra un approccio indicizzato allo scenario di disegno precedente.

![diagramma di un buffer di indice per il buffer vertex precedente](images/dip-fig3.png)

Il buffer index archivia i valori di indice VB, che fanno riferimento a un vertice specifico all'interno del buffer del vertice. Un buffer vertex può essere considerato come una matrice di vertici, quindi l'indice VB è semplicemente l'indice nel buffer dei vertici per il vertice di destinazione. Analogamente, un indice IB è un indice nel buffer di indice. Questa operazione può risultare molto confusa molto rapidamente se non si è attenti, quindi assicurarsi di essere in grado di usare il vocabolario: Indice dei valori di indice VB nel buffer dei vertici, indice dei valori di indice IB nel buffer di indice e il buffer di indice stesso archivia i valori di indice VB.

La chiamata di disegno è illustrata di seguito. Il significato di tutti gli argomenti viene discusso a lungo per lo scenario di disegno successivo. per il momento, è sufficiente tenere presente che questa chiamata indica a Direct3D di eseguire il rendering di un elenco di triangolo contenente due triangoli, a partire dalla posizione 0 all'interno del buffer dell'indice. Questa chiamata attirerà gli stessi due triangoli nello stesso ordine di prima, assicurando un corretto orientamento in senso orario:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Scenario 3: disegno di un triangolo con indicizzazione

Si supponga ora di voler disegnare solo il secondo triangolo, ma si vuole usare lo stesso buffer di vertex buffer e indice usato durante il disegno dell'intero quad, come illustrato nella figura seguente.

![diagramma del buffer di indice e del vertex buffer per il secondo triangolo](images/dip-fig4.png)

Per questa chiamata di disegno, il primo indice IB usato è 3; Questo valore è denominato StartIndex. L'indice VB più basso utilizzato è 0. Questo valore è denominato MinIndex. Sebbene siano necessari solo tre vertici per creare il triangolo, questi tre vertici vengono distribuiti in quattro posizioni adiacenti nel buffer dei vertici; il numero di posizioni all'interno del blocco contiguo della memoria del buffer dei vertici richiesto per la chiamata di disegno è denominato NumVertices e verrà impostato su 4 in questa chiamata. I valori MinIndex e NumVertices sono semplicemente suggerimenti per consentire a Direct3D di ottimizzare l'accesso alla memoria durante l'elaborazione dei vertici software e possono semplicemente essere impostati per includere l'intero buffer di vertex al prezzo delle prestazioni.

Di seguito è illustrata la chiamata di disegno per il singolo caso di triangolo. il significato dell'argomento BaseVertexIndex verrà illustrato di seguito:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Scenario 4: disegno di un triangolo con indicizzazione offset

BaseVertexIndex è un valore che viene effettivamente aggiunto a ogni indice VB archiviato nel buffer dell'indice. Se, ad esempio, è stato passato un valore di 50 per BaseVertexIndex durante la chiamata precedente, che sarebbe funzionalmente uguale all'uso del buffer di indice nel diagramma seguente per la durata della chiamata DrawIndexedPrimitive:

![diagramma di un buffer di indice con un valore di 50 per basevertexindex](images/dip-fig5.png)

Questo valore viene raramente impostato su un valore diverso da 0, ma può essere utile se si desidera separare il buffer dell'indice dal buffer vertex: se quando si compila il buffer di indice per una mesh particolare, la posizione della mesh nel buffer dei vertici non è ancora nota, è possibile semplicemente fingere che i vertici della mesh si trovino all'inizio del buffer dei vertici; Quando si tratta di eseguire la chiamata di progetto, è sufficiente passare la posizione iniziale effettiva come BaseVertexIndex.

Questa tecnica può essere usata anche quando si disegnano più istanze di una mesh usando un singolo buffer di indice; Se, ad esempio, il buffer dei vertici conteneva due mesh con un ordine di disegno identico ma vertici leggermente diversi (probabilmente diversi colori diffusi o coordinate di trama), entrambe le mesh potevano essere disegnate usando valori diversi per BaseVertexIndex. Considerando questo concetto, è possibile usare un buffer di indice per creare più istanze di una mesh, ciascuna contenuta in un buffer vertex diverso, semplicemente ciclando il buffer dei vertici attivo e modificando il BaseVertexIndex in base alle esigenze. Si noti che anche il valore BaseVertexIndex viene aggiunto automaticamente all'argomento MinIndex, che ha senso quando viene visualizzato il modo in cui viene usato:

Si supponga ora di voler creare di nuovo il secondo triangolo del Quad usando lo stesso buffer di indice precedente; Tuttavia, viene usato un buffer vertex diverso in cui il quad si trova in corrispondenza dell'indice VB 50. L'ordine relativo dei vertici Quad rimane invariato, ma solo la posizione iniziale all'interno del buffer dei vertici è diversa. Il buffer di indice e il buffer dei vertici avranno un aspetto simile al diagramma seguente.

![diagramma del buffer di indice e del buffer di vertex con indice VB 50](images/dip-fig6.png)

Di seguito è indicata la chiamata di progetto appropriata; Si noti che BaseVertexIndex è l'unico valore che è stato modificato rispetto allo scenario precedente:


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

 

 

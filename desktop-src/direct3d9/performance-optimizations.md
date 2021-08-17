---
description: Ogni sviluppatore che crea applicazioni in tempo reale che usano grafica 3D è interessato all'ottimizzazione delle prestazioni. Questa sezione fornisce linee guida per ottenere le prestazioni migliori dal codice.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Ottimizzazioni delle prestazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e22ff22e3cde3673a1fc5ccd1da1bdccd95c6a094d670f59742178b28954773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520428"
---
# <a name="performance-optimizations-direct3d-9"></a>Ottimizzazioni delle prestazioni (Direct3D 9)

Ogni sviluppatore che crea applicazioni in tempo reale che usano grafica 3D è interessato all'ottimizzazione delle prestazioni. Questa sezione fornisce linee guida per ottenere le prestazioni migliori dal codice.

-   [Prestazioni generali Suggerimenti](#general-performance-tips)
-   [Database ed Culling](#databases-and-culling)
-   [Primitive di invio in batch](#batching-primitives)
-   [Illuminazione Suggerimenti](#lighting-tips)
-   [Dimensioni trama](#texture-size)
-   [Trasformazioni con matrice](#matrix-transforms)
-   [Uso di trame dinamiche](#using-dynamic-textures)
-   [Uso dei vertici dinamici e dei buffer di indice](#using-dynamic-vertex-and-index-buffers)
-   [Uso delle mesh](#using-meshes)
-   [Prestazioni del buffer Z](#z-buffer-performance)

## <a name="general-performance-tips"></a>Prestazioni generali Suggerimenti

-   Deselezionare solo quando è necessario.
-   Ridurre al minimo le modifiche dello stato e raggruppare le modifiche rimanenti.
-   Usare trame più piccole, se possibile.
-   Disegnare gli oggetti nella scena dalla parte frontale alla parte posteriore.
-   Usare le strisce triangolare al posto di elenchi e ventole. Per ottenere prestazioni ottimali della cache dei vertici, disporre le strisce per riutilizzare i vertici dei triangoli prima, anziché in un secondo momento.
-   Ridurre normalmente gli effetti speciali che richiedono una condivisione sproporzionata delle risorse di sistema.
-   Testare costantemente le prestazioni dell'applicazione.
-   Ridurre al minimo i commutatori del buffer dei vertici.
-   Se possibile, usare buffer di vertici statici.
-   Usare un buffer dei vertici statico di grandi dimensioni per FVF per gli oggetti statici, anziché uno per ogni oggetto.
-   Se l'applicazione richiede l'accesso casuale al vertex buffer nella memoria AGP, scegliere una dimensione del formato dei vertici che sia un multiplo di 32 byte. In caso contrario, selezionare il formato più piccolo appropriato.
-   Disegnare usando primitive indicizzate. Ciò può consentire una memorizzazione nella cache dei vertici più efficiente all'interno dell'hardware.
-   Se il formato del buffer di profondità contiene un canale di stencil, cancellare sempre i canali di profondità e di stencil contemporaneamente.
-   Combinare l'istruzione shader e l'output dei dati, laddove possibile. Esempio:
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Database ed Culling

La creazione di un database affidabile degli oggetti nel mondo è fondamentale per ottenere prestazioni ottimali in Direct3D. È più importante dei miglioramenti alla rasterizzazione o all'hardware.

È consigliabile mantenere il numero di poligoni più basso che è possibile gestire. Progettare per un numero basso di poligoni creando modelli a poligono basso fin dall'inizio. Aggiungere poligoni se è possibile farlo senza compromettere le prestazioni più avanti nel processo di sviluppo. Tenere presente che i poligoni più veloci sono quelli che non si disegnano.

## <a name="batching-primitives"></a>Primitive di invio in batch

Per ottenere prestazioni di rendering ottimali durante l'esecuzione, provare a usare le primitive in batch e mantenere il numero di modifiche dello stato di rendering il più basso possibile. Ad esempio, se si dispone di un oggetto con due trame, raggruppare i triangoli che usano la prima trama e seguirli con lo stato di rendering necessario per modificare la trama. Raggruppare quindi tutti i triangoli che usano la seconda trama. Il supporto hardware più semplice per Direct3D viene chiamato con batch di stati di rendering e batch di primitive tramite il livello di astrazione hardware (HAL). Più efficacemente vengono eseguite le istruzioni in batch, minore è il numero di chiamate HAL eseguite durante l'esecuzione.

## <a name="lighting-tips"></a>Illuminazione Suggerimenti

Poiché le luci aggiungono un costo per vertice a ogni fotogramma sottoposto a rendering, è possibile migliorare significativamente le prestazioni facendo attenzione al modo in cui vengono usate nell'applicazione. La maggior parte dei suggerimenti seguenti deriva dalla massima, "il codice più veloce è il codice che non viene mai chiamato".

-   Usare il numero di sorgenti di luce possibile. Per aumentare il livello di illuminazione complessivo, ad esempio, usare la luce ambientale invece di aggiungere una nuova sorgente di luce.
-   Le luci direzionali sono più efficienti rispetto alle luci punto o ai faretti. Per le luci direzionali, la direzione verso la luce è fissa e non deve essere calcolata in base ai vertici.
-   I faretti possono essere più efficienti rispetto alle luci punto, perché l'area esterna al cono di luce viene calcolata rapidamente. Il fatto che i riflettori siano più efficienti o meno dipende dalla quantità di scena accesa dai riflettori.
-   Usare il parametro range per limitare le luci solo alle parti della scena da illuminare. Tutti i tipi di luce esciranno abbastanza presto quando non sono disponibili.
-   Evidenziazioni speculari quasi il doppio del costo di una luce. Usarli solo quando è necessario. Impostare lo stato di rendering D3DRS \_ SPECULARENABLE su 0, il valore predefinito, quando possibile. Quando si definiscono i materiali, è necessario impostare il valore di potenza speculare su zero per disattivare le evidenziazioni speculari per tale materiale; non è sufficiente impostare il colore speculare su 0,0,0.

## <a name="texture-size"></a>Dimensioni trama

Le prestazioni del mapping delle trame dipendono in larga parte dalla velocità della memoria. Esistono diversi modi per ottimizzare le prestazioni della cache delle trame dell'applicazione.

-   Mantenere piccole le trame. Più piccole sono le trame, maggiore è la probabilità che vengano mantenute nella cache secondaria della CPU principale.
-   Non modificare le trame in base alle primitive. Provare a mantenere i poligoni raggruppati in base all'ordine delle trame usate.
-   Usare trame quadrate quando possibile. Le trame le cui dimensioni sono 256x256 sono le più veloci. Se l'applicazione usa quattro trame 128x128, ad esempio, provare a verificare che usino la stessa tavolozza e le mettano tutte in una trama 256x256. Questa tecnica riduce anche la quantità di scambio di trame. Naturalmente, non è consigliabile usare trame 256x256 a meno che l'applicazione non richieda tale texturing perché, come accennato, le trame devono essere mantenute il più piccole possibile.

## <a name="matrix-transforms"></a>Trasformazioni con matrice

Direct3D usa le matrici world e view impostate per configurare diverse strutture di dati interne. Ogni volta che si imposta una nuova matrice globale o di visualizzazione, il sistema ricalcola le strutture interne associate. L'impostazione frequente di queste matrici, ad esempio migliaia di volte per frame, richiede molto tempo dal punto di vista del calcolo. È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzando le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità. Conservare le copie memorizzate nella cache delle singole matrici world e visualizzare in modo che sia possibile modificare, concatenare e reimpostare la matrice globale in base alle esigenze. Per maggiore chiarezza in questa documentazione, gli esempi Direct3D utilizzano raramente questa ottimizzazione.

## <a name="using-dynamic-textures"></a>Uso di trame dinamiche

Per determinare se il driver supporta trame dinamiche, controllare il flag D3DCAPS2 \_ DYNAMICTEXTURES della [**struttura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

Quando si lavora con trame dinamiche, tenere presente quanto segue.

-   Non possono essere gestiti. Ad esempio, il pool non può essere gestito da D3DPOOL. \_
-   Le trame dinamiche possono essere bloccate, anche se vengono create in D3DPOOL \_ DEFAULT.
-   D3DLOCK \_ DISCARD è un flag di blocco valido per le trame dinamiche.

È buona idea creare una sola trama dinamica per ogni formato e possibilmente per dimensione. Le mipmap dinamiche, i cubi e i volumi non sono consigliati a causa dell'overhead aggiuntivo nel blocco di ogni livello. Per le mipmap, D3DLOCK \_ DISCARD è consentito solo al livello superiore. Tutti i livelli vengono eliminati bloccando solo il livello superiore. Questo comportamento è lo stesso per volumi e cubi. Per i cubi, il livello superiore e il viso 0 sono bloccati.

Lo pseudocodice seguente illustra un esempio di uso di una trama dinamica.


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a>Uso dei vertici dinamici e dei buffer di indice

Il blocco di un vertex buffer statico mentre il processore grafico usa il buffer può avere una riduzione significativa delle prestazioni. La chiamata di blocco deve attendere il completamento della lettura dei dati del vertice o dell'indice dal buffer da parte del processore grafico prima che possa tornare all'applicazione chiamante, con un ritardo significativo. Il blocco e il rendering da un buffer statico più volte per frame impediscono inoltre al processore grafico di eseguire il buffering dei comandi di rendering, poiché deve completare i comandi prima di restituire il puntatore di blocco. Senza comandi memorizzati nel buffer, il processore di grafica rimane inattivo fino a quando l'applicazione non ha completato il riempimento del buffer dei vertici o index buffer e non esegue un comando di rendering.

Idealmente, i dati del vertice o dell'indice non cambieranno mai, ma questo non è sempre possibile. Esistono molte situazioni in cui l'applicazione deve modificare i dati dei vertici o indicizzare i dati ogni frame, anche più volte per fotogramma. In queste situazioni, il vertice o index buffer deve essere creato con D3DUSAGE \_ DYNAMIC. Questo flag di utilizzo determina l'ottimizzazione di Direct3D per operazioni di blocco frequenti. D3DUSAGE DYNAMIC è utile solo quando il buffer viene bloccato di frequente. I dati che rimangono costanti devono essere inseriti in un vertice statico o \_ in index buffer.

Per ottenere un miglioramento delle prestazioni quando si usano i buffer dei vertici dinamici, l'applicazione deve chiamare [**IDirect3DVertexBuffer9::Lock**](/windows/desktop/api) o [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) con i flag appropriati. D3DLOCK DISCARD indica che l'applicazione non deve mantenere i dati del vertice o \_ dell'indice precedente nel buffer. Se il processore di grafica usa ancora il buffer quando viene chiamato lock con D3DLOCK DISCARD, viene restituito un puntatore a una nuova area di memoria anziché i \_ dati del buffer precedente. In questo modo l'elaboratore di grafica può continuare a usare i dati vecchi mentre l'applicazione inserisce i dati nel nuovo buffer. Non è necessaria alcuna gestione aggiuntiva della memoria nell'applicazione. Il buffer precedente viene riutilizzato o eliminato automaticamente al termine dell'elaborazione grafica. Si noti che il blocco di un buffer con D3DLOCK DISCARD elimina sempre l'intero buffer, specificando un offset diverso da zero o un campo con dimensioni limitate non vengono mantenute le informazioni nelle aree sbloccate del \_ buffer.

In alcuni casi la quantità di dati che l'applicazione deve archiviare per ogni blocco è ridotta, ad esempio aggiungendo quattro vertici per eseguire il rendering di uno sprite. D3DLOCK NOOVERWRITE indica che l'applicazione non sovrascriverà i dati \_ già in uso nel buffer dinamico. La chiamata di blocco restituirà un puntatore ai dati meno usati, consentendo all'applicazione di aggiungere nuovi dati nelle aree inutilizzate del vertice o index buffer. L'applicazione non deve modificare i vertici o gli indici usati in un'operazione di disegno perché potrebbero essere ancora in uso dal processore di grafica. L'applicazione deve quindi usare D3DLOCK DISCARD dopo che il buffer dinamico è pieno per ricevere una nuova area di memoria, eliminando i dati del vertice o dell'indice precedente al termine dell'elaborazione \_ grafica.

Il meccanismo di query asincrono è utile per determinare se i vertici sono ancora in uso dal processore di grafica. Eseguire una query di tipo D3DQUERYTYPE \_ EVENT dopo l'ultima chiamata DrawPrimitive che usa i vertici. I vertici non sono più in uso quando [**IDirect3DQuery9::GetData**](/windows/desktop/api) restituisce S \_ OK. Il blocco di un buffer con D3DLOCK DISCARD o nessun flag garantisce sempre che i vertici siano sincronizzati correttamente con il processore di grafica, tuttavia l'uso del blocco senza flag comporta una penalità delle prestazioni descritta in \_ precedenza. Altre chiamate API, ad esempio [**IDirect3DDevice9::BeginScene**](/windows/desktop/api), [**IDirect3DDevice9::EndScene**](/windows/desktop/api)e [**IDirect3DDevice9::P resent,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) non garantiscono che il processore di grafica finirà di usare i vertici.

Di seguito sono riportati alcuni modi per usare i buffer dinamici e i flag di blocco adeguati.


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a>Uso di mesh

È possibile ottimizzare le mesh usando triangoli indicizzati Direct3D anziché strisce di triangoli indicizzati. L'hardware scoprirà che il 95% dei triangoli successivi forma effettivamente strisce e si adatta di conseguenza. Molti driver lo fanno anche per l'hardware meno recente.

Gli oggetti mesh D3DX possono avere ogni triangolo, o viso, contrassegnato con un DWORD, denominato attributo di tale viso. La semantica del valore DWORD è definita dall'utente. Vengono usati da D3DX per classificare la mesh in subset. L'applicazione imposta gli attributi per ogni viso usando la [**chiamata ID3DXMesh::LockAttributeBuffer.**](id3dxmesh--lockattributebuffer.md) Il [**metodo ID3DXMesh::Optimize**](id3dxmesh--optimize.md) consente di raggruppare vertici e visi mesh sugli attributi usando l'opzione ATTRSORT D3DXMESHOPT. \_ Al termine, l'oggetto mesh calcola una tabella di attributi che può essere ottenuta dall'applicazione chiamando [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md). Questa chiamata restituisce 0 se la mesh non è ordinata in base agli attributi. Un'applicazione non può impostare una tabella di attributi perché viene generata dal **metodo ID3DXMesh::Optimize.** L'ordinamento degli attributi è sensibile ai dati, quindi se l'applicazione sa che una mesh è ordinata con attributi, deve comunque chiamare **ID3DXMesh::Optimize** per generare la tabella degli attributi.

Gli argomenti seguenti descrivono i diversi attributi di una mesh.

### <a name="attribute-id"></a>ID attributo

Un ID attributo è un valore che associa un gruppo di visi a un gruppo di attributi. Questo ID descrive quale subset di [**visi ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) deve disegnare. Gli ID attributo vengono specificati per i visi nel buffer dell'attributo. I valori effettivi degli ID attributo possono essere qualsiasi valore che si adatti a 32 bit, ma è comune usare da 0 a n dove n è il numero di attributi.

### <a name="attribute-buffer"></a>Buffer degli attributi

Il buffer dell'attributo è una matrice di DWORD (uno per viso) che specifica il gruppo di attributi a cui appartiene ogni viso. Questo buffer viene inizializzato su zero al momento della creazione di una mesh, ma viene riempito dalle routine di caricamento o deve essere riempito dall'utente se si desidera più di un attributo con ID 0. Questo buffer contiene le informazioni usate per ordinare la mesh in base agli attributi in [**ID3DXMesh::Optimize.**](id3dxmesh--optimize.md) Se non è presente alcuna tabella di attributi, [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) analizza questo buffer per selezionare i visi dell'attributo specificato da disegnare.

### <a name="attribute-table"></a>Tabella degli attributi

La tabella degli attributi è una struttura di proprietà e gestita dalla mesh. L'unico modo per generare un elemento è chiamando [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) con l'ordinamento degli attributi o un'ottimizzazione più efficace abilitata. La tabella degli attributi viene usata per avviare rapidamente una singola chiamata primitiva di disegno a [**ID3DXBaseMesh::D rawSubset.**](id3dxbasemesh--drawsubset.md) L'unico altro uso è che anche le mesh in avanzamento mantengono questa struttura, quindi è possibile vedere quali visi e vertici sono attivi al livello di dettaglio corrente.

## <a name="z-buffer-performance"></a>Prestazioni del buffer Z

Le applicazioni possono migliorare le prestazioni quando si usa z-buffering e texturing assicurando che il rendering delle scene sia eseguito dall'avanti alla indietro. Le primitive con z buffer con trama vengono testate in base al z-buffer in base a una linea di analisi. Se una linea di analisi è nascosta da un poligono sottoposto a rendering in precedenza, il sistema la rifiuta in modo rapido ed efficiente. Il buffering Z può migliorare le prestazioni, ma la tecnica è particolarmente utile quando una scena disegna più volte gli stessi pixel. Questo è difficile da calcolare esattamente, ma spesso è possibile eseguire un'approssimazione vicina. Se gli stessi pixel vengono disegnati meno di due volte, è possibile ottenere prestazioni ottimali disattivando il buffering z ed eseguire il rendering della scena dall'indietro all'indietro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 

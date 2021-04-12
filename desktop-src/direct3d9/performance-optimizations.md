---
description: Ogni sviluppatore che crea applicazioni in tempo reale che usano grafica 3D è preoccupato per l'ottimizzazione delle prestazioni. In questa sezione vengono fornite le linee guida per ottenere le migliori prestazioni dal codice.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Ottimizzazioni delle prestazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d42be994522f0d83e36387b1a5866b3eee10df3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480692"
---
# <a name="performance-optimizations-direct3d-9"></a>Ottimizzazioni delle prestazioni (Direct3D 9)

Ogni sviluppatore che crea applicazioni in tempo reale che usano grafica 3D è preoccupato per l'ottimizzazione delle prestazioni. In questa sezione vengono fornite le linee guida per ottenere le migliori prestazioni dal codice.

-   [Suggerimenti generali sulle prestazioni](#general-performance-tips)
-   [Database ed eliminazione](#databases-and-culling)
-   [Primitive di batch](#batching-primitives)
-   [Suggerimenti per l'illuminazione](#lighting-tips)
-   [Dimensioni trama](#texture-size)
-   [Trasformazioni con matrice](#matrix-transforms)
-   [Uso di trame dinamiche](#using-dynamic-textures)
-   [Uso dei buffer di indice e vertex dinamici](#using-dynamic-vertex-and-index-buffers)
-   [Uso di mesh](#using-meshes)
-   [Prestazioni del buffer Z](#z-buffer-performance)

## <a name="general-performance-tips"></a>Suggerimenti generali sulle prestazioni

-   Deselezionare solo quando è necessario.
-   Ridurre al minimo le modifiche di stato e raggruppare le modifiche dello stato rimanenti.
-   Se possibile, utilizzare trame più piccole.
-   Consente di creare oggetti nella scena dalla parte anteriore a quella posteriore.
-   Usare le strisce di triangolo anziché gli elenchi e le ventole. Per ottimizzare le prestazioni della cache dei vertici, disponi le strisce per riutilizzare i vertici del triangolo prima, anziché più tardi.
-   Si riducono normalmente gli effetti speciali che richiedono una condivisione sproporzionata delle risorse di sistema.
-   Verifica costantemente le prestazioni dell'applicazione.
-   Ridurre al minimo le opzioni del buffer del vertice.
-   Usare i buffer dei vertici statici laddove possibile.
-   Usare un buffer di vertex statico di grandi dimensioni per ogni FVF per gli oggetti statici, anziché uno per ogni oggetto.
-   Se l'applicazione richiede l'accesso casuale al buffer dei vertici nella memoria AGP, scegliere una dimensione del formato del vertice che corrisponde a un multiplo di 32 byte. In caso contrario, selezionare il formato più piccolo appropriato.
-   Viene disegnato usando le primitive indicizzate. Ciò può consentire una memorizzazione nella cache dei vertici più efficiente all'interno dell'hardware.
-   Se il formato del buffer di profondità contiene un canale dello stencil, deselezionare sempre la profondità e i canali dello stencil nello stesso momento.
-   Combinare l'istruzione dello shader e l'output dei dati laddove possibile. Ad esempio:
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Database ed eliminazione

La creazione di un database affidabile degli oggetti nel mondo è fondamentale per prestazioni ottimali in Direct3D. È più importante dei miglioramenti apportati alla rasterizzazione o all'hardware.

È necessario mantenere il numero minimo di poligoni che è possibile gestire. Progettare per un numero ridotto di poligoni compilando i modelli a poligono basso dall'inizio. Aggiungere poligoni se è possibile farlo senza sacrificare le prestazioni in un secondo momento nel processo di sviluppo. Tenere presente che i poligoni più veloci sono quelli che non vengono disegnati.

## <a name="batching-primitives"></a>Primitive di batch

Per ottenere le migliori prestazioni di rendering durante l'esecuzione, provare a usare le primitive in batch e a limitare il numero di modifiche apportate allo stato di rendering al più basso possibile. Se, ad esempio, si dispone di un oggetto con due trame, raggruppare i triangoli che usano la prima trama e seguirli con lo stato di rendering necessario per modificare la trama. Quindi raggruppare tutti i triangoli che usano la seconda trama. Il supporto hardware più semplice per Direct3D viene chiamato con batch di Stati di rendering e batch di primitive tramite hardware abstraction layer (HAL). Più efficacemente vengono eseguite le istruzioni in batch, il minor numero di chiamate di HAL viene eseguito durante l'esecuzione.

## <a name="lighting-tips"></a>Suggerimenti per l'illuminazione

Poiché le luci aggiungono un costo per ogni vertice a ogni frame sottoposto a rendering, è possibile migliorare significativamente le prestazioni facendo attenzione a come vengono usate nell'applicazione. La maggior parte dei suggerimenti seguenti deriva dalla massima "il codice più veloce è il codice che non viene mai chiamato".

-   Usare il minor numero di fonti di luce possibili. Per aumentare il livello di illuminazione generale, ad esempio, usare la luce di ambiente anziché aggiungere una nuova sorgente di luce.
-   Le luci direzionali sono più efficienti rispetto alle luci puntiformi o ai faretti. Per le luci direzionali, la direzione verso la luce è fissa e non deve essere calcolata in base al vertice.
-   I Spotlight possono essere più efficienti delle luci puntiformi, in quanto l'area esterna al cono di luce viene calcolata rapidamente. Se i Spotlight sono più efficienti o meno, dipende dalla quantità di scena accesa da Spotlight.
-   Usare il parametro Range per limitare le luci solo alle parti della scena che è necessario illuminare. Tutti i tipi di luce terminano abbastanza presto quando sono fuori intervallo.
-   Le evidenziazioni speculari quasi il costo di una luce. Usarli solo quando è necessario. Impostare lo \_ stato di rendering SPECULARENABLE di D3DRS su 0, il valore predefinito, laddove possibile. Quando si definiscono i materiali, è necessario impostare il valore di potenza speculare su zero per disattivare le evidenziazioni speculari per quel materiale; Basta impostare il colore speculare su 0, 0, 0 non è sufficiente.

## <a name="texture-size"></a>Dimensioni trama

Le prestazioni di mapping delle trame sono molto dipendenti dalla velocità di memoria. Esistono diversi modi per ottimizzare le prestazioni della cache delle trame dell'applicazione.

-   Mantieni le trame di piccole dimensioni. Le trame più piccole sono, la probabilità migliore di essere mantenute nella cache secondaria principale della CPU.
-   Non modificare le trame in base alla primitiva. Provare a gestire i poligoni in base all'ordine delle trame usate.
-   Usare le trame quadre laddove possibile. Le trame le cui dimensioni sono 256x256 sono le più veloci. Se l'applicazione usa quattro trame 128x128, ad esempio, provare a verificare che usino la stessa tavolozza e posizionarli tutti in una trama 256x256. Questa tecnica riduce anche la quantità di swapping della trama. Naturalmente, è consigliabile non usare le trame 256x256, a meno che l'applicazione non richieda una maggiore texturing perché, come indicato, le trame devono essere mantenute il più piccolo possibile.

## <a name="matrix-transforms"></a>Trasformazioni con matrice

Direct3D usa le matrici World e View impostate per configurare diverse strutture di dati interne. Ogni volta che si imposta una nuova matrice World o View, il sistema ricalcola le strutture interne associate. L'impostazione frequente di queste matrici, ad esempio migliaia di volte per fotogramma, richiede molto tempo. È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzare le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità. Conserva le copie memorizzate nella cache di singole matrici e visualizza le matrici in modo che sia possibile modificare, concatenare e reimpostare la matrice globale in base alle esigenze. Per maggiore chiarezza in questa documentazione, gli esempi di Direct3D utilizzano raramente questa ottimizzazione.

## <a name="using-dynamic-textures"></a>Uso di trame dinamiche

Per determinare se il driver supporta le trame dinamiche, controllare il \_ flag D3DCAPS2 DYNAMICTEXTURES della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

Quando si utilizzano trame dinamiche, tenere presenti le considerazioni seguenti.

-   Non possono essere gestite. Il pool, ad esempio, non può essere \_ gestito D3DPOOL.
-   Le trame dinamiche possono essere bloccate, anche se vengono create in D3DPOOL \_ default.
-   D3DLOCK \_ scarto è un flag di blocco valido per le trame dinamiche.

È consigliabile creare una sola trama dinamica per ogni formato e possibilmente per dimensione. Non è consigliabile usare mipmap, cubi e volumi dinamici a causa dell'overhead aggiuntivo per il blocco di ogni livello. Per mipmap, l' \_ eliminazione D3DLOCK è consentita solo al primo livello. Tutti i livelli vengono eliminati bloccando solo il primo livello. Questo comportamento è identico per volumi e cubi. Per i cubi, il primo livello e il volto 0 sono bloccati.

Nello pseudocodice seguente viene illustrato un esempio di utilizzo di una trama dinamica.


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



## <a name="using-dynamic-vertex-and-index-buffers"></a>Uso dei buffer di indice e vertex dinamici

Il blocco di un buffer di vertex statico mentre il processore grafico sta utilizzando il buffer può comportare una riduzione significativa delle prestazioni. La chiamata di blocco deve attendere il completamento della lettura dei dati vertex o index dal buffer da parte del processore di grafica prima che sia possibile tornare all'applicazione chiamante, un ritardo significativo. Il blocco e il rendering da un buffer statico più volte per fotogramma impedisce inoltre al processore grafico di memorizzare nel buffer i comandi di rendering, dal momento che è necessario completare i comandi prima di restituire il puntatore di blocco. Senza i comandi memorizzati nel buffer, il processore di grafica rimane inattivo fino al termine dell'esecuzione del riempimento del buffer di vertex o dell'indice e genera un comando di rendering.

Idealmente, i dati dei vertici o degli indici non cambiano mai, ma ciò non è sempre possibile. Esistono molte situazioni in cui l'applicazione deve modificare i dati dei vertici o degli indici ogni frame, probabilmente anche più volte per fotogramma. Per queste situazioni, è necessario creare un vertex o un buffer di indice con D3DUSAGE \_ Dynamic. Questo flag di utilizzo consente a Direct3D di ottimizzare le operazioni di blocco frequenti. \_La dinamica D3DUSAGE è utile solo quando il buffer è bloccato di frequente; i dati che rimangono costanti devono essere inseriti in un vertex buffer statico o in un buffer di indice.

Per ottenere un miglioramento delle prestazioni quando si usano i buffer dei vertici dinamici, l'applicazione deve chiamare [**IDirect3DVertexBuffer9:: Lock**](/windows/desktop/api) o [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) con i flag appropriati. D3DLOCK \_ scarto indica che non è necessario che l'applicazione mantenga i dati del vertice o dell'indice precedente nel buffer. Se il processore grafico usa ancora il buffer quando il blocco viene chiamato con D3DLOCK \_ scarto, viene restituito un puntatore a una nuova area di memoria invece dei dati del buffer obsoleti. Questo consente al processore di grafica di continuare a usare i dati precedenti mentre l'applicazione inserisce i dati nel nuovo buffer. Nell'applicazione non è necessaria alcuna gestione della memoria aggiuntiva. il buffer precedente viene riutilizzato o eliminato automaticamente al termine dell'elaborazione grafica. Si noti che il blocco di un buffer con D3DLOCK \_ scarta sempre l'intero buffer, specificando un offset diverso da zero o un campo con dimensioni limitate non mantiene le informazioni nelle aree sbloccate del buffer.

Esistono casi in cui la quantità di dati che l'applicazione deve archiviare per blocco è ridotta, ad esempio l'aggiunta di quattro vertici per il rendering di uno sprite. D3DLOCK \_ nowrite indica che l'applicazione non sovrascriverà i dati già in uso nel buffer dinamico. La chiamata di blocco restituirà un puntatore ai dati obsoleti, consentendo all'applicazione di aggiungere nuovi dati in aree inutilizzate del vertex buffer o dell'indice. L'applicazione non deve modificare i vertici o gli indici usati in un'operazione di estrazione, perché potrebbero essere ancora usati dal processore di grafica. L'applicazione deve quindi usare D3DLOCK \_ scarto dopo che il buffer dinamico è pieno per ricevere una nuova area di memoria, rimuovendo i dati del vertice o dell'indice precedenti al termine del processore di grafica.

Il meccanismo di query asincrono è utile per determinare se i vertici sono ancora in uso da parte del processore di grafica. Eseguire una query di tipo \_ evento D3DQUERYTYPE dopo l'ultima chiamata DrawPrimitive che usa i vertici. I vertici non vengono più usati quando [**IDirect3DQuery9:: GetData**](/windows/desktop/api) restituisce S \_ OK. Il blocco di un buffer con D3DLOCK \_ scartare o nessun flag garantisce sempre che i vertici siano sincronizzati correttamente con il processore grafico. Tuttavia, l'uso del blocco senza flag comporterà la riduzione delle prestazioni descritta in precedenza. Altre chiamate API, ad esempio [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api), [**IDirect3DDevice9:: EndScene**](/windows/desktop/api)e [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) reinviate, non garantiscono che il processore grafico abbia terminato di usare i vertici.

Di seguito sono riportati i modi per usare i buffer dinamici e i flag di blocco appropriati.


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

È possibile ottimizzare le mesh usando triangoli indicizzati Direct3D anziché le strisce triangolari indicizzate. L'hardware scoprirà che il 95% dei triangoli successivi effettivamente forma le strisce e si adatta di conseguenza. Molti driver eseguono questa operazione anche per i componenti hardware meno recenti.

Gli oggetti mesh D3DX possono avere ogni triangolo, o volto, contrassegnato con un valore DWORD, denominato attributo della faccia. La semantica del valore DWORD è definita dall'utente. Vengono usati da D3DX per classificare la mesh in subset. L'applicazione imposta gli attributi per volto usando la chiamata [**ID3DXMesh:: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) . Il metodo [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) dispone di un'opzione per raggruppare i vertici mesh e i visi sugli attributi usando l' \_ opzione ATTRSORT di D3DXMESHOPT. Al termine di questa operazione, l'oggetto mesh calcola una tabella degli attributi che può essere ottenuta dall'applicazione chiamando [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md). Questa chiamata restituisce 0 se la mesh non è ordinata in base agli attributi. Per un'applicazione non è possibile impostare una tabella di attributi perché viene generata dal metodo **ID3DXMesh:: Optimize** . L'ordinamento dell'attributo è sensibile ai dati, pertanto se l'applicazione sa che una mesh è ordinata per l'attributo, è comunque necessario chiamare **ID3DXMesh:: Optimize** per generare la tabella degli attributi.

Negli argomenti seguenti vengono descritti i diversi attributi di una rete mesh.

### <a name="attribute-id"></a>ID attributo

Un ID di attributo è un valore che associa un gruppo di visi a un gruppo di attributi. Questo ID descrive il subset di visi [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) deve essere disegnato. Gli ID attributo sono specificati per i visi nel buffer dell'attributo. I valori effettivi degli ID degli attributi possono essere qualsiasi elemento che si trovi in 32 bit, ma è normale usare 0 per n dove n è il numero di attributi.

### <a name="attribute-buffer"></a>Buffer degli attributi

Il buffer dell'attributo è una matrice di DWORD (uno per volto) che specifica il gruppo di attributi a cui ogni face appartiene. Questo buffer viene inizializzato su zero durante la creazione di una mesh, ma viene compilato dalle routine di caricamento oppure deve essere compilato dall'utente se si desidera più di un attributo con ID 0. Questo buffer contiene le informazioni utilizzate per ordinare la mesh in base agli attributi in [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md). Se non è presente alcuna tabella degli attributi, [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) analizza questo buffer per selezionare i visi dell'attributo specificato da creare.

### <a name="attribute-table"></a>Tabella di attributi

La tabella attribute è una struttura di proprietà e gestita dalla mesh. L'unico modo per generarne uno è chiamando [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con l'ordinamento degli attributi o l'ottimizzazione più avanzata abilitata. La tabella attribute viene usata per avviare rapidamente una singola chiamata primitiva di estrazione a [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md). L'unico altro uso è che l'avanzamento delle mesh gestisce anche questa struttura, quindi è possibile vedere quali visi e vertici sono attivi al livello di dettaglio corrente.

## <a name="z-buffer-performance"></a>Prestazioni del buffer Z

Le applicazioni possono migliorare le prestazioni quando si usano il buffering z e la texturing garantendo il rendering delle scene dalla parte anteriore a quella posteriore. Le primitive con buffer z con trama vengono pretestate rispetto al buffer z in base a una linea di analisi. Se una riga di analisi è nascosta da un poligono di cui è stato eseguito il rendering in precedenza, il sistema lo respinge in modo rapido ed efficiente. Il buffer Z può migliorare le prestazioni, ma la tecnica risulta particolarmente utile quando una scena disegna gli stessi pixel più di una volta. Questo è difficile da calcolare esattamente, ma è spesso possibile creare un'approssimazione vicina. Se gli stessi pixel vengono disegnati meno di due volte, è possibile ottenere prestazioni ottimali disattivando il buffer z ed eseguendo il rendering della scena dal retro all'inizio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 

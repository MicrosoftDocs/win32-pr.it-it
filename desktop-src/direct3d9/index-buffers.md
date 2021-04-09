---
description: I buffer di indice, rappresentati dall'interfaccia IDirect3DIndexBuffer9, sono buffer di memoria contenenti dati di indice.
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: Buffer di indice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876193"
---
# <a name="index-buffers-direct3d-9"></a>Buffer di indice (Direct3D 9)

I buffer di indice, rappresentati dall'interfaccia [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , sono buffer di memoria contenenti dati di indice. I dati di indice, o indici, sono offset di tipo integer nei buffer dei vertici e vengono usati per eseguire il rendering delle primitive usando il metodo [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

Un buffer di vertici contiene vertici; Pertanto, è possibile creare un buffer vertex con o senza primitive indicizzate. Tuttavia, poiché in un buffer di indice sono contenuti indici, non è possibile utilizzare un buffer di indice senza un buffer vertex corrispondente. (Come nota collaterale, [**IDirect3DDevice9::D rawindexedprimitiveup**](/windows/desktop/api) e [**IDirect3DDevice9::D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) sono gli unici metodi di estrazione che vengono disegnato senza un indice o un vertex buffer).

## <a name="index-buffer-description"></a>Descrizione buffer di indice

Un buffer di indice viene descritto in termini di capacità, ad esempio dove è presente in memoria, se supporta la lettura e la scrittura, nonché il tipo e il numero di indici che può contenere. Questi tratti sono contenuti in una struttura [**D3DINDEXBUFFER \_ desc**](d3dindexbuffer-desc.md) .

Le descrizioni dei buffer di indice indicano all'applicazione il modo in cui è stato creato un buffer esistente. Si fornisce una struttura di descrizione vuota per il sistema in modo da riempire le funzionalità di un buffer di indice creato in precedenza.

-   Il membro Format descrive il formato di superficie dei dati del buffer dell'indice.
-   Il tipo identifica il tipo di risorsa del buffer dell'indice.
-   Il membro della struttura Usage contiene flag di funzionalità generali. Il \_ flag SOFTWAREPROCESSING di D3DUSAGE indica che il buffer dell'indice deve essere usato con l'elaborazione dei vertici software. La presenza del \_ flag WRITEONLY di D3DUSAGE nell'utilizzo indica che la memoria buffer dell'indice viene utilizzata solo per le operazioni di scrittura. Questo consente di liberare il driver per inserire i dati dell'indice nella migliore posizione di memoria per consentire l'elaborazione e il rendering rapidi. Se il \_ flag WRITEONLY di D3DUSAGE non viene utilizzato, è meno probabile che i dati vengano inseriti in un percorso non efficiente per le operazioni di lettura. Questo comporta una certa velocità di elaborazione e di rendering. Se questo flag non è specificato, si presuppone che le applicazioni eseguano operazioni di lettura e scrittura sui dati nel buffer dell'indice.
-   Pool specifica la classe di memoria allocata per il buffer dell'indice. Il \_ flag SYSTEMMEM di D3DPOOL indica che il sistema ha creato il buffer di indice nella memoria di sistema.
-   Il membro size archivia le dimensioni, in byte, dei dati del buffer dei vertici.
-   L'ultimo parametro pSharedHandle non viene utilizzato. Impostarla su **null**.

## <a name="index-processing-requirements"></a>Requisiti di elaborazione degli indici

Le prestazioni delle operazioni di elaborazione degli indici dipendono in larga misura dal punto in cui è presente il buffer dell'indice in memoria e dal tipo di dispositivo di rendering utilizzato. Le applicazioni controllano l'allocazione di memoria per i buffer di indice al momento della creazione. Quando \_ viene impostato il flag di Memoria D3DPOOL SYSTEMMEM, il buffer dell'indice viene creato nella memoria di sistema. Quando \_ viene utilizzato il flag di memoria predefinito D3DPOOL, il driver di dispositivo determina la posizione in cui viene allocata la memoria per il buffer di indice, spesso definita memoria ottimale del driver. Driver: la memoria ottimale può essere memoria video locale, memoria video non locale o memoria di sistema.

\_Se si imposta il flag di comportamento SOFTWAREPROCESSING di D3DUSAGE quando si chiama il metodo [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) , viene specificato che il buffer dell'indice deve essere utilizzato con l'elaborazione dei vertici software. Questo flag è obbligatorio in modalità mista (D3DCREATE \_ mixed \_ VERTEXPROCESSING) quando si usa l'elaborazione dei vertici software.

L'applicazione può scrivere direttamente gli indici in un buffer di indice allocato nella memoria ottimale del driver. Questa tecnica impedisce un'operazione di copia ridondante in un secondo momento. Questa tecnica non funziona bene se l'applicazione legge i dati da un buffer di indice, perché le operazioni di lettura eseguite dall'host dalla memoria ottimale del driver possono essere molto lente. Pertanto, se l'applicazione deve leggere durante l'elaborazione o scrive i dati nel buffer in modo anomalo, è preferibile scegliere un buffer di indice della memoria di sistema.

> [!Note]  
> Usare sempre D3DPOOL \_ default, tranne quando non si vuole usare la memoria video o usare grandi quantità di RAM con blocco di pagina quando il driver inserisce i buffer dei vertici o degli indici nella memoria AGP.

 

## <a name="create-an-index-buffer"></a>Creazione di un buffer di indice

Creare un oggetto buffer di indice chiamando il metodo [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) , che accetta sei parametri.

-   Il primo parametro specifica la lunghezza in byte del buffer di indice.
-   Il secondo parametro è un set di controlli di utilizzo. Tra le altre cose, il valore determina se i vertici a cui fanno riferimento gli indici sono in grado di contenere informazioni di ritaglio. Per migliorare le prestazioni, specificare D3DUSAGE \_ DONOTCLIP quando il ritaglio non è necessario.

    Il \_ flag D3DUSAGE SOFTWAREPROCESSING può essere impostato quando è abilitata l'elaborazione di vertici in modalità mista o software (D3DCREATE \_ mixed \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) per tale dispositivo. \_È necessario impostare D3DUSAGE SOFTWAREPROCESSING per i buffer da usare con l'elaborazione dei vertici software in modalità mista, ma non deve essere impostata per ottenere le migliori prestazioni possibili quando si usa l'elaborazione degli indici hardware in modalità mista ( \_ hardware D3DCREATE \_ VERTEXPROCESSING). Tuttavia, l'impostazione di D3DUSAGE \_ SOFTWAREPROCESSING è l'unica opzione quando si usa un singolo buffer con l'elaborazione dei vertici hardware e software. D3DUSAGE \_ SOFTWAREPROCESSING è consentito per i dispositivi misti e software.

    È possibile forzare i buffer dei vertici e degli indici nella memoria di sistema specificando D3DPOOL \_ SYSTEMMEM, anche quando l'elaborazione dell'indice viene eseguita in hardware. Questo è un modo per evitare quantità eccessivamente elevate di memoria con blocco di pagina quando un driver inserisce questi buffer nella memoria AGP.

-   Il terzo parametro è il membro D3DFMT \_ INDEX16 o D3DFMT \_ INDEX32 del tipo enumerato [D3DFORMAT](d3dformat.md) che specifica la dimensione di ogni indice.

-   Il quarto parametro è un membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) che indica al sistema in cui inserire il nuovo buffer di indice in memoria.

-   Il parametro finale che [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) accetta è l'indirizzo di una variabile che viene riempito con un puntatore alla nuova interfaccia [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) dell'oggetto vertex buffer, se la chiamata ha esito positivo.

Nell'esempio di codice C++ riportato di seguito viene illustrato l'aspetto della creazione di un buffer di indice nel codice.


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a>Accedere a un buffer di indice

Gli oggetti buffer di indice consentono alle applicazioni di accedere direttamente alla memoria allocata per i dati dell'indice. È possibile recuperare un puntatore alla memoria del buffer di indicizzazione chiamando il metodo [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) e quindi accedendo alla memoria in base alle esigenze per riempire il buffer con i nuovi dati di indice o per leggere i dati in esso contenuti. Il metodo Lock accetta quattro parametri. Il primo, *OffsetToLock*, è l'offset nei dati dell'indice. Il secondo parametro corrisponde alla dimensione, espressa in byte, dei dati dell'indice. Il terzo parametro accettato dal metodo **IDirect3DIndexBuffer9:: Lock** , *ppbData*, è l'indirizzo di un puntatore di byte riempito con un puntatore ai dati di indice, se la chiamata ha esito positivo.

L'ultimo parametro, *Flags*, indica al sistema la modalità di blocco della memoria. È possibile usarlo per indicare il modo in cui l'applicazione accede ai dati nel buffer. Specificare le costanti per il parametro *Flags* in base alla modalità di accesso ai dati dell'indice da parte dell'applicazione. Ciò consente al driver di bloccare la memoria e fornire le migliori prestazioni in base al tipo di accesso richiesto. Usare \_ il flag di sola lettura D3DLOCK se l'applicazione viene letta solo dalla memoria buffer dell'indice. L'inclusione di questo flag consente a Direct3D di ottimizzare le procedure interne per migliorare l'efficienza, dato che l'accesso alla memoria sarà di sola lettura.

Dopo aver compilato o letto i dati dell'indice, chiamare il metodo [**IDirect3DIndexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) , come illustrato nell'esempio di codice seguente.


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> Se si crea un buffer di indice con il \_ flag D3DUSAGE WRITEONLY, non usare il flag di blocco di sola \_ lettura D3DLOCK. Usare il \_ flag di sola lettura D3DLOCK se l'applicazione viene letta solo dalla memoria buffer dell'indice. L'inclusione di questo flag consente a Direct3D di ottimizzare le procedure interne per migliorare l'efficienza, dato che l'accesso alla memoria sarà di sola lettura.
>
> Per informazioni sull'uso di D3DLOCK \_ scarto o D3DLOCK \_ nowrite per il parametro *Flags* del metodo [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) , vedere [ottimizzazioni delle prestazioni (Direct3D 9)](performance-optimizations.md).

 

In C++, poiché si accede direttamente alla memoria allocata per il buffer di indice, assicurarsi che l'applicazione acceda correttamente alla memoria allocata. In caso contrario, si rischia il rendering della memoria non valida. Usare lo stride del formato di indice usato dall'applicazione per passare da un indice nel buffer allocato a un altro.

Recuperare informazioni su un buffer dell'indice chiamando il metodo [**IDirect3DIndexBuffer9:: getdesc**](/windows/desktop/api) . Questo metodo compila i membri della struttura [**D3DINDEXBUFFER \_ desc**](d3dindexbuffer-desc.md) con le informazioni sul buffer dell'indice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> <dt>

[Rendering dai buffer di Vertex e index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Buffer vertex (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 

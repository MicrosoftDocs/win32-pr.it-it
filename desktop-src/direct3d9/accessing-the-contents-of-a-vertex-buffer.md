---
description: Gli oggetti vertex buffer consentono alle applicazioni di accedere direttamente alla memoria allocata per i dati dei vertici.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Accesso al contenuto di un buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304883"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a>Accesso al contenuto di un buffer vertex (Direct3D 9)

Gli oggetti vertex buffer consentono alle applicazioni di accedere direttamente alla memoria allocata per i dati dei vertici. È possibile recuperare un puntatore alla memoria del buffer dei vertici chiamando il metodo [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) e quindi accedendo alla memoria in base alle esigenze per riempire il buffer con i nuovi dati dei vertici o per leggere i dati già contenuti. Il metodo **IDirect3DVertexBuffer9:: Lock** accetta quattro parametri. Il primo, *OffsetToLock*, è l'offset nei dati del vertice. Il secondo parametro è la dimensione, espressa in byte, dei dati del vertice. Il terzo parametro accettato è l'indirizzo di un puntatore che punta ai dati del vertice, se la chiamata ha esito positivo.

L'ultimo parametro, *Flags*, indica al sistema la modalità di blocco della memoria. Specificare le costanti per il parametro *Flags* in base alla modalità di accesso ai dati dei vertici. Verificare che il valore scelto per [**D3DUSAGE**](d3dusage.md) corrisponda al valore scelto per [D3DLOCK](d3dlock.md). Se, ad esempio, si crea un buffer vertex con solo accesso in scrittura, non è sensato provare a leggere i dati specificando D3DLOCK \_ ReadOnly. L'utilizzo di questi flag consente al driver di bloccare la memoria e fornire le migliori prestazioni, dato il tipo di accesso richiesto.

Dopo aver completato la compilazione o la lettura dei dati dei vertici, chiamare il metodo [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , come illustrato nell'esempio di codice seguente.


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



Se si crea un buffer vertex con il \_ flag WRITEONLY di D3DUSAGE, non usare il flag di blocco di sola \_ lettura D3DLOCK. Usare il \_ flag di sola lettura D3DLOCK se l'applicazione viene letta solo dalla memoria del buffer dei vertici. L'inclusione di questo flag consente a Direct3D di ottimizzare le procedure interne per migliorare l'efficienza, dato che l'accesso alla memoria sarà di sola lettura.

Per [](performance-optimizations.md) informazioni sull'uso di D3DLOCK \_ scarto o D3DLOCK \_ sovrascrittura per il parametro Flags di [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), vedere uso dei buffer di indice e dei vertici dinamici.

In C++, poiché si accede direttamente alla memoria allocata per il buffer dei vertici, assicurarsi che l'applicazione acceda correttamente alla memoria allocata. In caso contrario, si rischia il rendering della memoria non valida. Usare lo stride del formato Vertex usato dall'applicazione per spostarsi da un vertice nel buffer allocato a un altro. La memoria del buffer dei vertici è una semplice matrice di vertici specificati in FVF. Utilizzare lo stride della struttura del formato Vertex definito. È possibile calcolare lo stride di ogni vertice in fase di esecuzione esaminando i [D3DFVF](d3dfvf.md) contenuti nella descrizione del buffer dei vertici. Nella tabella seguente vengono illustrate le dimensioni di ogni componente vertice.



| Flag di formato vertici | Dimensione              |
|--------------------|-------------------|
| D3DFVF \_ diffuse    | sizeof (DWORD)     |
| D3DFVF \_ normale     | sizeof (float) x 3 |
| D3DFVF \_ speculare   | sizeof (DWORD)     |
| \_TEXN D3DFVF       | sizeof (float) x n |
| D3DFVF \_ XYZ        | sizeof (float) x 3 |
| \_XYZRHW D3DFVF     | sizeof (float) x 4 |



 

Il numero di coordinate di trama presenti nel formato vertici è descritto dai \_ flag D3DFVF Tex n (dove n è un valore compreso tra 0 e 8). Moltiplicare il numero di set di coordinate di trama per la dimensione di un set di coordinate di trama, che può variare da uno a quattro float, per calcolare la memoria necessaria per quel numero di coordinate di trama.

Usare lo stride totale del vertice per incrementare e decrementare il puntatore di memoria in base alle esigenze per accedere a vertici specifici.

## <a name="retrieving-vertex-buffer-descriptions"></a>Recupero delle descrizioni dei buffer dei vertici

È possibile recuperare informazioni su un buffer vertex chiamando il metodo [**IDirect3DVertexBuffer9:: getdesc**](/windows/desktop/api) . Questo metodo compila i membri della struttura [**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md) con le informazioni sul buffer dei vertici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer vertici](vertex-buffers.md)
</dt> </dl>

 

 

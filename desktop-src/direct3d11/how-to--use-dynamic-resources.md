---
title: Come usare le risorse dinamiche
description: Le risorse dinamiche vengono create e usate quando l'app deve modificare i dati in tali risorse. È possibile creare trame e buffer per l'utilizzo dinamico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d85933490d1e3bbbd09cc83720651c4fd634012f8e5aa70562396e87c096ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633101"
---
# <a name="how-to-use-dynamic-resources"></a>Procedura: Usare le risorse dinamiche

**API importanti**

-   [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**UTILIZZO D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Le risorse dinamiche vengono create e usate quando l'app deve modificare i dati in tali risorse. È possibile creare trame e buffer per l'utilizzo dinamico.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Procedura: Creare una trama](overviews-direct3d-11-resources-textures-create.md)
-   [Procedura: Inizializzare una trama a livello di codice](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Procedura: Creare un buffer costante](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Prerequisiti

Partiamo dal presupposto che tu abbia familiarità con C++. Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-specify-dynamic-usage"></a>Passaggio 1: Specificare l'utilizzo dinamico

Se si vuole che l'app sia in grado di apportare modifiche alle risorse, è necessario specificare tali risorse come dinamiche e scrivibili durante la creazione.

**Per specificare l'utilizzo dinamico**

1.  Specificare l'utilizzo delle risorse come dinamico. Ad esempio, specificare il valore [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) nel membro **Usage** di [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) per un vertice o un buffer costante e specificare il valore **D3D11 \_ USAGE \_ DYNAMIC** nel membro **Usage** di [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) per una trama 2D.
2.  Specificare la risorsa come scrivibile. Ad esempio, specificare il [**valore D3D11 \_ CPU ACCESS \_ \_ WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) nel membro **CPUAccessFlags** di [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) o [**D3D11 \_ TEXTURE2D \_ DESC.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)
3.  Passare la descrizione della risorsa alla funzione di creazione. Ad esempio, passare l'indirizzo di [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e passare l'indirizzo di [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) a [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Di seguito è riportato un esempio di creazione di un vertex buffer dinamico:


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a>Passaggio 2: Modificare una risorsa dinamica

Se una risorsa è stata specificata come dinamica e scrivibile al momento della creazione, è possibile apportare modifiche a tale risorsa in un secondo momento.

**Per modificare i dati in una risorsa dinamica**

1.  Configurare i nuovi dati per la risorsa. Dichiarare una [**variabile di tipo D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inizializzarla su zero. Questa variabile verrà utilizzata per modificare la risorsa.
2.  Disabilitare l'accesso alle unità di elaborazione grafica (GPU) ai dati da modificare e ottenere un puntatore alla memoria che contiene i dati. Per ottenere questo puntatore, passare [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) al parametro *MapType* quando si [**chiama ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). Impostare questo puntatore sull'indirizzo della [**variabile \_ \_ SUBRESOURCE MAPPATA D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) del passaggio precedente.
3.  Scrivere i nuovi dati nella memoria.
4.  Chiamare [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) per riabilitarne l'accesso gpu ai dati al termine della scrittura dei nuovi dati.

Di seguito è riportato un esempio di modifica di un vertex buffer dinamico:


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a>Commenti

### <a name="using-dynamic-textures"></a>Uso di trame dinamiche

È consigliabile creare una sola trama dinamica per ogni formato e possibilmente per ogni dimensione. Non è consigliabile creare mipmap, cubi e volumi dinamici a causa dell'overhead aggiuntivo nel mapping di ogni livello. Per le mipmap, è possibile specificare [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) solo nel livello superiore. Tutti i livelli vengono eliminati tramite il mapping solo al livello superiore. Questo comportamento è lo stesso per i volumi e i cubi. Per i cubi, viene eseguito il mapping del livello superiore e della faccia 0.

### <a name="using-dynamic-buffers"></a>Uso di buffer dinamici

Quando si chiama [**Map su**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) un buffer dei vertici statico mentre la GPU usa il buffer, si ottiene una riduzione significativa delle prestazioni. In questo caso, **Map** deve attendere fino a quando la GPU non completa la lettura dei dati del vertice o dell'indice dal buffer prima che **Map** possa tornare all'app chiamante, causando un ritardo significativo. La **chiamata a Map** e quindi il rendering da un buffer statico più volte per frame impediscono anche alla GPU di eseguire il buffering dei comandi di rendering perché deve completare i comandi prima di restituire il puntatore della mappa. Senza comandi memorizzati nel buffer, la GPU rimane inattiva fino a quando l'app non ha completato il riempimento del buffer dei vertici o index buffer e non esegue un comando di rendering.

Idealmente, i dati del vertice o dell'indice non cambieranno mai, ma questo non è sempre possibile. In molte situazioni l'app deve modificare i dati dei vertici o indicizzare i dati ogni frame, anche più volte per fotogramma. In queste situazioni, è consigliabile creare il vertice o il index buffer [**con D3D11 \_ USAGE \_ DYNAMIC.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) Questo flag di utilizzo determina l'ottimizzazione del runtime per le operazioni di mapping frequenti. **D3D11 \_ USAGE \_ DYNAMIC è** utile solo quando il buffer viene mappato di frequente. Se i dati devono rimanere costanti, posizionare i dati in un vertice statico o in index buffer.

Per ottenere un miglioramento delle prestazioni quando si usano i buffer dei vertici dinamici, l'app deve chiamare [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) con i valori [**\_ MAP D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) appropriati. [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica che l'app non deve mantenere i dati del vertice o dell'indice precedente nel buffer. Se la GPU usa ancora il buffer quando si chiama **Map** con **D3D11 \_ MAP WRITE \_ \_ DISCARD,** il runtime restituisce un puntatore a una nuova area di memoria anziché ai dati del buffer precedente. Ciò consente alla GPU di continuare a usare i dati vecchi mentre l'app inserisce i dati nel nuovo buffer. Non è necessaria alcuna gestione aggiuntiva della memoria nell'app. il buffer precedente viene riutilizzato o eliminato automaticamente al termine della GPU.

> [!Note]  
> Quando si esegue il mapping di un buffer [**con D3D11 \_ MAP WRITE \_ \_ DISCARD,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)il runtime elimina sempre l'intero buffer. Non è possibile mantenere le informazioni nelle aree del buffer non mappate specificando un campo con offset diverso da zero o dimensioni limitate.

 

In alcuni casi la quantità di dati che l'app deve archiviare per ogni mappa è ridotta, ad esempio aggiungendo quattro vertici per eseguire il rendering di uno sprite. [**D3D11 \_ MAP \_ WRITE \_ NO \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica che l'app non sovrascriverà i dati già in uso nel buffer dinamico. La [**chiamata**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) map restituirà un puntatore ai dati meno usati, che consentirà all'app di aggiungere nuovi dati nelle aree inutilizzate del vertice o index buffer. L'app non deve modificare i vertici o gli indici usati in un'operazione di disegno perché potrebbero essere ancora in uso dalla GPU. È consigliabile che l'app usi quindi [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) dopo che il buffer dinamico è pieno per ricevere una nuova area di memoria, che rimuove i dati del vertice o dell'indice precedente al termine della GPU.

Il meccanismo di query asincrona è utile per determinare se i vertici sono ancora in uso dalla GPU. Eseguire una query di tipo [**D3D11 \_ QUERY \_ EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) dopo l'ultima chiamata di disegno che usa i vertici. I vertici non sono più in uso quando [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) restituisce S \_ OK. Quando si esegue il mapping di un buffer con [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o nessun valore della mappa, viene sempre garantito che i vertici siano sincronizzati correttamente con la GPU. Tuttavia, quando si esegue il mapping senza valori della mappa, si incorre in una penalità delle prestazioni descritta in precedenza.

> [!Note]  
> Il runtime Direct3D 11.1, disponibile a partire da Windows 8, consente il mapping di buffer costanti dinamiche e viste risorse shader di buffer dinamici con [**D3D11 \_ MAP WRITE NO \_ \_ \_ OVERWRITE.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) I runtime Direct3D 11 e precedenti limitano il mapping di aggiornamento parziale senza sovrascrittura ai buffer dei vertici o degli indici. Per determinare se un dispositivo Direct3D supporta queste funzionalità, chiamare [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** riempie i membri di una struttura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) con le funzionalità del dispositivo. I membri pertinenti sono **MapNoOverwriteOnDynamicConstantBuffer** e **MapNoOverwriteOnDynamicBufferSRV.**

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





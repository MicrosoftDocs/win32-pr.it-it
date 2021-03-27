---
title: Come usare le risorse dinamiche
description: Quando l'app deve modificare i dati in tali risorse, è possibile creare e usare risorse dinamiche. È possibile creare trame e buffer per l'utilizzo dinamico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221038"
---
# <a name="how-to-use-dynamic-resources"></a>Procedura: usare risorse dinamiche

**API importanti**

-   [**Sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**Sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**Utilizzo di D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Quando l'app deve modificare i dati in tali risorse, è possibile creare e usare risorse dinamiche. È possibile creare trame e buffer per l'utilizzo dinamico.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Procedura: creare una trama](overviews-direct3d-11-resources-textures-create.md)
-   [Procedura: inizializzare una trama a livello di codice](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Procedura: creare un buffer costante](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Prerequisiti

Partiamo dal presupposto che tu abbia familiarità con C++. Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-specify-dynamic-usage"></a>Passaggio 1: specificare l'utilizzo dinamico

Se si vuole che l'app sia in grado di apportare modifiche alle risorse, è necessario specificare tali risorse come dinamiche e scrivibili quando vengono create.

**Per specificare l'utilizzo dinamico**

1.  Specificare l'utilizzo delle risorse come dinamico. Ad esempio, specificare il [**valore \_ \_ dinamico utilizzo d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) nel membro **Usage** di [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) per un vertex o un buffer costante e specificare il valore **\_ \_ dinamico utilizzo d3d11** nel membro **Usage** di [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) per una trama 2D.
2.  Specificare la risorsa come scrivibile. Ad esempio, specificare il valore di [**scrittura di \_ accesso alla CPU \_ \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) nel membro **CPUAccessFlags** di [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) o [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).
3.  Passare la descrizione della risorsa alla funzione di creazione. Ad esempio, passare l'indirizzo del [**\_ buffer D3D11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e passare l'indirizzo di [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Di seguito è riportato un esempio di creazione di un buffer dei vertici dinamici:


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



### <a name="step-2-change-a-dynamic-resource"></a>Passaggio 2: modificare una risorsa dinamica

Se una risorsa è stata specificata come dinamica e scrivibile quando è stata creata, è possibile apportare modifiche in un secondo momento a tale risorsa.

**Per modificare i dati in una risorsa dinamica**

1.  Configurare i nuovi dati per la risorsa. Dichiarare una variabile di tipo [**\_ \_ sottorisorsa con mapping di d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inizializzarla su zero. Questa variabile verrà usata per modificare la risorsa.
2.  Disabilitare l'accesso alla GPU (Graphics Processing Unit) ai dati che si desidera modificare e ottenere un puntatore alla memoria che contiene i dati. Per ottenere questo puntatore, passare [**d3d11 \_ Map \_ Write \_ scarti**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) al parametro *MapType* quando si chiama [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). Impostare questo puntatore sull'indirizzo della variabile della [**\_ \_ sottorisorsa mappata d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) dal passaggio precedente.
3.  Scrivere i nuovi dati nella memoria.
4.  Chiamare [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) per riabilitare l'accesso alla GPU ai dati al termine della scrittura dei nuovi dati.

Ecco un esempio di modifica di un buffer dei vertici dinamici:


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

Si consiglia di creare una sola trama dinamica per ogni formato e possibilmente per dimensione. Non è consigliabile creare mipmap, cubi e volumi dinamici a causa del sovraccarico aggiuntivo nel mapping di ogni livello. Per mipmap, è possibile specificare [**d3d11 \_ mapping \_ Write \_ scarti**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) solo al livello principale. Tutti i livelli vengono eliminati eseguendo il mapping solo del primo livello. Questo comportamento è identico per volumi e cubi. Per i cubi, viene eseguito il mapping del primo livello e del volto 0.

### <a name="using-dynamic-buffers"></a>Uso di buffer dinamici

Quando si chiama [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) su un buffer di vertice statico mentre la GPU usa il buffer, si ottiene un calo significativo delle prestazioni. In questa situazione, **Map** deve attendere fino al termine della lettura dei dati vertex o index dal buffer prima che **Map** possa tornare all'app chiamante, causando un ritardo significativo. La chiamata di **Map** e quindi il rendering da un buffer statico più volte per fotogramma impedisce inoltre alla GPU di memorizzare nel buffer i comandi di rendering perché devono terminare i comandi prima di restituire il puntatore della mappa. Senza i comandi memorizzati nel buffer, la GPU rimane inattiva finché l'app non riempie il buffer dei vertici o degli indici e genera un comando di rendering.

Idealmente, i dati dei vertici o degli indici non cambiano mai, ma ciò non è sempre possibile. Esistono molte situazioni in cui l'app deve modificare i dati dei vertici o degli indici ogni frame, probabilmente anche più volte per fotogramma. Per queste situazioni, è consigliabile creare il vertex buffer o index buffer con [**d3d11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Questo flag di utilizzo determina l'ottimizzazione del runtime per operazioni di mapping frequenti. **D3d11 \_ \_Dynamic Usage** è utile solo quando il buffer è mappato di frequente; Se i dati devono rimanere costanti, inserire i dati in un vertex buffer statico o indice.

Per ottenere un miglioramento delle prestazioni quando si usano i buffer dei vertici dinamici, l'app deve chiamare [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) con i valori di [**\_ mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) appropriati. [**D3d11 \_ Lo \_ \_ scarto di scrittura della mappa**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica che l'app non deve conservare i dati del vertice o dell'indice precedente nel buffer. Se la GPU sta ancora usando il buffer quando si chiama **Map** con **l' \_ \_ \_ eliminazione della scrittura della mappa d3d11**, il runtime restituisce un puntatore a una nuova area di memoria anziché ai dati del buffer obsoleti. Questo consente alla GPU di continuare a usare i dati obsoleti mentre l'app inserisce i dati nel nuovo buffer. Nell'app non è necessaria alcuna gestione della memoria aggiuntiva. il buffer precedente viene riutilizzato o eliminato automaticamente al termine della GPU.

> [!Note]  
> Quando si esegue il mapping di un buffer con lo [**\_ scarto di \_ scrittura \_ della mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), il runtime elimina sempre l'intero buffer. Non è possibile mantenere le informazioni nelle aree non mappate del buffer specificando un campo offset diverso da zero o dimensioni limitate.

 

Esistono casi in cui la quantità di dati che l'app deve archiviare per ogni mappa è ridotta, ad esempio l'aggiunta di quattro vertici per il rendering di uno sprite. [**D3d11 \_ MAP \_ Write \_ No \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) overwrite indica che l'app non sovrascriverà i dati già in uso nel buffer dinamico. La chiamata della [**mappa**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) restituirà un puntatore ai dati obsoleti, che consentirà all'app di aggiungere nuovi dati in aree inutilizzate del vertex buffer o dell'indice. L'app non deve modificare i vertici o gli indici usati in un'operazione di estrazione, perché potrebbero essere ancora in uso dalla GPU. È consigliabile che l'app usi quindi [**lo \_ \_ \_ scarto di scrittura della mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) dopo che il buffer dinamico è pieno per ricevere una nuova area di memoria, che elimina il vertice o i dati di indice precedenti al termine della GPU.

Il meccanismo di query asincrono è utile per determinare se i vertici sono ancora in uso dalla GPU. Eseguire una query di tipo [**\_ \_ evento di query d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) dopo l'ultima chiamata di progetto che usa i vertici. I vertici non vengono più usati quando [**sul ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) restituisce S \_ OK. Quando si esegue il mapping di un buffer con l' [**\_ \_ \_ eliminazione della mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o senza valori della mappa, si garantisce sempre che i vertici vengano sincronizzati correttamente con la GPU. Tuttavia, quando si esegue il mapping senza valori della mappa, si comporterà la riduzione delle prestazioni descritta in precedenza.

> [!Note]  
> Il runtime Direct3D 11,1, disponibile a partire da Windows 8, Abilita il mapping dei buffer costanti dinamici e delle visualizzazioni delle risorse dello shader (SRVs) dei buffer dinamici con la [**\_ mappa d3d11 \_ \_ senza \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)sovrascrivere. I runtime Direct3D 11 e versioni precedenti hanno limitato la sovrascrittura del mapping di aggiornamento parziale ai buffer vertex o index. Per determinare se un dispositivo Direct3D supporta queste funzionalità, chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**le \_ \_ \_ Opzioni della funzionalità d3d11 di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** riempie i membri di una struttura di [**\_ \_ \_ \_ Opzioni d3d11 di dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) con le funzionalità del dispositivo. I membri pertinenti sono **MapNoOverwriteOnDynamicConstantBuffer** e **MapNoOverwriteOnDynamicBufferSRV**.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





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
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="eb252-104">Procedura: usare risorse dinamiche</span><span class="sxs-lookup"><span data-stu-id="eb252-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="eb252-105">**API importanti**</span><span class="sxs-lookup"><span data-stu-id="eb252-105">**Important APIs**</span></span>

-   [<span data-ttu-id="eb252-106">**Sul ID3D11DeviceContext:: Map**</span><span class="sxs-lookup"><span data-stu-id="eb252-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="eb252-107">**Sul ID3D11DeviceContext:: annullare**</span><span class="sxs-lookup"><span data-stu-id="eb252-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="eb252-108">**Utilizzo di D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="eb252-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="eb252-109">Quando l'app deve modificare i dati in tali risorse, è possibile creare e usare risorse dinamiche.</span><span class="sxs-lookup"><span data-stu-id="eb252-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="eb252-110">È possibile creare trame e buffer per l'utilizzo dinamico.</span><span class="sxs-lookup"><span data-stu-id="eb252-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="eb252-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="eb252-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="eb252-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="eb252-112">Technologies</span></span>

-   [<span data-ttu-id="eb252-113">Procedura: creare una trama</span><span class="sxs-lookup"><span data-stu-id="eb252-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="eb252-114">Procedura: inizializzare una trama a livello di codice</span><span class="sxs-lookup"><span data-stu-id="eb252-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="eb252-115">Procedura: creare un buffer costante</span><span class="sxs-lookup"><span data-stu-id="eb252-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="eb252-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="eb252-116">Prerequisites</span></span>

<span data-ttu-id="eb252-117">Partiamo dal presupposto che tu abbia familiarità con C++.</span><span class="sxs-lookup"><span data-stu-id="eb252-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="eb252-118">Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.</span><span class="sxs-lookup"><span data-stu-id="eb252-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="eb252-119">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="eb252-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="eb252-120">Passaggio 1: specificare l'utilizzo dinamico</span><span class="sxs-lookup"><span data-stu-id="eb252-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="eb252-121">Se si vuole che l'app sia in grado di apportare modifiche alle risorse, è necessario specificare tali risorse come dinamiche e scrivibili quando vengono create.</span><span class="sxs-lookup"><span data-stu-id="eb252-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="eb252-122">**Per specificare l'utilizzo dinamico**</span><span class="sxs-lookup"><span data-stu-id="eb252-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="eb252-123">Specificare l'utilizzo delle risorse come dinamico.</span><span class="sxs-lookup"><span data-stu-id="eb252-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="eb252-124">Ad esempio, specificare il [**valore \_ \_ dinamico utilizzo d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) nel membro **Usage** di [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) per un vertex o un buffer costante e specificare il valore **\_ \_ dinamico utilizzo d3d11** nel membro **Usage** di [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) per una trama 2D.</span><span class="sxs-lookup"><span data-stu-id="eb252-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="eb252-125">Specificare la risorsa come scrivibile.</span><span class="sxs-lookup"><span data-stu-id="eb252-125">Specify the resource as writable.</span></span> <span data-ttu-id="eb252-126">Ad esempio, specificare il valore di [**scrittura di \_ accesso alla CPU \_ \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) nel membro **CPUAccessFlags** di [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) o [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span><span class="sxs-lookup"><span data-stu-id="eb252-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="eb252-127">Passare la descrizione della risorsa alla funzione di creazione.</span><span class="sxs-lookup"><span data-stu-id="eb252-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="eb252-128">Ad esempio, passare l'indirizzo del [**\_ buffer D3D11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e passare l'indirizzo di [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span><span class="sxs-lookup"><span data-stu-id="eb252-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="eb252-129">Di seguito è riportato un esempio di creazione di un buffer dei vertici dinamici:</span><span class="sxs-lookup"><span data-stu-id="eb252-129">Here is an example of creating a dynamic vertex buffer:</span></span>


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



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="eb252-130">Passaggio 2: modificare una risorsa dinamica</span><span class="sxs-lookup"><span data-stu-id="eb252-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="eb252-131">Se una risorsa è stata specificata come dinamica e scrivibile quando è stata creata, è possibile apportare modifiche in un secondo momento a tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb252-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="eb252-132">**Per modificare i dati in una risorsa dinamica**</span><span class="sxs-lookup"><span data-stu-id="eb252-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="eb252-133">Configurare i nuovi dati per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb252-133">Set up the new data for the resource.</span></span> <span data-ttu-id="eb252-134">Dichiarare una variabile di tipo [**\_ \_ sottorisorsa con mapping di d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inizializzarla su zero.</span><span class="sxs-lookup"><span data-stu-id="eb252-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="eb252-135">Questa variabile verrà usata per modificare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb252-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="eb252-136">Disabilitare l'accesso alla GPU (Graphics Processing Unit) ai dati che si desidera modificare e ottenere un puntatore alla memoria che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="eb252-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="eb252-137">Per ottenere questo puntatore, passare [**d3d11 \_ Map \_ Write \_ scarti**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) al parametro *MapType* quando si chiama [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="eb252-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="eb252-138">Impostare questo puntatore sull'indirizzo della variabile della [**\_ \_ sottorisorsa mappata d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) dal passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="eb252-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="eb252-139">Scrivere i nuovi dati nella memoria.</span><span class="sxs-lookup"><span data-stu-id="eb252-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="eb252-140">Chiamare [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) per riabilitare l'accesso alla GPU ai dati al termine della scrittura dei nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="eb252-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="eb252-141">Ecco un esempio di modifica di un buffer dei vertici dinamici:</span><span class="sxs-lookup"><span data-stu-id="eb252-141">Here is an example of changing a dynamic vertex buffer:</span></span>


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



## <a name="remarks"></a><span data-ttu-id="eb252-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb252-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="eb252-143">Uso di trame dinamiche</span><span class="sxs-lookup"><span data-stu-id="eb252-143">Using dynamic textures</span></span>

<span data-ttu-id="eb252-144">Si consiglia di creare una sola trama dinamica per ogni formato e possibilmente per dimensione.</span><span class="sxs-lookup"><span data-stu-id="eb252-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="eb252-145">Non è consigliabile creare mipmap, cubi e volumi dinamici a causa del sovraccarico aggiuntivo nel mapping di ogni livello.</span><span class="sxs-lookup"><span data-stu-id="eb252-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="eb252-146">Per mipmap, è possibile specificare [**d3d11 \_ mapping \_ Write \_ scarti**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) solo al livello principale.</span><span class="sxs-lookup"><span data-stu-id="eb252-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="eb252-147">Tutti i livelli vengono eliminati eseguendo il mapping solo del primo livello.</span><span class="sxs-lookup"><span data-stu-id="eb252-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="eb252-148">Questo comportamento è identico per volumi e cubi.</span><span class="sxs-lookup"><span data-stu-id="eb252-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="eb252-149">Per i cubi, viene eseguito il mapping del primo livello e del volto 0.</span><span class="sxs-lookup"><span data-stu-id="eb252-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="eb252-150">Uso di buffer dinamici</span><span class="sxs-lookup"><span data-stu-id="eb252-150">Using dynamic buffers</span></span>

<span data-ttu-id="eb252-151">Quando si chiama [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) su un buffer di vertice statico mentre la GPU usa il buffer, si ottiene un calo significativo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb252-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="eb252-152">In questa situazione, **Map** deve attendere fino al termine della lettura dei dati vertex o index dal buffer prima che **Map** possa tornare all'app chiamante, causando un ritardo significativo.</span><span class="sxs-lookup"><span data-stu-id="eb252-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="eb252-153">La chiamata di **Map** e quindi il rendering da un buffer statico più volte per fotogramma impedisce inoltre alla GPU di memorizzare nel buffer i comandi di rendering perché devono terminare i comandi prima di restituire il puntatore della mappa.</span><span class="sxs-lookup"><span data-stu-id="eb252-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="eb252-154">Senza i comandi memorizzati nel buffer, la GPU rimane inattiva finché l'app non riempie il buffer dei vertici o degli indici e genera un comando di rendering.</span><span class="sxs-lookup"><span data-stu-id="eb252-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="eb252-155">Idealmente, i dati dei vertici o degli indici non cambiano mai, ma ciò non è sempre possibile.</span><span class="sxs-lookup"><span data-stu-id="eb252-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="eb252-156">Esistono molte situazioni in cui l'app deve modificare i dati dei vertici o degli indici ogni frame, probabilmente anche più volte per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="eb252-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="eb252-157">Per queste situazioni, è consigliabile creare il vertex buffer o index buffer con [**d3d11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="eb252-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="eb252-158">Questo flag di utilizzo determina l'ottimizzazione del runtime per operazioni di mapping frequenti.</span><span class="sxs-lookup"><span data-stu-id="eb252-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="eb252-159">**D3d11 \_ \_Dynamic Usage** è utile solo quando il buffer è mappato di frequente; Se i dati devono rimanere costanti, inserire i dati in un vertex buffer statico o indice.</span><span class="sxs-lookup"><span data-stu-id="eb252-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="eb252-160">Per ottenere un miglioramento delle prestazioni quando si usano i buffer dei vertici dinamici, l'app deve chiamare [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) con i valori di [**\_ mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) appropriati.</span><span class="sxs-lookup"><span data-stu-id="eb252-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="eb252-161">[**D3d11 \_ Lo \_ \_ scarto di scrittura della mappa**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica che l'app non deve conservare i dati del vertice o dell'indice precedente nel buffer.</span><span class="sxs-lookup"><span data-stu-id="eb252-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="eb252-162">Se la GPU sta ancora usando il buffer quando si chiama **Map** con **l' \_ \_ \_ eliminazione della scrittura della mappa d3d11**, il runtime restituisce un puntatore a una nuova area di memoria anziché ai dati del buffer obsoleti.</span><span class="sxs-lookup"><span data-stu-id="eb252-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="eb252-163">Questo consente alla GPU di continuare a usare i dati obsoleti mentre l'app inserisce i dati nel nuovo buffer.</span><span class="sxs-lookup"><span data-stu-id="eb252-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="eb252-164">Nell'app non è necessaria alcuna gestione della memoria aggiuntiva. il buffer precedente viene riutilizzato o eliminato automaticamente al termine della GPU.</span><span class="sxs-lookup"><span data-stu-id="eb252-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="eb252-165">Quando si esegue il mapping di un buffer con lo [**\_ scarto di \_ scrittura \_ della mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), il runtime elimina sempre l'intero buffer.</span><span class="sxs-lookup"><span data-stu-id="eb252-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="eb252-166">Non è possibile mantenere le informazioni nelle aree non mappate del buffer specificando un campo offset diverso da zero o dimensioni limitate.</span><span class="sxs-lookup"><span data-stu-id="eb252-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="eb252-167">Esistono casi in cui la quantità di dati che l'app deve archiviare per ogni mappa è ridotta, ad esempio l'aggiunta di quattro vertici per il rendering di uno sprite.</span><span class="sxs-lookup"><span data-stu-id="eb252-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="eb252-168">[**D3d11 \_ MAP \_ Write \_ No \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) overwrite indica che l'app non sovrascriverà i dati già in uso nel buffer dinamico.</span><span class="sxs-lookup"><span data-stu-id="eb252-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="eb252-169">La chiamata della [**mappa**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) restituirà un puntatore ai dati obsoleti, che consentirà all'app di aggiungere nuovi dati in aree inutilizzate del vertex buffer o dell'indice.</span><span class="sxs-lookup"><span data-stu-id="eb252-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="eb252-170">L'app non deve modificare i vertici o gli indici usati in un'operazione di estrazione, perché potrebbero essere ancora in uso dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="eb252-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="eb252-171">È consigliabile che l'app usi quindi [**lo \_ \_ \_ scarto di scrittura della mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) dopo che il buffer dinamico è pieno per ricevere una nuova area di memoria, che elimina il vertice o i dati di indice precedenti al termine della GPU.</span><span class="sxs-lookup"><span data-stu-id="eb252-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="eb252-172">Il meccanismo di query asincrono è utile per determinare se i vertici sono ancora in uso dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="eb252-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="eb252-173">Eseguire una query di tipo [**\_ \_ evento di query d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) dopo l'ultima chiamata di progetto che usa i vertici.</span><span class="sxs-lookup"><span data-stu-id="eb252-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="eb252-174">I vertici non vengono più usati quando [**sul ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb252-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="eb252-175">Quando si esegue il mapping di un buffer con l' [**\_ \_ \_ eliminazione della mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o senza valori della mappa, si garantisce sempre che i vertici vengano sincronizzati correttamente con la GPU.</span><span class="sxs-lookup"><span data-stu-id="eb252-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="eb252-176">Tuttavia, quando si esegue il mapping senza valori della mappa, si comporterà la riduzione delle prestazioni descritta in precedenza.</span><span class="sxs-lookup"><span data-stu-id="eb252-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="eb252-177">Il runtime Direct3D 11,1, disponibile a partire da Windows 8, Abilita il mapping dei buffer costanti dinamici e delle visualizzazioni delle risorse dello shader (SRVs) dei buffer dinamici con la [**\_ mappa d3d11 \_ \_ senza \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="eb252-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="eb252-178">I runtime Direct3D 11 e versioni precedenti hanno limitato la sovrascrittura del mapping di aggiornamento parziale ai buffer vertex o index.</span><span class="sxs-lookup"><span data-stu-id="eb252-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="eb252-179">Per determinare se un dispositivo Direct3D supporta queste funzionalità, chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**le \_ \_ \_ Opzioni della funzionalità d3d11 di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="eb252-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="eb252-180">**CheckFeatureSupport** riempie i membri di una struttura di [**\_ \_ \_ \_ Opzioni d3d11 di dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) con le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb252-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="eb252-181">I membri pertinenti sono **MapNoOverwriteOnDynamicConstantBuffer** e **MapNoOverwriteOnDynamicBufferSRV**.</span><span class="sxs-lookup"><span data-stu-id="eb252-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eb252-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb252-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb252-183">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="eb252-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





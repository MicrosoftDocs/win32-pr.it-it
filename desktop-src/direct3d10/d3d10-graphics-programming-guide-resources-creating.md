---
description: Per la creazione di buffer è necessario definire i dati archiviati nel buffer, fornire dati di inizializzazione e impostare i flag di utilizzo e di associazione appropriati. Per creare trame, vedere Creazione di risorse di trama (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Creazione di risorse buffer (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748514"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="160ec-104">Creazione di risorse buffer (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="160ec-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="160ec-105">Per la creazione di buffer è necessario definire i dati archiviati nel buffer, fornire dati di inizializzazione e impostare i flag di utilizzo e di associazione appropriati.</span><span class="sxs-lookup"><span data-stu-id="160ec-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="160ec-106">Per creare trame, vedere [creazione di risorse di trama (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="160ec-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="160ec-107">Creare un buffer vertici</span><span class="sxs-lookup"><span data-stu-id="160ec-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="160ec-108">Creare una descrizione del buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="160ec-109">Creare i dati di inizializzazione per il buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="160ec-110">Creare il buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="160ec-111">Creazione di un buffer di indice</span><span class="sxs-lookup"><span data-stu-id="160ec-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="160ec-112">Creare un buffer costante</span><span class="sxs-lookup"><span data-stu-id="160ec-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="160ec-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="160ec-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="160ec-114">Creare un buffer vertici</span><span class="sxs-lookup"><span data-stu-id="160ec-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="160ec-115">Di seguito sono riportati i passaggi per la creazione di un [buffer vertex](d3d10-graphics-programming-guide-resources-types.md) .</span><span class="sxs-lookup"><span data-stu-id="160ec-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="160ec-116">Creare una descrizione del buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="160ec-117">Creare i dati di inizializzazione per il buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="160ec-118">Creare il buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="160ec-119">Creare una descrizione del buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-119">Create a Buffer Description</span></span>

<span data-ttu-id="160ec-120">Quando si crea un vertex buffer, viene usata una descrizione del buffer (vedere [**D3D10 \_ buffer \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) per definire la modalità di organizzazione dei dati all'interno del buffer, il modo in cui la pipeline può accedere al buffer e il modo in cui verrà usato il buffer.</span><span class="sxs-lookup"><span data-stu-id="160ec-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="160ec-121">Nell'esempio seguente viene illustrato come creare una descrizione del buffer per un singolo triangolo con vertici che contengono valori di posizione e colore.</span><span class="sxs-lookup"><span data-stu-id="160ec-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="160ec-122">In questo esempio la descrizione del buffer viene inizializzata con quasi tutte le impostazioni predefinite per l' [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**l'accesso alla CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) e i [**flag varie**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="160ec-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="160ec-123">Le altre impostazioni sono per il [**flag di binding**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) che identifica la risorsa solo come buffer dei vertici e le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="160ec-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="160ec-124">I flag di utilizzo e di accesso alla CPU sono importanti per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="160ec-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="160ec-125">Questi due flag determinano la frequenza con cui viene eseguito l'accesso a una risorsa, il tipo di memoria in cui è possibile caricare la risorsa e il processore che deve accedere alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="160ec-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="160ec-126">Utilizzo predefinito questa risorsa non verrà aggiornata molto spesso.</span><span class="sxs-lookup"><span data-stu-id="160ec-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="160ec-127">Se si imposta l'accesso alla CPU su 0, la CPU non dovrà leggere o scrivere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="160ec-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="160ec-128">In combinazione, questo significa che il runtime può caricare la risorsa nella memoria più elevata per la GPU, perché la risorsa non richiede l'accesso alla CPU.</span><span class="sxs-lookup"><span data-stu-id="160ec-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="160ec-129">Come previsto, esiste un compromesso tra prestazioni ottimali e accessibilità in qualsiasi momento da parte del processore.</span><span class="sxs-lookup"><span data-stu-id="160ec-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="160ec-130">Ad esempio, l'utilizzo predefinito senza accesso alla CPU significa che la risorsa può essere resa disponibile esclusivamente alla GPU.</span><span class="sxs-lookup"><span data-stu-id="160ec-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="160ec-131">Questo potrebbe includere il caricamento della risorsa in memoria non direttamente accessibile dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="160ec-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="160ec-132">La risorsa può essere modificata solo con [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span><span class="sxs-lookup"><span data-stu-id="160ec-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="160ec-133">Creare i dati di inizializzazione per il buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="160ec-134">Un buffer è semplicemente una raccolta di elementi ed è disposto come matrice 1D.</span><span class="sxs-lookup"><span data-stu-id="160ec-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="160ec-135">Di conseguenza, il pitch della memoria di sistema e il passo della sezione della memoria di sistema sono uguali; dimensione della dichiarazione dei dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="160ec-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="160ec-136">Un'applicazione può fornire dati di inizializzazione quando viene creato un buffer usando una [**Descrizione della sottorisorsa**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), che contiene un puntatore ai dati della risorsa effettivi e contiene informazioni sulle dimensioni e sul layout dei dati.</span><span class="sxs-lookup"><span data-stu-id="160ec-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="160ec-137">Qualsiasi buffer creato con utilizzo non modificabile (vedere l' [**utilizzo di D3D10 non \_ \_ modificabile**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) deve essere inizializzato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="160ec-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="160ec-138">I buffer che usano uno qualsiasi degli altri flag di utilizzo possono essere aggiornati dopo l'inizializzazione usando [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)e [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)oppure accedendo alla relativa memoria sottostante usando il metodo [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .</span><span class="sxs-lookup"><span data-stu-id="160ec-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="160ec-139">Creare il buffer</span><span class="sxs-lookup"><span data-stu-id="160ec-139">Create the Buffer</span></span>

<span data-ttu-id="160ec-140">Utilizzando la descrizione del buffer e i dati di inizializzazione (facoltativo), chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) per creare un buffer vertex.</span><span class="sxs-lookup"><span data-stu-id="160ec-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="160ec-141">Il frammento di codice seguente illustra come creare un buffer vertex da una matrice di dati vertex dichiarata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="160ec-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="160ec-142">Creazione di un buffer di indice</span><span class="sxs-lookup"><span data-stu-id="160ec-142">Create an Index Buffer</span></span>

<span data-ttu-id="160ec-143">La creazione di un buffer di indice è molto simile alla creazione di un buffer vertex; con due differenze.</span><span class="sxs-lookup"><span data-stu-id="160ec-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="160ec-144">Un buffer di indice contiene solo dati a 16 bit o a 32 bit, anziché l'ampia gamma di formati disponibili per un buffer di vertici.</span><span class="sxs-lookup"><span data-stu-id="160ec-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="160ec-145">Un buffer di indice richiede anche un flag di binding del buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="160ec-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="160ec-146">Nell'esempio seguente viene illustrato come creare un buffer di indice da una matrice di dati di indice.</span><span class="sxs-lookup"><span data-stu-id="160ec-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="160ec-147">Creare un buffer costante</span><span class="sxs-lookup"><span data-stu-id="160ec-147">Create a Constant Buffer</span></span>

<span data-ttu-id="160ec-148">Direct3D 10 introduce un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="160ec-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="160ec-149">Un buffer costante o un buffer costante dello shader è un buffer che contiene costanti shader.</span><span class="sxs-lookup"><span data-stu-id="160ec-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="160ec-150">Di seguito è riportato un esempio di creazione di un buffer costante, tratto dall' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="160ec-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="160ec-151">Si noti che quando si usa l'interfaccia [**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , il processo di creazione, associazione e invio di un buffer costante viene gestito dall'istanza dell' **interfaccia ID3D10Effect** .</span><span class="sxs-lookup"><span data-stu-id="160ec-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="160ec-152">In tal caso, è solo nescesary ottenere la variabile dall'effetto con uno dei metodi GetVariable, ad esempio [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , e aggiornare la variabile con uno dei metodi sevariable, ad esempio [**sematrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span><span class="sxs-lookup"><span data-stu-id="160ec-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="160ec-153">Per un esempio di utilizzo dell' **interfaccia ID3D10Effect** per la gestione di un buffer costante [, vedere Esercitazione 7: mapping di trame e buffer costanti](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="160ec-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="160ec-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="160ec-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="160ec-155">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="160ec-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




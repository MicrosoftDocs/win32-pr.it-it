---
description: Una risorsa di trama è una raccolta strutturata di dati.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Creazione di risorse di trama (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966170"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="ba0c1-103">Creazione di risorse di trama (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ba0c1-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="ba0c1-104">Una risorsa di [trama](d3d10-graphics-programming-guide-resources-types.md) è una raccolta strutturata di dati.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="ba0c1-105">In genere, i valori dei colori vengono archiviati in trame ed è possibile accedervi durante il rendering da parte della [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) in varie fasi sia per l'input che per l'output.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="ba0c1-106">La creazione di trame e la definizione del modo in cui verranno usate è una parte importante del rendering di scene interessanti in Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="ba0c1-107">Anche se le trame contengono in genere informazioni sul colore, la creazione di trame con un [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) diverso consente loro di archiviare tipi diversi di dati.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="ba0c1-108">Questi dati possono quindi essere utilizzati dalla pipeline Direct3D 10 in modi non tradizionali.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="ba0c1-109">Tutte le trame hanno limiti sulla quantità di memoria utilizzata e sul numero di Texel in essi contenuti.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="ba0c1-110">Questi limiti sono specificati dalle [costanti di risorsa](d3d10-graphics-reference-resource-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="ba0c1-111">Creare una trama da un file</span><span class="sxs-lookup"><span data-stu-id="ba0c1-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="ba0c1-112">Crea trama e Visualizza separatamente</span><span class="sxs-lookup"><span data-stu-id="ba0c1-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="ba0c1-113">Crea trama e visualizza simultaneamente</span><span class="sxs-lookup"><span data-stu-id="ba0c1-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="ba0c1-114">Creazione di trame vuote</span><span class="sxs-lookup"><span data-stu-id="ba0c1-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="ba0c1-115">Rendering in una trama</span><span class="sxs-lookup"><span data-stu-id="ba0c1-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="ba0c1-116">Riempimento manuale delle trame</span><span class="sxs-lookup"><span data-stu-id="ba0c1-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="ba0c1-117">Più Rendertargets</span><span class="sxs-lookup"><span data-stu-id="ba0c1-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="ba0c1-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba0c1-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="ba0c1-119">Creare una trama da un file</span><span class="sxs-lookup"><span data-stu-id="ba0c1-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="ba0c1-120">La [libreria di utilità D3DX](d3d10-graphics-reference-d3dx10.md) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="ba0c1-121">Quando si crea una trama in Direct3D 10, è anche necessario creare una [vista](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="ba0c1-122">Una vista è un oggetto che indica al dispositivo la modalità di accesso a una trama durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="ba0c1-123">Il modo più comune per accedere a una trama consiste nel leggerlo usando uno [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="ba0c1-124">Una visualizzazione risorse shader indica a uno shader come leggere da una trama durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="ba0c1-125">Il tipo di visualizzazione che verrà utilizzato da una trama deve essere specificato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="ba0c1-126">La creazione di una trama e il caricamento dei dati iniziali possono essere eseguiti in due modi diversi: creare una trama e visualizzare separatamente oppure creare contemporaneamente la trama e la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="ba0c1-127">L'API fornisce entrambe le tecniche per poter scegliere la soluzione più adatta alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="ba0c1-128">Crea trama e Visualizza separatamente</span><span class="sxs-lookup"><span data-stu-id="ba0c1-128">Create Texture and View Separately</span></span>

<span data-ttu-id="ba0c1-129">Il modo più semplice per creare una trama consiste nel caricarlo da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="ba0c1-130">Per creare la trama, è sufficiente compilare una struttura e fornire il nome della trama a [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="ba0c1-131">La funzione D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) esegue tre operazioni: innanzitutto crea un oggetto trama Direct3D 10; in secondo luogo, legge il file di immagine di input; in terzo luogo, archivia i dati dell'immagine nell'oggetto texture.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="ba0c1-132">Nell'esempio precedente viene caricato un file BMP, ma la funzione può caricare un'ampia gamma di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="ba0c1-133">Il flag di binding indica che la trama verrà creata come una risorsa shader che consente a una fase dello shader di leggere dalla trama durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="ba0c1-134">Nell'esempio precedente non vengono specificati tutti i parametri di caricamento.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="ba0c1-135">In realtà, è spesso utile semplicemente azzerare i parametri di caricamento, in quanto ciò consente a D3DX di scegliere i valori appropriati in base all'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="ba0c1-136">Se si vuole che l'immagine di input determini tutti i parametri con cui viene creata la trama, è sufficiente specificare **null** per il parametro **loadInfo** come segue:</span><span class="sxs-lookup"><span data-stu-id="ba0c1-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="ba0c1-137">La specifica di **null** per le informazioni di caricamento è un collegamento semplice ma potente.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="ba0c1-138">Ora che è stata creata una trama, è necessario creare una visualizzazione delle risorse dello shader in modo che la trama possa essere associata come input a uno shader.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="ba0c1-139">Poiché [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) restituisce un puntatore a una risorsa e non un puntatore a una trama, è necessario determinare il tipo esatto di risorsa che è stata caricata, quindi è possibile creare una visualizzazione delle risorse dello shader usando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="ba0c1-140">Sebbene l'esempio precedente crei una visualizzazione della risorsa shader 2D, il codice per creare altri tipi di visualizzazione delle risorse shader è molto simile.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="ba0c1-141">Una fase di shader ora può usare questa trama come input.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="ba0c1-142">L'uso di [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) per creare una trama e la visualizzazione associata è un modo per preparare una trama da associare a una fase dello shader.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="ba0c1-143">Un altro modo per eseguire questa operazione consiste nel creare contemporaneamente la trama e la relativa visualizzazione, come illustrato nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="ba0c1-144">Crea trama e visualizza simultaneamente</span><span class="sxs-lookup"><span data-stu-id="ba0c1-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="ba0c1-145">Direct3D 10 richiede una visualizzazione di trama e una risorsa shader per leggere da una trama durante il Runtime.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="ba0c1-146">Poiché la creazione di una trama e di una visualizzazione risorse dello shader è un'attività molto comune, D3DX fornisce il [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="ba0c1-147">Con una singola chiamata di D3DX, vengono create sia la trama che la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="ba0c1-148">La funzionalità del parametro **loadInfo** è invariata. è possibile usarlo per personalizzare la modalità di creazione della trama oppure derivare i parametri necessari dal file di input specificando **null** per il parametro **loadInfo** .</span><span class="sxs-lookup"><span data-stu-id="ba0c1-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="ba0c1-149">L'oggetto [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) restituito dalla funzione [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) può essere usato in un secondo momento per recuperare l'interfaccia [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) originale, se necessaria.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="ba0c1-150">Questa operazione può essere eseguita chiamando il metodo [**getResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .</span><span class="sxs-lookup"><span data-stu-id="ba0c1-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="ba0c1-151">D3DX fornisce una singola funzione per la creazione di una trama e una visualizzazione delle risorse dello shader come convienience; è necessario decidere quale metodo di creazione di una trama e una visualizzazione si adatta meglio alle esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="ba0c1-152">Ora che si è appreso come creare una trama e la relativa visualizzazione delle risorse dello shader, nella sezione successiva verrà illustrato come è possibile campionare (leggere) da tale trama usando uno shader.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="ba0c1-153">Creazione di trame vuote</span><span class="sxs-lookup"><span data-stu-id="ba0c1-153">Creating Empty Textures</span></span>

<span data-ttu-id="ba0c1-154">Talvolta le applicazioni desiderano creare una trama e calcolare i dati da archiviare nella trama oppure utilizzare la [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) grafica per eseguire il rendering in questa trama e successivamente utilizzare i risultati in un'altra elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="ba0c1-155">Queste trame potrebbero essere aggiornate dalla pipeline grafica o dall'applicazione stessa, a seconda del tipo di [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) specificato per la trama al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="ba0c1-156">Rendering in una trama</span><span class="sxs-lookup"><span data-stu-id="ba0c1-156">Rendering to a texture</span></span>

<span data-ttu-id="ba0c1-157">Il caso più comune di creare una trama vuota da riempire con i dati durante il runtime è il caso in cui un'applicazione vuole eseguire il rendering in una trama e quindi usare i risultati dell'operazione di rendering in un passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="ba0c1-158">Le trame create con questo scopo devono specificare l' [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)predefinito.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="ba0c1-159">Nell'esempio di codice seguente viene creata una trama vuota che può essere sottoposta a rendering dalla pipeline e successivamente utilizzata come input per uno [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="ba0c1-160">Per creare la trama è necessario che l'applicazione specifichi alcune informazioni sulle proprietà che la trama avrà.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="ba0c1-161">La larghezza e l'altezza della trama nei Texel sono impostate su 256.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="ba0c1-162">Per questa destinazione di rendering, è sufficiente un singolo livello di mipmap.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="ba0c1-163">È necessaria una sola destinazione di rendering, quindi la dimensione della matrice è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="ba0c1-164">Ogni Texel contiene valori a virgola mobile a 4 32 bit, che possono essere usati per archiviare informazioni molto precise (vedere [**DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="ba0c1-165">È sufficiente un campione per pixel.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="ba0c1-166">L'utilizzo è impostato su predefinito perché consente la posizione più efficiente della destinazione di rendering in memoria.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="ba0c1-167">Infine, il fatto che la trama verrà associata come destinazione di rendering e verrà specificata una risorsa shader in momenti diversi.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="ba0c1-168">Non è possibile associare le trame per il rendering diretto della pipeline. usare una visualizzazione di destinazione di rendering, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="ba0c1-169">Il formato della visualizzazione di destinazione di rendering è semplicemente impostato sul formato della trama originale.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="ba0c1-170">Le informazioni nella risorsa devono essere interpretate come una trama 2D e si vuole usare solo il primo livello mipmap della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="ba0c1-171">Analogamente al modo in cui è necessario creare una visualizzazione di destinazione del rendering in modo che la destinazione di rendering possa essere associata per l'output alla pipeline, è necessario creare una visualizzazione della risorsa shader in modo che la destinazione di rendering possa essere associata alla pipeline come input.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="ba0c1-172">Nell'esempio di codice riportato di seguito viene illustrato questo.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="ba0c1-173">I parametri delle descrizioni delle visualizzazioni delle risorse shader sono molto simili a quelli delle descrizioni delle visualizzazioni di destinazione di rendering e sono stati scelti per gli stessi motivi.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="ba0c1-174">Riempimento manuale delle trame</span><span class="sxs-lookup"><span data-stu-id="ba0c1-174">Filling Textures Manually</span></span>

<span data-ttu-id="ba0c1-175">A volte le applicazioni desiderano calcolare i valori in fase di esecuzione, inserirli manualmente in una trama e quindi fare in modo che la [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) grafica usi questa trama in operazioni di rendering successive.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="ba0c1-176">A tale scopo, l'applicazione deve creare una trama vuota in modo tale da consentire alla CPU di accedere alla memoria sottostante.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="ba0c1-177">Questa operazione viene eseguita creando una trama dinamica e ottenendo l'accesso alla memoria sottostante chiamando un metodo specifico.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="ba0c1-178">Nell'esempio di codice seguente viene illustrato come eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="ba0c1-179">Si noti che il formato è impostato su un 32 bit per pixel, dove ogni componente è definito da 8 bit.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="ba0c1-180">Il parametro Usage è impostato su Dynamic mentre i flag di binding sono impostati per specificare che la trama sarà accessibile da uno shader.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="ba0c1-181">Il resto della descrizione della trama è simile alla creazione di una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="ba0c1-182">La chiamata della [**mappa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) consente all'applicazione di accedere alla memoria sottostante della trama.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="ba0c1-183">Il puntatore recuperato viene quindi utilizzato per riempire la trama con i dati.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="ba0c1-184">Questa operazione può essere visualizzata nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="ba0c1-185">Più Rendertargets</span><span class="sxs-lookup"><span data-stu-id="ba0c1-185">Multiple Rendertargets</span></span>

<span data-ttu-id="ba0c1-186">Fino a otto visualizzazioni di destinazione di rendering possono essere associate alla pipeline alla volta (con [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="ba0c1-187">Per ogni pixel (o ogni campione se è abilitato il campionamento multiplo), la fusione viene eseguita indipendentemente per ogni visualizzazione di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="ba0c1-188">Due delle variabili di stato di Blend-BlendEnable e RenderTargetWriteMask-sono matrici di otto, ogni membro della matrice corrisponde a una visualizzazione di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="ba0c1-189">Quando si usano più destinazioni di rendering, ogni destinazione di rendering deve essere lo stesso [tipo di risorsa](d3d10-graphics-programming-guide-resources-types.md) (buffer, trama 1D, matrice di trama 2D e così via) e deve avere la stessa dimensione (larghezza, altezza, profondità per le trame 3D e dimensioni della matrice per le matrici di trama).</span><span class="sxs-lookup"><span data-stu-id="ba0c1-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="ba0c1-190">Se le destinazioni di rendering sono multicampionate, devono avere lo stesso numero di campioni per pixel.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="ba0c1-191">Può essere attivo un solo buffer di stencil Depth, indipendentemente dal numero di destinazioni di rendering attive.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="ba0c1-192">Quando si usano le matrici di trama come destinazioni di rendering, tutte le dimensioni di visualizzazione devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="ba0c1-193">Non è necessario che le destinazioni di rendering abbiano lo stesso formato di trama.</span><span class="sxs-lookup"><span data-stu-id="ba0c1-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba0c1-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba0c1-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba0c1-195">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ba0c1-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 

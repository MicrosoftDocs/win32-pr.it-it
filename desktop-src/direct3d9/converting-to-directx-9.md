---
description: Le funzionalità seguenti sono state modificate in Microsoft Direct3D 9. Se si usano queste funzionalità, vedere le modifiche elencate di seguito per trasferire l'applicazione a Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Conversione in Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305057"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="e6729-104">Conversione in Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e6729-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="e6729-105">Le funzionalità seguenti sono state modificate in Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e6729-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="e6729-106">Se si usano queste funzionalità, vedere le modifiche elencate di seguito per trasferire l'applicazione a Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e6729-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="e6729-107">BaseVertexIndex modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="e6729-108">CreateImageSurface modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="e6729-109">D3DENUM \_ Nessuna \_ modifica a livello di WHQL \_</span><span class="sxs-lookup"><span data-stu-id="e6729-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="e6729-110">Crea modifiche alle risorse</span><span class="sxs-lookup"><span data-stu-id="e6729-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="e6729-111">EnumAdapterModes modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="e6729-112">Modifiche Get/SetStreamSource \_</span><span class="sxs-lookup"><span data-stu-id="e6729-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="e6729-113">Modifiche della qualità del campionamento multiplo</span><span class="sxs-lookup"><span data-stu-id="e6729-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="e6729-114">ResourceManagerDiscardBytes modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="e6729-115">SetSoftwareVertexProcessing modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="e6729-116">Modifiche al campionatore trama</span><span class="sxs-lookup"><span data-stu-id="e6729-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="e6729-117">Modifiche della dichiarazione vertici</span><span class="sxs-lookup"><span data-stu-id="e6729-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="e6729-118">Intervalli \_ e \_ modifiche SwapEffects \_</span><span class="sxs-lookup"><span data-stu-id="e6729-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="e6729-119">BaseVertexIndex modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="e6729-120">In DirectX 8. x, IDirect3DDevice8:: SetIndices richiede un puntatore al buffer di indice e un BaseVertexIndex per la posizione iniziale nel buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e6729-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="e6729-121">Un'applicazione che suddivide in batch oggetti diversi nel buffer dei vertici ha dovuto cambiare il buffer dell'indice (oppure effettuare una chiamata a IDirect3DDevice8:: SetIndices) prima di chiamare IDirect3DDevice8::D rawIndexedPrimitive.</span><span class="sxs-lookup"><span data-stu-id="e6729-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="e6729-122">In Direct3D 9, la posizione iniziale nel buffer vertex, *BaseVertexIndex*, è stata spostata in IDirect3DDevice9::D rawindexedprimitive e il tipo di dati è stato modificato da DWORD a int.</span><span class="sxs-lookup"><span data-stu-id="e6729-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="e6729-123">CreateImageSurface modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="e6729-124">IDirect3DDevice8:: CreateImageSurface è stato rinominato [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span><span class="sxs-lookup"><span data-stu-id="e6729-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="e6729-125">È stato aggiunto un parametro aggiuntivo che accetta un tipo D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="e6729-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="e6729-126">D3DPOOL \_ Scratch restituirà una superficie con caratteristiche identiche a una superficie creata da IDirect3DDevice8:: CreateImageSurface.</span><span class="sxs-lookup"><span data-stu-id="e6729-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="e6729-127">D3DPOOL \_ default è il pool appropriato da usare con [**StretchRect**](/windows/desktop/api) e [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span><span class="sxs-lookup"><span data-stu-id="e6729-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="e6729-128">D3DENUM \_ Nessuna \_ modifica a livello di WHQL \_</span><span class="sxs-lookup"><span data-stu-id="e6729-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="e6729-129">Le applicazioni devono ora richiedere in modo esplicito Microsoft Windows Hardware Quality Labs (WHQL) perché la risposta richiede tempo relativamente lungo (pochi secondi).</span><span class="sxs-lookup"><span data-stu-id="e6729-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="e6729-130">D3DENUM \_ non \_ \_ è stato rimosso alcun livello WHQL ed \_ \_ è stato aggiunto il livello di D3DENUM WHQL.</span><span class="sxs-lookup"><span data-stu-id="e6729-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="e6729-131">Crea modifiche alle risorse</span><span class="sxs-lookup"><span data-stu-id="e6729-131">Create Resource Changes</span></span>

<span data-ttu-id="e6729-132">Un handle è stato aggiunto a diversi metodi e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e6729-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="e6729-133">I metodi interessati includono:</span><span class="sxs-lookup"><span data-stu-id="e6729-133">The methods affected include:</span></span>

-   [<span data-ttu-id="e6729-134">**CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="e6729-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="e6729-135">**CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="e6729-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="e6729-136">**CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="e6729-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="e6729-137">**CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e6729-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="e6729-138">**CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e6729-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="e6729-139">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e6729-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="e6729-140">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="e6729-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="e6729-141">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="e6729-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="e6729-142">EnumAdapterModes modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="e6729-143">Il [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) ora accetta un D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="e6729-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="e6729-144">Il formato supporta un set di modalità di visualizzazione in espansione.</span><span class="sxs-lookup"><span data-stu-id="e6729-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="e6729-145">Per proteggere le applicazioni dall'enumerazione dei formati che non sono stati inventati quando l'applicazione è stata spedita, l'applicazione deve indicare a Direct3D il formato per le modalità di visualizzazione da enumerare.</span><span class="sxs-lookup"><span data-stu-id="e6729-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="e6729-146">La matrice di modalità di visualizzazione risultante si differenzia solo per larghezza, altezza e frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e6729-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="e6729-147">L'applicazione specifica un formato pixel e l'enumerazione è limitata a tali modalità di visualizzazione che corrispondono esattamente al formato.</span><span class="sxs-lookup"><span data-stu-id="e6729-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="e6729-148">Di seguito è riportato un elenco dei formati consentiti:</span><span class="sxs-lookup"><span data-stu-id="e6729-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="e6729-149">\_A1R5G5B5 D3DFMT</span><span class="sxs-lookup"><span data-stu-id="e6729-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="e6729-150">\_A2B10G10R10 D3DFMT</span><span class="sxs-lookup"><span data-stu-id="e6729-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="e6729-151">\_A8R8G8B8 D3DFMT</span><span class="sxs-lookup"><span data-stu-id="e6729-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="e6729-152">\_R5G6B5 D3DFMT</span><span class="sxs-lookup"><span data-stu-id="e6729-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="e6729-153">\_X1R5G5B5 D3DFMT</span><span class="sxs-lookup"><span data-stu-id="e6729-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="e6729-154">\_X8R8G8B8 D3DFMT</span><span class="sxs-lookup"><span data-stu-id="e6729-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="e6729-155">L'enumerazione è equivalente per le versioni alfa e non Alpha dello stesso formato.</span><span class="sxs-lookup"><span data-stu-id="e6729-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="e6729-156">Il formato restituito verrà sempre riempito con lo stesso formato fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6729-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="e6729-157">Questo metodo considera 565 e 555 come equivalente e restituisce la versione corretta nel formato.</span><span class="sxs-lookup"><span data-stu-id="e6729-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="e6729-158">La differenza entra in gioco solo quando l'applicazione blocca il buffer nascosto ed esiste un flag esplicito che l'applicazione deve impostare per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e6729-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="e6729-159">Modifiche Get/SetStreamSource</span><span class="sxs-lookup"><span data-stu-id="e6729-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="e6729-160">È stato aggiunto un parametro ai metodi [**GetStreamSource**](/windows/desktop/api) e [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) .</span><span class="sxs-lookup"><span data-stu-id="e6729-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="e6729-161">L'offset è il numero di byte tra l'inizio del flusso e l'inizio dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="e6729-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="e6729-162">È misurata in byte.</span><span class="sxs-lookup"><span data-stu-id="e6729-162">It is measured in bytes.</span></span> <span data-ttu-id="e6729-163">Ciò consente alla pipeline di supportare gli offset del flusso.</span><span class="sxs-lookup"><span data-stu-id="e6729-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="e6729-164">Per sapere se il dispositivo supporta gli offset del flusso, vedere D3DDEVCAPS2 \_ STREAMOFFSET.</span><span class="sxs-lookup"><span data-stu-id="e6729-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="e6729-165">Modifiche della qualità del campionamento multiplo</span><span class="sxs-lookup"><span data-stu-id="e6729-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="e6729-166">In precedenza era presente solo l' \_ enumerazione del tipo D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="e6729-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="e6729-167">Direct3D 9 mantiene questa enumerazione e aggiunge l'idea di un livello di qualità per ogni elemento dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e6729-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="e6729-168">Il livello di qualità indica un compromesso tra qualità e prestazioni visive indicante il numero di campioni mascherabili (nel senso di D3DRS \_ MULTISAMPLEMASK).</span><span class="sxs-lookup"><span data-stu-id="e6729-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="e6729-169">Un'applicazione deve scegliere il numero di campioni mascherabili necessari e quindi consultare pQualityLevels.</span><span class="sxs-lookup"><span data-stu-id="e6729-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="e6729-170">Se diverso da zero, questo valore indica il numero di livelli di qualità che l'applicazione può passare alle varie funzioni di creazione tramite MultiSampleQuality.</span><span class="sxs-lookup"><span data-stu-id="e6729-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="e6729-171">Poiché i driver espongono tutti gli schemi multisample come livelli di qualità in D3DMULTISAMPLE \_ non mascherabili, è possibile enumerare tutti gli schemi multicampionamento disponibili tramite questo tipo se l'applicazione non deve mascherare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="e6729-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="e6729-172">Il \_ bit D3DPRASTERCAPS STRETCHBLTMULTISAMPLE Caps è stato ritirato.</span><span class="sxs-lookup"><span data-stu-id="e6729-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="e6729-173">Questo bit utilizzato per indicare che il metodo di campionamento multiplo non supporta le maschere di scrittura e non può essere attivato e disattivato tra [**BeginScene**](/windows/desktop/api) e [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span><span class="sxs-lookup"><span data-stu-id="e6729-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="e6729-174">Questi metodi non mascherabili sono ora esposti tramite D3DMULTISAMPLE non \_ mascherabile.</span><span class="sxs-lookup"><span data-stu-id="e6729-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="e6729-175">Per ogni numero di campioni mascherabili è disponibile un valore massimo diverso.</span><span class="sxs-lookup"><span data-stu-id="e6729-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="e6729-176">Ad esempio, gli \_ \_ esempi di D3DMULTISAMPLE 4 potrebbero avere tre livelli di qualità, mentre gli esempi di D3DMULTISAMPLE \_ 2 \_ possono avere solo uno.</span><span class="sxs-lookup"><span data-stu-id="e6729-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="e6729-177">Esistono al massimo otto livelli di qualità per ogni numero di campioni mascherabili (il driver non è autorizzato a esprimere più).</span><span class="sxs-lookup"><span data-stu-id="e6729-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="e6729-178">La qualità varia da zero a ( \* pQualityLevels-1).</span><span class="sxs-lookup"><span data-stu-id="e6729-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="e6729-179">ResourceManagerDiscardBytes modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="e6729-180">ResourceManagerDiscardBytes è stato sostituito da IDirect3DDevice9:: EvictManagedResources.</span><span class="sxs-lookup"><span data-stu-id="e6729-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="e6729-181">Consente di rimuovere tutte le risorse, sia Direct3D che i driver.</span><span class="sxs-lookup"><span data-stu-id="e6729-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="e6729-182">Resource Manager viene ora consultato quando la creazione di una risorsa (gestita o non gestita) ha esito negativo perché la memoria video è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e6729-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="e6729-183">Al responsabile verrà automaticamente richiesto di liberare risorse sufficienti per la creazione.</span><span class="sxs-lookup"><span data-stu-id="e6729-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="e6729-184">In DirectX 8,0, non si tratta di un processo automatizzato.</span><span class="sxs-lookup"><span data-stu-id="e6729-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="e6729-185">SetSoftwareVertexProcessing modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="e6729-186">Un'applicazione può creare un dispositivo in modalità mista per usare l'elaborazione dei vertici software e hardware.</span><span class="sxs-lookup"><span data-stu-id="e6729-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="e6729-187">Per passare tra le due modalità di elaborazione dei vertici in DirectX 8. x, chiamare IDirect3DDevice8:: SetRenderState.</span><span class="sxs-lookup"><span data-stu-id="e6729-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="e6729-188">Questa operazione è stata sostituita con [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) per semplificare i problemi causati da blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="e6729-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="e6729-189">Questo nuovo metodo non viene registrato dai blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="e6729-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="e6729-190">Modifiche al campionatore trama</span><span class="sxs-lookup"><span data-stu-id="e6729-190">Texture Sampler Changes</span></span>

<span data-ttu-id="e6729-191">Direct3D 9 supporta fino a sedici superfici di trama in un unico passaggio usando il modello pixel shader 2 \_ 0. Tuttavia, il numero di coordinate di trama rimane limitato a otto.</span><span class="sxs-lookup"><span data-stu-id="e6729-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="e6729-192">Lo stato della fase trama è associato a superfici, set di coordinate, elaborazione dei vertici e elaborazione pixel.</span><span class="sxs-lookup"><span data-stu-id="e6729-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="e6729-193">Per gestire queste differenze in fase di compilazione, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) è stato suddiviso in due metodi:</span><span class="sxs-lookup"><span data-stu-id="e6729-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="e6729-194">IDirect3DDevice9:: SetTextureStageState verrà comunque utilizzato per lo stato della coordinata di trama, ad esempio le modalità a capo e la generazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="e6729-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="e6729-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) è stato aggiunto e verrà ora usato per filtrare, affiancare, bloccare, MIPLOD e così via.</span><span class="sxs-lookup"><span data-stu-id="e6729-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="e6729-196">Questa operazione funzionerà per un massimo di sedici esempi.</span><span class="sxs-lookup"><span data-stu-id="e6729-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="e6729-197">SetTextureStageState modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="e6729-198">IDirect3DDevice9:: SetTextureStageState ora imposta gli Stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6729-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="e6729-199">Stato di elaborazione vertice funzione fisso.</span><span class="sxs-lookup"><span data-stu-id="e6729-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="e6729-200">Questo stato controlla la manipolazione delle coordinate di trama D3DTSS \_ TEXTURETRANSFORMFLAGS e D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="e6729-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="e6729-201">È possibile impostare fino a otto, perché otto coordinate di trama sono sempre supportate.</span><span class="sxs-lookup"><span data-stu-id="e6729-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="e6729-202">D3DTSS \_ TEXCOORDINDEX è uno stato di elaborazione Vertex della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="e6729-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="e6729-203">Se viene usato un vertex shader programmabile, questo stato viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e6729-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="e6729-204">Funzione Fixed pixel shader stato (TextureStageState legacy).</span><span class="sxs-lookup"><span data-stu-id="e6729-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="e6729-205">\_ALPHAARG0 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="e6729-206">\_ALPHAARG1 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="e6729-207">\_ALPHAARG2 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="e6729-208">\_ALPHAOP D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="e6729-209">\_BUMPENVLOFFSET D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="e6729-210">\_BUMPENVLSCALE D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="e6729-211">\_BUMPENVMAT00 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="e6729-212">\_BUMPENVMAT01 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="e6729-213">\_BUMPENVMAT10 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="e6729-214">\_BUMPENVMAT11 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="e6729-215">\_COLORARG0 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="e6729-216">\_COLORARG1 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="e6729-217">\_COLORARG2 D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="e6729-218">\_COLOROP D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="e6729-219">\_RESULTARG D3DTSS</span><span class="sxs-lookup"><span data-stu-id="e6729-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="e6729-220">Il numero degli Stati pixel shader di funzione fissa che è possibile impostare è minore o uguale al numero rappresentato da MaxTextureBlendStages.</span><span class="sxs-lookup"><span data-stu-id="e6729-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="e6729-221">Il numero di campioni di trama disponibili per l'applicazione è determinato dalla versione pixel shader, come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e6729-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="e6729-222">Nome</span><span class="sxs-lookup"><span data-stu-id="e6729-222">Name</span></span>                    | <span data-ttu-id="e6729-223">Number</span><span class="sxs-lookup"><span data-stu-id="e6729-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6729-224">\_da PS 1 \_ 1 a PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e6729-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="e6729-225">4 campionatori trama</span><span class="sxs-lookup"><span data-stu-id="e6729-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="e6729-226">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="e6729-226">ps\_1\_4</span></span>                | <span data-ttu-id="e6729-227">6 esempi di trama</span><span class="sxs-lookup"><span data-stu-id="e6729-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="e6729-228">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6729-228">ps\_2\_0</span></span>                | <span data-ttu-id="e6729-229">16 Sampler trama</span><span class="sxs-lookup"><span data-stu-id="e6729-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="e6729-230">pipeline della funzione fissa</span><span class="sxs-lookup"><span data-stu-id="e6729-230">fixed function pipeline</span></span> | <span data-ttu-id="e6729-231">MaxTextureBlendStages/MaxSimultaneousTextures trama Samplers</span><span class="sxs-lookup"><span data-stu-id="e6729-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="e6729-232">I dispositivi che supportano il mapping di spostamento in Direct3D 9 supporteranno un campionatore aggiuntivo (D3DDMAPSAMPLER), che consente di campionare le mappe di spostamento nell'unità mosaico.</span><span class="sxs-lookup"><span data-stu-id="e6729-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="e6729-233">SetSamplerState modifiche</span><span class="sxs-lookup"><span data-stu-id="e6729-233">SetSamplerState Changes</span></span>

<span data-ttu-id="e6729-234">IDirect3DDevice9:: SetSamplerState imposta lo stato del campionatore (incluso quello usato nell'unità mosaico per eseguire il campionamento delle mappe di spostamento).</span><span class="sxs-lookup"><span data-stu-id="e6729-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="e6729-235">Questi sono stati rinominati con un \_ prefisso D3DSAMP per abilitare il rilevamento degli errori in fase di compilazione durante il porting da DirectX 8. x.</span><span class="sxs-lookup"><span data-stu-id="e6729-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="e6729-236">Gli stati includono:</span><span class="sxs-lookup"><span data-stu-id="e6729-236">The states include:</span></span>

-   <span data-ttu-id="e6729-237">\_Indirizzo D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="e6729-238">\_ADDRESSV D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="e6729-239">\_ADDRESSW D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="e6729-240">\_BorderColor D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="e6729-241">\_MAGFILTER D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="e6729-242">\_MAXANISOTROPY D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="e6729-243">\_MAXMIPLEVEL D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="e6729-244">\_MINFILTER D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="e6729-245">\_MIPFILTER D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="e6729-246">\_MIPMAPLODBIAS D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="e6729-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="e6729-247">Modifiche della dichiarazione vertici</span><span class="sxs-lookup"><span data-stu-id="e6729-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="e6729-248">Le dichiarazioni dei vertici sono ora disaccoppiate dalla creazione del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e6729-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="e6729-249">Le dichiarazioni Vertex ora usano un'interfaccia Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="e6729-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="e6729-250">Per DirectX 8. x, le dichiarazioni di vertice sono associate a vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e6729-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="e6729-251">Per la pipeline della funzione fissa, chiamare [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) con il codice FVF (Flexible Vertex Format) del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e6729-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="e6729-252">Per i vertex shader, chiamare IDirect3DDevice9:: SetVertexShader con un handle per un vertex shader creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e6729-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="e6729-253">Lo shader include una dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="e6729-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="e6729-254">Per Direct3D 9, le dichiarazioni dei vertici sono separate dai vertex shader e possono essere usate con la pipeline della funzione fissa o con gli shader.</span><span class="sxs-lookup"><span data-stu-id="e6729-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="e6729-255">Per la pipeline della funzione fixed, non è necessario chiamare IDirect3DDevice9:: SetVertexShader.</span><span class="sxs-lookup"><span data-stu-id="e6729-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="e6729-256">Se tuttavia si desidera passare alla pipeline della funzione fissa e in precedenza è stato utilizzato un vertex shader, chiamare IDirect3DDevice9:: SetVertexShader (**null**).</span><span class="sxs-lookup"><span data-stu-id="e6729-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="e6729-257">Al termine, sarà comunque necessario chiamare [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) per dichiarare il codice FVF.</span><span class="sxs-lookup"><span data-stu-id="e6729-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="e6729-258">Quando si usano vertex shader, chiamare IDirect3DDevice9:: SetVertexShader con l'oggetto vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e6729-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="e6729-259">Inoltre, chiamare IDirect3DDevice9:: SetFVF per impostare una dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="e6729-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="e6729-260">Questa operazione usa le informazioni implicite in FVF.</span><span class="sxs-lookup"><span data-stu-id="e6729-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="e6729-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) può essere chiamato al posto di IDirect3DDevice9:: SetFVF perché supporta le dichiarazioni dei vertici che non possono essere espresse con un FVF.</span><span class="sxs-lookup"><span data-stu-id="e6729-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="e6729-262">Intervalli e modifiche SwapEffects</span><span class="sxs-lookup"><span data-stu-id="e6729-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="e6729-263">Sono state apportate diverse modifiche per fornire all'utente un maggiore controllo sulla frequenza di aggiornamento del monitor, sulla velocità di presentazione e sul disegno di buffer back-buffer.</span><span class="sxs-lookup"><span data-stu-id="e6729-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="e6729-264">Ecco quali sono:</span><span class="sxs-lookup"><span data-stu-id="e6729-264">They are as follows:</span></span>

-   <span data-ttu-id="e6729-265">Rimossi un effetto di swap, una \_ copia D3DSWAPEFFECT \_ vsync e una frequenza di presentazione, D3DPRESENT \_ rate \_ Unlimited.</span><span class="sxs-lookup"><span data-stu-id="e6729-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="e6729-266">Parametri D3DPRESENT rinominati \_ . \_PresentationInterval a schermo intero a PresentationIntervals.</span><span class="sxs-lookup"><span data-stu-id="e6729-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="e6729-267">Aggiunta \_ dell'intervallo \_ di D3DPRESENT immediate, il che significa che la presentazione non è sincronizzata con la sincronizzazione verticale. Come in DirectX 8. x, il \_ valore predefinito per l'intervallo di D3DPRESENT \_ è pari a zero ed è equivalente a D3DPRESENT \_ interval \_ One.</span><span class="sxs-lookup"><span data-stu-id="e6729-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="e6729-268">D3DPRESENT \_ interval \_ default è una praticità per l'inizializzazione dei \_ parametri D3DPRESENT su zero.</span><span class="sxs-lookup"><span data-stu-id="e6729-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="e6729-269">Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="e6729-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6729-270">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6729-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6729-271">Grafica Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e6729-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 

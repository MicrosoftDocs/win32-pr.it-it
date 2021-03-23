---
title: Carichi UAV (unordered Access View) tipizzati
description: Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548818"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="3a619-103">Carichi UAV (unordered Access View) tipizzati</span><span class="sxs-lookup"><span data-stu-id="3a619-103">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="3a619-104">Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)specifico.</span><span class="sxs-lookup"><span data-stu-id="3a619-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="3a619-105">Overview</span><span class="sxs-lookup"><span data-stu-id="3a619-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="3a619-106">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="3a619-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="3a619-107">Uso dei caricamenti UAV tipizzati da HLSL</span><span class="sxs-lookup"><span data-stu-id="3a619-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="3a619-108">Uso di UNORM e di un UAV tipizzato da HLSL</span><span class="sxs-lookup"><span data-stu-id="3a619-108">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="3a619-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a619-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="3a619-110">Panoramica</span><span class="sxs-lookup"><span data-stu-id="3a619-110">Overview</span></span>

<span data-ttu-id="3a619-111">Una visualizzazione di accesso non ordinato (UAV) è una vista di una risorsa di accesso non ordinato (che può includere buffer, trame e matrici di trama, sebbene senza campionamento multiplo).</span><span class="sxs-lookup"><span data-stu-id="3a619-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="3a619-112">Un UAV consente un accesso in lettura/scrittura temporaneamente non ordinato da più thread.</span><span class="sxs-lookup"><span data-stu-id="3a619-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="3a619-113">Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria.</span><span class="sxs-lookup"><span data-stu-id="3a619-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="3a619-114">Questo accesso simultaneo viene gestito tramite l'utilizzo di [funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="3a619-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="3a619-115">D3D12 (e D3D 11.3) si espande nell'elenco dei formati che possono essere usati con i caricamenti UAV tipizzati.</span><span class="sxs-lookup"><span data-stu-id="3a619-115">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="3a619-116">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="3a619-116">Supported formats and API calls</span></span>

<span data-ttu-id="3a619-117">In precedenza, i tre formati seguenti supportano i caricamenti UAV tipizzati e sono necessari per l'hardware D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="3a619-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="3a619-118">Sono supportati per tutti i componenti hardware di D3D 11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="3a619-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="3a619-119">\_Float R32</span><span class="sxs-lookup"><span data-stu-id="3a619-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="3a619-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-120">R32\_UINT</span></span>
-   <span data-ttu-id="3a619-121">R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-121">R32\_SINT</span></span>

<span data-ttu-id="3a619-122">I formati seguenti sono supportati come set nell'hardware D3D12 o D3D 11.3, quindi se ne è supportato uno tutti sono supportati.</span><span class="sxs-lookup"><span data-stu-id="3a619-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="3a619-123">\_Float R32G32B32A32</span><span class="sxs-lookup"><span data-stu-id="3a619-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="3a619-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="3a619-125">R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="3a619-126">\_Float R16G16B16A16</span><span class="sxs-lookup"><span data-stu-id="3a619-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="3a619-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="3a619-128">R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="3a619-129">\_UNORM R8G8B8A8</span><span class="sxs-lookup"><span data-stu-id="3a619-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="3a619-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="3a619-131">R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="3a619-132">\_Float R16</span><span class="sxs-lookup"><span data-stu-id="3a619-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="3a619-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-133">R16\_UINT</span></span>
-   <span data-ttu-id="3a619-134">R16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-134">R16\_SINT</span></span>
-   <span data-ttu-id="3a619-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="3a619-135">R8\_UNORM</span></span>
-   <span data-ttu-id="3a619-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-136">R8\_UINT</span></span>
-   <span data-ttu-id="3a619-137">R8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-137">R8\_SINT</span></span>

<span data-ttu-id="3a619-138">I formati seguenti sono facoltativamente supportati individualmente nell'hardware D3D12 e D3D 11.3, quindi è necessario eseguire una singola query su ogni formato per verificare il supporto.</span><span class="sxs-lookup"><span data-stu-id="3a619-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="3a619-139">\_UNORM R16G16B16A16</span><span class="sxs-lookup"><span data-stu-id="3a619-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="3a619-140">R16G16B16A16 \_ russare</span><span class="sxs-lookup"><span data-stu-id="3a619-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="3a619-141">\_Float R32G32</span><span class="sxs-lookup"><span data-stu-id="3a619-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="3a619-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="3a619-143">R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="3a619-144">\_UNORM R10G10B10A2</span><span class="sxs-lookup"><span data-stu-id="3a619-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="3a619-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="3a619-146">\_Float R11G11B10</span><span class="sxs-lookup"><span data-stu-id="3a619-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="3a619-147">R8G8B8A8 \_ russare</span><span class="sxs-lookup"><span data-stu-id="3a619-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="3a619-148">\_Float R16G16</span><span class="sxs-lookup"><span data-stu-id="3a619-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="3a619-149">\_UNORM R16G16</span><span class="sxs-lookup"><span data-stu-id="3a619-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="3a619-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="3a619-151">R16G16 \_ russare</span><span class="sxs-lookup"><span data-stu-id="3a619-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="3a619-152">R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="3a619-153">\_UNORM R8G8</span><span class="sxs-lookup"><span data-stu-id="3a619-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="3a619-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="3a619-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="3a619-155">R8G8 \_ russare</span><span class="sxs-lookup"><span data-stu-id="3a619-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="3a619-156">R8G8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="3a619-156">R8G8\_SINT</span></span>
-   <span data-ttu-id="3a619-157">\_UNORM R16</span><span class="sxs-lookup"><span data-stu-id="3a619-157">R16\_UNORM</span></span>
-   <span data-ttu-id="3a619-158">R16 \_ russare</span><span class="sxs-lookup"><span data-stu-id="3a619-158">R16\_SNORM</span></span>
-   <span data-ttu-id="3a619-159">R8 \_ russamento</span><span class="sxs-lookup"><span data-stu-id="3a619-159">R8\_SNORM</span></span>
-   <span data-ttu-id="3a619-160">\_UNORM a8</span><span class="sxs-lookup"><span data-stu-id="3a619-160">A8\_UNORM</span></span>
-   <span data-ttu-id="3a619-161">\_UNORM B5G6R5</span><span class="sxs-lookup"><span data-stu-id="3a619-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="3a619-162">\_UNORM B5G5R5A1</span><span class="sxs-lookup"><span data-stu-id="3a619-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="3a619-163">\_UNORM B4G4R4A4</span><span class="sxs-lookup"><span data-stu-id="3a619-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="3a619-164">Per determinare il supporto per qualsiasi formato aggiuntivo, chiamare [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la struttura di [**\_ \_ \_ \_ Opzioni D3D12 dei dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) come primo parametro (vedere l'articolo relativo all' [esecuzione di query sulle funzionalità](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="3a619-164">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="3a619-165">Il campo *TypedUAVLoadAdditionalFormats* verrà impostato se è supportato l'elenco "supportato come set".</span><span class="sxs-lookup"><span data-stu-id="3a619-165">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="3a619-166">Eseguire una seconda chiamata a **CheckFeatureSupport**, usando una struttura di [**\_ \_ \_ \_ supporto del formato dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (controllando la struttura restituita rispetto al \_ formato D3D12 SUPPORT2 il \_ \_ \_ \_ membro di caricamento tipizzato UAV del [**\_ formato \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) per determinare il supporto nell'elenco dei formati eventualmente supportati sopra indicati, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="3a619-166">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="3a619-167">Uso dei caricamenti UAV tipizzati da HLSL</span><span class="sxs-lookup"><span data-stu-id="3a619-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="3a619-168">Per i UAV tipizzati, il flag HLSL è D3D \_ shader \_ richiede un \_ UAV tipizzato per \_ \_ caricare \_ \_ formati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3a619-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="3a619-169">Di seguito è riportato un esempio di codice shader per elaborare un carico di UAV tipizzato:</span><span class="sxs-lookup"><span data-stu-id="3a619-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="3a619-170">Uso di UNORM e di un UAV tipizzato da HLSL</span><span class="sxs-lookup"><span data-stu-id="3a619-170">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="3a619-171">Quando si usano i caricamenti UAV tipizzati per leggere da una risorsa UNORM o RUSSAr, è necessario dichiarare correttamente il tipo di elemento dell'oggetto HLSL come `unorm` o `snorm` .</span><span class="sxs-lookup"><span data-stu-id="3a619-171">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="3a619-172">Viene specificato come comportamento non definito in modo che non corrisponda al tipo di elemento dichiarato in HLSL con il tipo di dati della risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="3a619-172">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="3a619-173">Ad esempio, se si usano i caricamenti UAV tipizzati in una risorsa di buffer con \_ i dati di R8 UNORM, è necessario dichiarare il tipo di elemento come `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="3a619-173">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="3a619-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a619-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a619-175">Rendering</span><span class="sxs-lookup"><span data-stu-id="3a619-175">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="3a619-176">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="3a619-176">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="3a619-177">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="3a619-177">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="3a619-178">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="3a619-178">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="3a619-179">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="3a619-179">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
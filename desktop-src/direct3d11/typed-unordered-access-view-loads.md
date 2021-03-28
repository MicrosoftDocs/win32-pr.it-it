---
title: Caricamenti Unordered Access View tipizzati
description: Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0958b3563ab8001fd7b34ae62c9bcc37ad75c07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337902"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="e77a5-103">Caricamenti Unordered Access View tipizzati</span><span class="sxs-lookup"><span data-stu-id="e77a5-103">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="e77a5-104">Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .</span><span class="sxs-lookup"><span data-stu-id="e77a5-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="e77a5-105">Overview</span><span class="sxs-lookup"><span data-stu-id="e77a5-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="e77a5-106">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="e77a5-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="e77a5-107">Uso dei caricamenti UAV tipizzati da HLSL</span><span class="sxs-lookup"><span data-stu-id="e77a5-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="e77a5-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e77a5-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e77a5-109">Panoramica</span><span class="sxs-lookup"><span data-stu-id="e77a5-109">Overview</span></span>

<span data-ttu-id="e77a5-110">Una visualizzazione di accesso non ordinato (UAV) è una vista di una risorsa di accesso non ordinato (che può includere buffer, trame e matrici di trama, sebbene senza campionamento multiplo).</span><span class="sxs-lookup"><span data-stu-id="e77a5-110">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="e77a5-111">Un UAV consente un accesso in lettura/scrittura temporaneamente non ordinato da più thread.</span><span class="sxs-lookup"><span data-stu-id="e77a5-111">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="e77a5-112">Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria.</span><span class="sxs-lookup"><span data-stu-id="e77a5-112">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="e77a5-113">Questo accesso simultaneo viene gestito tramite l'utilizzo di [funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="e77a5-113">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="e77a5-114">D3D12 e D3D 11.3 si espande nell'elenco dei formati che possono essere usati con i caricamenti UAV tipizzati.</span><span class="sxs-lookup"><span data-stu-id="e77a5-114">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="e77a5-115">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="e77a5-115">Supported formats and API calls</span></span>

<span data-ttu-id="e77a5-116">In precedenza, i tre formati seguenti supportano i caricamenti UAV tipizzati e sono necessari per l'hardware D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="e77a5-116">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="e77a5-117">Sono supportati per tutti i componenti hardware di D3D 11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="e77a5-117">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="e77a5-118">\_Float R32</span><span class="sxs-lookup"><span data-stu-id="e77a5-118">R32\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-119">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-119">R32\_UINT</span></span>
-   <span data-ttu-id="e77a5-120">R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-120">R32\_SINT</span></span>

<span data-ttu-id="e77a5-121">I formati seguenti sono supportati come set nell'hardware D3D12 o D3D 11.3, quindi se ne è supportato uno tutti sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e77a5-121">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="e77a5-122">\_Float R32G32B32A32</span><span class="sxs-lookup"><span data-stu-id="e77a5-122">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-123">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-123">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="e77a5-124">R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-124">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="e77a5-125">\_Float R16G16B16A16</span><span class="sxs-lookup"><span data-stu-id="e77a5-125">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-126">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-126">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="e77a5-127">R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-127">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="e77a5-128">\_UNORM R8G8B8A8</span><span class="sxs-lookup"><span data-stu-id="e77a5-128">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="e77a5-129">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-129">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="e77a5-130">R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-130">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="e77a5-131">\_Float R16</span><span class="sxs-lookup"><span data-stu-id="e77a5-131">R16\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-132">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-132">R16\_UINT</span></span>
-   <span data-ttu-id="e77a5-133">R16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-133">R16\_SINT</span></span>
-   <span data-ttu-id="e77a5-134">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e77a5-134">R8\_UNORM</span></span>
-   <span data-ttu-id="e77a5-135">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-135">R8\_UINT</span></span>
-   <span data-ttu-id="e77a5-136">R8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-136">R8\_SINT</span></span>

<span data-ttu-id="e77a5-137">I formati seguenti sono facoltativamente supportati individualmente nell'hardware D3D12 e D3D 11.3, quindi è necessario eseguire una singola query su ogni formato per verificare il supporto.</span><span class="sxs-lookup"><span data-stu-id="e77a5-137">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="e77a5-138">\_UNORM R16G16B16A16</span><span class="sxs-lookup"><span data-stu-id="e77a5-138">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="e77a5-139">R16G16B16A16 \_ russare</span><span class="sxs-lookup"><span data-stu-id="e77a5-139">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="e77a5-140">\_Float R32G32</span><span class="sxs-lookup"><span data-stu-id="e77a5-140">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-141">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-141">R32G32\_UINT</span></span>
-   <span data-ttu-id="e77a5-142">R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-142">R32G32\_SINT</span></span>
-   <span data-ttu-id="e77a5-143">\_UNORM R10G10B10A2</span><span class="sxs-lookup"><span data-stu-id="e77a5-143">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="e77a5-144">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-144">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="e77a5-145">\_Float R11G11B10</span><span class="sxs-lookup"><span data-stu-id="e77a5-145">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-146">R8G8B8A8 \_ russare</span><span class="sxs-lookup"><span data-stu-id="e77a5-146">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="e77a5-147">\_Float R16G16</span><span class="sxs-lookup"><span data-stu-id="e77a5-147">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="e77a5-148">\_UNORM R16G16</span><span class="sxs-lookup"><span data-stu-id="e77a5-148">R16G16\_UNORM</span></span>
-   <span data-ttu-id="e77a5-149">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-149">R16G16\_UINT</span></span>
-   <span data-ttu-id="e77a5-150">R16G16 \_ russare</span><span class="sxs-lookup"><span data-stu-id="e77a5-150">R16G16\_SNORM</span></span>
-   <span data-ttu-id="e77a5-151">R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-151">R16G16\_SINT</span></span>
-   <span data-ttu-id="e77a5-152">\_UNORM R8G8</span><span class="sxs-lookup"><span data-stu-id="e77a5-152">R8G8\_UNORM</span></span>
-   <span data-ttu-id="e77a5-153">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e77a5-153">R8G8\_UINT</span></span>
-   <span data-ttu-id="e77a5-154">R8G8 \_ russare</span><span class="sxs-lookup"><span data-stu-id="e77a5-154">R8G8\_SNORM</span></span>
-   <span data-ttu-id="e77a5-155">8G8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="e77a5-155">8G8\_SINT</span></span>
-   <span data-ttu-id="e77a5-156">\_UNORM R16</span><span class="sxs-lookup"><span data-stu-id="e77a5-156">R16\_UNORM</span></span>
-   <span data-ttu-id="e77a5-157">R16 \_ russare</span><span class="sxs-lookup"><span data-stu-id="e77a5-157">R16\_SNORM</span></span>
-   <span data-ttu-id="e77a5-158">R8 \_ russamento</span><span class="sxs-lookup"><span data-stu-id="e77a5-158">R8\_SNORM</span></span>
-   <span data-ttu-id="e77a5-159">\_UNORM a8</span><span class="sxs-lookup"><span data-stu-id="e77a5-159">A8\_UNORM</span></span>
-   <span data-ttu-id="e77a5-160">\_UNORM B5G6R5</span><span class="sxs-lookup"><span data-stu-id="e77a5-160">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="e77a5-161">\_UNORM B5G5R5A1</span><span class="sxs-lookup"><span data-stu-id="e77a5-161">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="e77a5-162">\_UNORM B4G4R4A4</span><span class="sxs-lookup"><span data-stu-id="e77a5-162">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="e77a5-163">Per determinare il supporto per qualsiasi formato aggiuntivo, chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con i [**\_ dati della funzionalità d3d11 d3d11 struttura \_ \_ \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="e77a5-163">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="e77a5-164">Il `TypedUAVLoadAdditionalFormats` bit verrà impostato se è supportato l'elenco "supportato come set".</span><span class="sxs-lookup"><span data-stu-id="e77a5-164">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="e77a5-165">Eseguire una seconda chiamata a **CheckFeatureSupport**, usando una [**struttura \_ \_ SUPPORT2 del \_ formato \_ dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (controllando la struttura restituita rispetto al formato D3D12 \_ SUPPORT2 il \_ \_ \_ membro di caricamento tipizzato UAV \_ del [**\_ formato \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) d3d11 enum) per determinare il supporto nell'elenco di formati eventualmente supportati, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e77a5-165">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="e77a5-166">Uso dei caricamenti UAV tipizzati da HLSL</span><span class="sxs-lookup"><span data-stu-id="e77a5-166">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="e77a5-167">Per i UAV tipizzati, il flag HLSL è D3D \_ shader \_ richiede un \_ UAV tipizzato per \_ \_ caricare \_ \_ formati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e77a5-167">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="e77a5-168">Di seguito è riportato un esempio di codice shader per elaborare un carico di UAV tipizzato:</span><span class="sxs-lookup"><span data-stu-id="e77a5-168">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="e77a5-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e77a5-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e77a5-170">Funzionalità di Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="e77a5-170">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="e77a5-171">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="e77a5-171">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
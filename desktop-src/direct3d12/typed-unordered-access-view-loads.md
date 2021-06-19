---
title: Caricamento della visualizzazione di accesso non ordinato (UAV) tipi
description: Informazioni sul carico Unordered Access View (UAV) in Direct3D 12. Il caricamento tipidato UAV consente a uno shader di leggere da un UAV con un DXGI_FORMAT.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394766"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="d77ff-104">Caricamento della visualizzazione di accesso non ordinato (UAV) tipi</span><span class="sxs-lookup"><span data-stu-id="d77ff-104">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="d77ff-105">Unordered Access View (UAV) Typed Load è la possibilità per uno shader di leggere da un UAV con un formato [**DXGI \_ specifico.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="d77ff-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="d77ff-106">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d77ff-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="d77ff-107">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="d77ff-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="d77ff-108">Uso dei caricamenti UAV tipiati da HLSL</span><span class="sxs-lookup"><span data-stu-id="d77ff-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="d77ff-109">Uso dei caricamenti UAV tipiati UNORM e SNORM da HLSL</span><span class="sxs-lookup"><span data-stu-id="d77ff-109">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="d77ff-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d77ff-110">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d77ff-111">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d77ff-111">Overview</span></span>

<span data-ttu-id="d77ff-112">Una visualizzazione di accesso non ordinato (UAV) è una visualizzazione di una risorsa di accesso non ordinata (che può includere buffer, trame e matrici di trame, anche se senza campionamento multiplo).</span><span class="sxs-lookup"><span data-stu-id="d77ff-112">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="d77ff-113">Un UAV consente l'accesso in lettura/scrittura non ordinato a livello temporale da più thread.</span><span class="sxs-lookup"><span data-stu-id="d77ff-113">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="d77ff-114">Questo significa che questo tipo di risorsa può essere letto/scritto contemporaneamente da più thread senza generare conflitti di memoria.</span><span class="sxs-lookup"><span data-stu-id="d77ff-114">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="d77ff-115">Questo accesso simultaneo viene gestito tramite l'uso di [Funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="d77ff-115">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="d77ff-116">D3D12 (e D3D11.3) si espande nell'elenco dei formati che possono essere usati con carichi UAV tipici.</span><span class="sxs-lookup"><span data-stu-id="d77ff-116">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="d77ff-117">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="d77ff-117">Supported formats and API calls</span></span>

<span data-ttu-id="d77ff-118">In precedenza, i tre formati seguenti supportavano i caricamenti UAV tipiati ed erano necessari per l'hardware D3D11.0.</span><span class="sxs-lookup"><span data-stu-id="d77ff-118">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="d77ff-119">Sono supportati per tutto l'hardware D3D11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="d77ff-119">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="d77ff-120">R32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-120">R32\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-121">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-121">R32\_UINT</span></span>
-   <span data-ttu-id="d77ff-122">R32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-122">R32\_SINT</span></span>

<span data-ttu-id="d77ff-123">I formati seguenti sono supportati come set nell'hardware D3D12 o D3D11.3, quindi se ne è supportato uno qualsiasi, sono supportati tutti.</span><span class="sxs-lookup"><span data-stu-id="d77ff-123">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="d77ff-124">R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-124">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-125">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-125">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="d77ff-126">R32G32B32A32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-126">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="d77ff-127">R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-127">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-128">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-128">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="d77ff-129">R16G16B16A16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-129">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="d77ff-130">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-130">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="d77ff-131">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-131">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="d77ff-132">R8G8B8A8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-132">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="d77ff-133">R16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-133">R16\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-134">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-134">R16\_UINT</span></span>
-   <span data-ttu-id="d77ff-135">R16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-135">R16\_SINT</span></span>
-   <span data-ttu-id="d77ff-136">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-136">R8\_UNORM</span></span>
-   <span data-ttu-id="d77ff-137">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-137">R8\_UINT</span></span>
-   <span data-ttu-id="d77ff-138">R8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-138">R8\_SINT</span></span>

<span data-ttu-id="d77ff-139">I formati seguenti sono supportati facoltativamente e singolarmente nell'hardware D3D12 e D3D11.3, quindi per testare il supporto è necessario eseguire una singola query su ogni formato.</span><span class="sxs-lookup"><span data-stu-id="d77ff-139">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="d77ff-140">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-140">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="d77ff-141">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-141">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="d77ff-142">R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-142">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-143">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-143">R32G32\_UINT</span></span>
-   <span data-ttu-id="d77ff-144">R32G32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-144">R32G32\_SINT</span></span>
-   <span data-ttu-id="d77ff-145">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-145">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="d77ff-146">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-146">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="d77ff-147">R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-147">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-148">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-148">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="d77ff-149">R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d77ff-149">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="d77ff-150">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-150">R16G16\_UNORM</span></span>
-   <span data-ttu-id="d77ff-151">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-151">R16G16\_UINT</span></span>
-   <span data-ttu-id="d77ff-152">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-152">R16G16\_SNORM</span></span>
-   <span data-ttu-id="d77ff-153">R16G16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-153">R16G16\_SINT</span></span>
-   <span data-ttu-id="d77ff-154">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-154">R8G8\_UNORM</span></span>
-   <span data-ttu-id="d77ff-155">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-155">R8G8\_UINT</span></span>
-   <span data-ttu-id="d77ff-156">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-156">R8G8\_SNORM</span></span>
-   <span data-ttu-id="d77ff-157">R8G8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="d77ff-157">R8G8\_SINT</span></span>
-   <span data-ttu-id="d77ff-158">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-158">R16\_UNORM</span></span>
-   <span data-ttu-id="d77ff-159">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-159">R16\_SNORM</span></span>
-   <span data-ttu-id="d77ff-160">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-160">R8\_SNORM</span></span>
-   <span data-ttu-id="d77ff-161">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-161">A8\_UNORM</span></span>
-   <span data-ttu-id="d77ff-162">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-162">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="d77ff-163">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-163">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="d77ff-164">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="d77ff-164">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="d77ff-165">Per determinare il supporto per eventuali formati aggiuntivi, chiamare [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con la struttura [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) come primo parametro (vedere [Capability Querying](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="d77ff-165">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="d77ff-166">Il *campo TypedUAVLoadAdditionalFormats* verrà impostato se è supportato l'elenco "supportato come set" precedente.</span><span class="sxs-lookup"><span data-stu-id="d77ff-166">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="d77ff-167">Eseguire una seconda chiamata a **CheckFeatureSupport** usando una struttura [**D3D12 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (verificando la struttura restituita rispetto al membro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD dell'enumerazione \_ \_ \_ \_ \_ [**D3D12 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) per determinare il supporto nell'elenco dei formati supportati elencati in precedenza, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d77ff-167">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="d77ff-168">Uso dei caricamenti UAV tipiati da HLSL</span><span class="sxs-lookup"><span data-stu-id="d77ff-168">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="d77ff-169">Per le UAV tipive, il flag HLSL è D3D SHADER REQUIRES TYPED UAV LOAD ADDITIONAL FORMATS (RICHIEDE FORMATI AGGIUNTIVI DI CARICAMENTO \_ \_ \_ \_ UAV \_ \_ \_ TIPISTI).</span><span class="sxs-lookup"><span data-stu-id="d77ff-169">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="d77ff-170">Di seguito è riportato un esempio di codice shader per elaborare un carico UAV tipiato:</span><span class="sxs-lookup"><span data-stu-id="d77ff-170">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="d77ff-171">Uso dei caricamenti UAV tipiati UNORM e SNORM da HLSL</span><span class="sxs-lookup"><span data-stu-id="d77ff-171">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="d77ff-172">Quando si usano caricamenti UAV tipiati per la lettura da una risorsa UNORM o SNORM, è necessario dichiarare correttamente il tipo di elemento dell'oggetto HLSL come `unorm` o `snorm` .</span><span class="sxs-lookup"><span data-stu-id="d77ff-172">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="d77ff-173">Viene specificato come comportamento non definito per non trovare la corrispondenza tra il tipo di elemento dichiarato in HLSL e il tipo di dati della risorsa sottostante.</span><span class="sxs-lookup"><span data-stu-id="d77ff-173">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="d77ff-174">Ad esempio, se si usa il caricamento UAV tipiato in una risorsa buffer con dati R8 UNORM, è necessario dichiarare il tipo di elemento \_ come `unorm float` :</span><span class="sxs-lookup"><span data-stu-id="d77ff-174">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="d77ff-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d77ff-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d77ff-176">Rendering</span><span class="sxs-lookup"><span data-stu-id="d77ff-176">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="d77ff-177">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="d77ff-177">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="d77ff-178">Associazione di risorse in HLSL</span><span class="sxs-lookup"><span data-stu-id="d77ff-178">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="d77ff-179">Modello shader 5.1</span><span class="sxs-lookup"><span data-stu-id="d77ff-179">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="d77ff-180">Specifica delle firme radice in HLSL</span><span class="sxs-lookup"><span data-stu-id="d77ff-180">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
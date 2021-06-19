---
title: Carichi Unordered Access View tipi
description: Informazioni sul Unordered Access View (UAV) in Direct3D 11. Il caricamento tipidato UAV consente a uno shader di leggere da un UAV con un DXGI_FORMAT.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396286"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="2d50d-104">Carichi Unordered Access View tipi</span><span class="sxs-lookup"><span data-stu-id="2d50d-104">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="2d50d-105">Unordered Access View (UAV) Typed Load è la possibilità per uno shader di leggere da un UAV con un formato DXGI \_ specifico.</span><span class="sxs-lookup"><span data-stu-id="2d50d-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="2d50d-106">Panoramica</span><span class="sxs-lookup"><span data-stu-id="2d50d-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="2d50d-107">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="2d50d-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="2d50d-108">Uso dei caricamenti UAV tipiati da HLSL</span><span class="sxs-lookup"><span data-stu-id="2d50d-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="2d50d-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d50d-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="2d50d-110">Panoramica</span><span class="sxs-lookup"><span data-stu-id="2d50d-110">Overview</span></span>

<span data-ttu-id="2d50d-111">Una visualizzazione di accesso non ordinato (UAV) è una visualizzazione di una risorsa di accesso non ordinata (che può includere buffer, trame e matrici di trame, anche se senza campionamento multiplo).</span><span class="sxs-lookup"><span data-stu-id="2d50d-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="2d50d-112">Un UAV consente l'accesso in lettura/scrittura non ordinato a livello temporale da più thread.</span><span class="sxs-lookup"><span data-stu-id="2d50d-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="2d50d-113">Questo significa che questo tipo di risorsa può essere letto/scritto contemporaneamente da più thread senza generare conflitti di memoria.</span><span class="sxs-lookup"><span data-stu-id="2d50d-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="2d50d-114">Questo accesso simultaneo viene gestito tramite l'uso di [Funzioni atomiche](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="2d50d-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="2d50d-115">D3D12 e D3D11.3 si espandono nell'elenco dei formati che è possibile usare con carichi UAV tipici.</span><span class="sxs-lookup"><span data-stu-id="2d50d-115">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="2d50d-116">Formati supportati e chiamate API</span><span class="sxs-lookup"><span data-stu-id="2d50d-116">Supported formats and API calls</span></span>

<span data-ttu-id="2d50d-117">In precedenza, i tre formati seguenti supportavano i caricamenti UAV tipiati ed erano necessari per l'hardware D3D11.0.</span><span class="sxs-lookup"><span data-stu-id="2d50d-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="2d50d-118">Sono supportati per tutto l'hardware D3D11.3 e D3D12.</span><span class="sxs-lookup"><span data-stu-id="2d50d-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="2d50d-119">R32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-120">R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-120">R32\_UINT</span></span>
-   <span data-ttu-id="2d50d-121">R32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-121">R32\_SINT</span></span>

<span data-ttu-id="2d50d-122">I formati seguenti sono supportati come set nell'hardware D3D12 o D3D11.3, quindi se ne è supportato uno qualsiasi, sono supportati tutti.</span><span class="sxs-lookup"><span data-stu-id="2d50d-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="2d50d-123">R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-124">R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="2d50d-125">R32G32B32A32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="2d50d-126">R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-127">R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="2d50d-128">R16G16B16A16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="2d50d-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="2d50d-130">R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="2d50d-131">R8G8B8A8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="2d50d-132">R16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-133">R16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-133">R16\_UINT</span></span>
-   <span data-ttu-id="2d50d-134">R16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-134">R16\_SINT</span></span>
-   <span data-ttu-id="2d50d-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-135">R8\_UNORM</span></span>
-   <span data-ttu-id="2d50d-136">R8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-136">R8\_UINT</span></span>
-   <span data-ttu-id="2d50d-137">R8 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-137">R8\_SINT</span></span>

<span data-ttu-id="2d50d-138">I formati seguenti sono supportati facoltativamente e singolarmente nell'hardware D3D12 e D3D11.3, quindi per testare il supporto è necessario eseguire una singola query su ogni formato.</span><span class="sxs-lookup"><span data-stu-id="2d50d-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="2d50d-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="2d50d-140">R16G16B16A16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="2d50d-141">R32G32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-142">R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="2d50d-143">R32G32 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="2d50d-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="2d50d-145">R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="2d50d-146">R11G11B10 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-147">R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="2d50d-148">R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="2d50d-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="2d50d-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="2d50d-150">R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="2d50d-151">R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="2d50d-152">R16G16 \_ SINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="2d50d-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="2d50d-154">R8G8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="2d50d-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="2d50d-155">R8G8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="2d50d-156">SINT 8G8 \_</span><span class="sxs-lookup"><span data-stu-id="2d50d-156">8G8\_SINT</span></span>
-   <span data-ttu-id="2d50d-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-157">R16\_UNORM</span></span>
-   <span data-ttu-id="2d50d-158">R16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-158">R16\_SNORM</span></span>
-   <span data-ttu-id="2d50d-159">R8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-159">R8\_SNORM</span></span>
-   <span data-ttu-id="2d50d-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-160">A8\_UNORM</span></span>
-   <span data-ttu-id="2d50d-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="2d50d-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="2d50d-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="2d50d-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="2d50d-164">Per determinare il supporto per eventuali formati aggiuntivi, chiamare [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la struttura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="2d50d-164">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="2d50d-165">Il `TypedUAVLoadAdditionalFormats` bit verrà impostato se è supportato l'elenco "supportato come set" precedente.</span><span class="sxs-lookup"><span data-stu-id="2d50d-165">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="2d50d-166">Eseguire una seconda chiamata a **CheckFeatureSupport** usando una struttura [**D3D11 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) (verificando la struttura restituita rispetto al membro D3D12 FORMAT SUPPORT2 UAV TYPED LOAD dell'enumerazione \_ \_ \_ \_ \_ [**D3D11 \_ FORMAT \_ SUPPORT2)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) per determinare il supporto nell'elenco dei formati supportati in precedenza, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2d50d-166">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

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

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="2d50d-167">Uso dei caricamenti UAV tipiati da HLSL</span><span class="sxs-lookup"><span data-stu-id="2d50d-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="2d50d-168">Per le UAV tipive, il flag HLSL è D3D SHADER REQUIRES TYPED UAV LOAD ADDITIONAL FORMATS (RICHIEDE FORMATI AGGIUNTIVI DI CARICAMENTO \_ \_ \_ \_ UAV \_ \_ \_ TIPISTI).</span><span class="sxs-lookup"><span data-stu-id="2d50d-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="2d50d-169">Di seguito è riportato un esempio di codice shader per elaborare un carico UAV tipiato:</span><span class="sxs-lookup"><span data-stu-id="2d50d-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="2d50d-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d50d-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d50d-171">Funzionalità di Direct3D 11.3</span><span class="sxs-lookup"><span data-stu-id="2d50d-171">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="2d50d-172">Modello shader 5.1</span><span class="sxs-lookup"><span data-stu-id="2d50d-172">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
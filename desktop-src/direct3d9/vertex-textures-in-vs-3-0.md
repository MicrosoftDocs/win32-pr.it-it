---
description: Il modello vertex shader 3,0 supporta la ricerca di trame nel vertex shader usando l'istruzione texldl-vs texture Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Trame di vertici in vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747159"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="5db0a-103">Trame di vertici in vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5db0a-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="5db0a-104">Il modello vertex shader 3,0 supporta la ricerca di trame nel vertex shader usando l'istruzione [texldl-vs](../direct3dhlsl/texldl---vs.md) texture Load.</span><span class="sxs-lookup"><span data-stu-id="5db0a-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="5db0a-105">Il motore Vertex contiene quattro fasi del campionatore di trama, denominate [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 e D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="5db0a-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="5db0a-106">Sono distinti dal campionatore della mappa di spostamento e dagli esempi di trama nel motore di pixel.</span><span class="sxs-lookup"><span data-stu-id="5db0a-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="5db0a-107">Per eseguire il campionamento delle trame in queste quattro fasi, è possibile usare il motore di Vertex e programmare le fasi con il metodo [**CheckDeviceFormat**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="5db0a-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5db0a-108">Impostare le trame in tali fasi usando la [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)con l'indice della fase [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) tramite D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="5db0a-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="5db0a-109">Nel vertex shader è stato introdotto un nuovo registro, ovvero il registro del campionatore, come in PS \_ 2 \_ 0, che rappresenta il campionatore di trame dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5db0a-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="5db0a-110">Questo registro deve essere definito nello shader prima di usarlo.</span><span class="sxs-lookup"><span data-stu-id="5db0a-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="5db0a-111">Un'applicazione può eseguire una query se un formato è supportato come trama del vertice chiamando [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ query \_ VERTEXTEXTURE](d3dusage-query.md).</span><span class="sxs-lookup"><span data-stu-id="5db0a-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="5db0a-112">Si tratta di un flag di query in modo che non venga accettato in alcuna funzione CreateXXX.</span><span class="sxs-lookup"><span data-stu-id="5db0a-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="5db0a-113">Una trama del vertice creata nel pool predefinito può essere impostata come trama in pixel e viceversa.</span><span class="sxs-lookup"><span data-stu-id="5db0a-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="5db0a-114">Tuttavia, per usare l'elaborazione dei vertici software, è necessario creare la trama del vertice nel pool di Scratch (indipendentemente dal fatto che si tratta di un dispositivo in modalità mista o di un dispositivo di elaborazione dei vertici software).</span><span class="sxs-lookup"><span data-stu-id="5db0a-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="5db0a-115">La funzionalità è identica alle trame in pixel, ad eccezione di quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5db0a-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="5db0a-116">Il filtro di trama anisotropico non è supportato, di conseguenza D3DSAMP \_ MAXANISOTROPY viene ignorato e \_ non è possibile impostare D3DTEXF anisotropico per ingrandire o minimizzare per queste fasi.</span><span class="sxs-lookup"><span data-stu-id="5db0a-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="5db0a-117">La frequenza delle informazioni sulle modifiche non è disponibile, di conseguenza l'applicazione deve calcolare il livello di dettaglio e fornire tali informazioni come parametro a [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="5db0a-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="5db0a-118">Tali restrizioni includono:</span><span class="sxs-lookup"><span data-stu-id="5db0a-118">Restrictions include:</span></span>

-   <span data-ttu-id="5db0a-119">Come nei pixel shader, se sono supportate le trame a più elementi, \_ viene usato D3DSAMP ELEMENTINDEX per determinare l'elemento da campionare.</span><span class="sxs-lookup"><span data-stu-id="5db0a-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="5db0a-120">Lo stato D3DSAMP \_ DMAPOFFSET viene ignorato per queste fasi.</span><span class="sxs-lookup"><span data-stu-id="5db0a-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="5db0a-121">Usare [**CheckDeviceFormat**](/windows/desktop/api) con [D3DUSAGE \_ query \_ VERTEXTEXTURE "](d3dusage-query.md) per eseguire una query su una trama per verificare se può essere usata come trama del vertice.</span><span class="sxs-lookup"><span data-stu-id="5db0a-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="5db0a-122">VertexTextureFilterCaps indica il tipo di filtro consentito nei campioni di trama dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5db0a-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="5db0a-123">[D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) e D3DPTFILTERCAPS \_ MAGFANISOTROPIC non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="5db0a-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="5db0a-124">Registri fasi di campionamento</span><span class="sxs-lookup"><span data-stu-id="5db0a-124">Sampling Stage Registers</span></span>

<span data-ttu-id="5db0a-125">Un registro della fase di campionamento identifica un'unità di campionamento che può essere usata nelle istruzioni per il caricamento di trame.</span><span class="sxs-lookup"><span data-stu-id="5db0a-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="5db0a-126">Un'unità di campionamento corrisponde alla fase di campionamento della trama, che incapsula lo stato specifico del campionamento fornito in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="5db0a-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="5db0a-127">Ogni campionatore identifica in modo univoco una singola superficie di trama impostata sul campionatore corrispondente usando la [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="5db0a-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="5db0a-128">Tuttavia, la stessa superficie di trama può essere impostata su più Sampler.</span><span class="sxs-lookup"><span data-stu-id="5db0a-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="5db0a-129">In fase di disegnare non è possibile impostare contemporaneamente una trama come destinazione di rendering e una trama in una fase.</span><span class="sxs-lookup"><span data-stu-id="5db0a-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="5db0a-130">Poiché vs \_ 3 \_ 0 supporta quattro campionatori, è possibile leggere fino a quattro superfici di trama in un unico passaggio dello shader.</span><span class="sxs-lookup"><span data-stu-id="5db0a-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="5db0a-131">Un registro campionatore può apparire solo come argomento nell'istruzione Load di trama: [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="5db0a-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="5db0a-132">In vs \_ 3 \_ 0, se si usa un campionatore, è necessario dichiararlo all'inizio del programma shader, usando [DCL \_ samplerType (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (come in PS \_ 2 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="5db0a-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="5db0a-133">Elaborazione software</span><span class="sxs-lookup"><span data-stu-id="5db0a-133">Software Processing</span></span>

<span data-ttu-id="5db0a-134">Questa funzionalità sarà supportata nell'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="5db0a-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="5db0a-135">I tipi di filtro specifici supportati possono essere controllati chiamando [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) e controllando VertexTextureFilterCaps.</span><span class="sxs-lookup"><span data-stu-id="5db0a-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="5db0a-136">Tutti i formati di trama pubblicati saranno supportati come trame di vertici nell'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="5db0a-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="5db0a-137">Le applicazioni possono verificare se un particolare formato di trama è supportato nella modalità di elaborazione dei vertici software chiamando [**CheckDeviceFormat**](/windows/desktop/api) e specificando (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) come utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5db0a-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="5db0a-138">Tutti i formati sono supportati per l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="5db0a-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="5db0a-139">Il pool di Scratch è necessario per l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="5db0a-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="5db0a-140">Modifiche API</span><span class="sxs-lookup"><span data-stu-id="5db0a-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="5db0a-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5db0a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5db0a-142">Pipeline Vertex</span><span class="sxs-lookup"><span data-stu-id="5db0a-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 

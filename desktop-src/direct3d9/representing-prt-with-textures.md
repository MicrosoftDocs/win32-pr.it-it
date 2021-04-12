---
description: L'esempio PRTDemo e il simulatore PRTCmdLine incluso in DirectX SDK rappresentano i vettori di trasferimento ai vertici di una rete mesh.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Rappresentazione di PRT con trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225472"
---
# <a name="representing-prt-with-textures-direct3d-9"></a><span data-ttu-id="ea527-103">Rappresentazione di PRT con trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ea527-103">Representing PRT With Textures (Direct3D 9)</span></span>

<span data-ttu-id="ea527-104">L'esempio PRTDemo e il simulatore PRTCmdLine incluso in DirectX SDK rappresentano i vettori di trasferimento ai vertici di una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="ea527-104">The PRTDemo sample and PRTCmdLine simulator included in the DirectX SDK represent transfer vectors at the vertices of a mesh.</span></span> <span data-ttu-id="ea527-105">Per rappresentare accuratamente il segnale PRT, può essere necessario tassellature che può risultare poco pratico per i giochi correnti.</span><span class="sxs-lookup"><span data-stu-id="ea527-105">In order to represent the PRT signal accurately, this can require tessellations that may be impractical for current games.</span></span> <span data-ttu-id="ea527-106">Rappresenta un approccio alternativo con lo stesso costo dei dati indipendente dalla complessità della rete.</span><span class="sxs-lookup"><span data-stu-id="ea527-106">Representing transfer vectors in texture maps is an alternative approach that has the same data cost independent of mesh complexity.</span></span> <span data-ttu-id="ea527-107">Esistono diversi modi per generare mappe di trame vettori di trasferimento usando la libreria PRT D3DX.</span><span class="sxs-lookup"><span data-stu-id="ea527-107">There are several ways to generate transfer vector texture maps using the D3DX PRT Library.</span></span>

## <a name="precomputing-transfer-vectors"></a><span data-ttu-id="ea527-108">Vettori di trasferimento per il precalcolo</span><span class="sxs-lookup"><span data-stu-id="ea527-108">Precomputing Transfer Vectors</span></span>

<span data-ttu-id="ea527-109">Un approccio consiste nel modificare gli esempi di PRTDemo e PRTCmdLine per calcolare un vettore di trasferimento a ogni Texel in una parametrizzazione di una superficie.</span><span class="sxs-lookup"><span data-stu-id="ea527-109">One approach would be to modify the PRTDemo and PRTCmdLine samples to compute a transfer vector at every texel in a parameterization of a surface.</span></span> <span data-ttu-id="ea527-110">Per eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="ea527-110">To do this:</span></span>

1.  <span data-ttu-id="ea527-111">Modificare la chiamata a [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) per estrarre le coordinate di trama dalla mesh (ExtractUVs deve essere **true**)</span><span class="sxs-lookup"><span data-stu-id="ea527-111">Modify the call to [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to extract texture coordinates from the mesh (ExtractUVs must be **TRUE**)</span></span>
2.  <span data-ttu-id="ea527-112">Sostituire le chiamate [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) usando le stesse dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="ea527-112">Replace [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) calls with [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) using the same texture size.</span></span>

<span data-ttu-id="ea527-113">Tutti i metodi ID3DXPRTEngine funzionano con le simulazioni per Texel, ad eccezione di: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS e ComputeDirectLightingSHAdaptive.</span><span class="sxs-lookup"><span data-stu-id="ea527-113">All ID3DXPRTEngine methods work with per-texel simulations except for: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS, and ComputeDirectLightingSHAdaptive.</span></span> <span data-ttu-id="ea527-114">Anche se la simulazione dello spazio di trama genera il risultato corretto, spesso può essere piuttosto lento poiché probabilmente sarà il calcolo dei vettori di trasferimento a densità elevata.</span><span class="sxs-lookup"><span data-stu-id="ea527-114">While texture-space simulation will generate the correct result, it can often be fairly slow since it will most likely be computing transfer vectors at a high density.</span></span>

<span data-ttu-id="ea527-115">Un altro approccio consiste nel calcolare una simulazione di PRT per un vertice adattivo (con coordinate di trama che verranno usate per i dati per Texel) e quindi chiamare [**ID3DXPRTEngine:: ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (usando un buffer di output creato con [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) alla risoluzione appropriata).</span><span class="sxs-lookup"><span data-stu-id="ea527-115">Another approach is to compute an adaptive per-vertex PRT simulation (with texture coordinates that will be used for the per-texel data) and then call [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (using an output buffer created using [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) at the appropriate resolution).</span></span> <span data-ttu-id="ea527-116">Funziona con tutte le funzionalità di D3DX PRT nell'SDK e spesso può essere molto più efficiente rispetto al calcolo diretto di un buffer di trasferimento per Texel.</span><span class="sxs-lookup"><span data-stu-id="ea527-116">This works with all D3DX PRT functionality in the SDK and can often be much more efficient than directly computing a per-texel transfer buffer.</span></span>

## <a name="runtime-calculations"></a><span data-ttu-id="ea527-117">Calcoli di runtime</span><span class="sxs-lookup"><span data-stu-id="ea527-117">Runtime Calculations</span></span>

<span data-ttu-id="ea527-118">Se viene usato un singolo cluster, i risultati possono essere filtrati e con mapping MIP come qualsiasi altra trama e il pixel shader è identico al codice del vertex shader fornito con PRTDemo.</span><span class="sxs-lookup"><span data-stu-id="ea527-118">If a single cluster is used the results can be filtered and mip-mapped like any other texture and the pixel shader is identical to the vertex shader code that ships with PRTDemo.</span></span>

<span data-ttu-id="ea527-119">Se la compressione genera più cluster, non è possibile filtrare o mipmap i dati perché gli indici clustering non sono continui.</span><span class="sxs-lookup"><span data-stu-id="ea527-119">If compression generates multiple clusters, you cannot filter or mipmap the data because clustering indexes are not continuous.</span></span> <span data-ttu-id="ea527-120">Di seguito sono riportate alcune alternative per la gestione dei dati multicluster:</span><span class="sxs-lookup"><span data-stu-id="ea527-120">Here are some alternatives for handling multi-clustered data:</span></span>

-   <span data-ttu-id="ea527-121">Eseguire tutte le operazioni di filtro nel pixel shader.</span><span class="sxs-lookup"><span data-stu-id="ea527-121">Do all of the filtering yourself in the pixel shader.</span></span> <span data-ttu-id="ea527-122">Sfortunatamente, questa operazione è in genere poco pratica per motivi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ea527-122">Unfortunately, this is generally impractical for performance reasons.</span></span>
-   <span data-ttu-id="ea527-123">Se le trame sono trame con mapping non MIP a bassa risoluzione (ad esempio, mappe luminose), è più probabile che si calcoli semplicemente l'illuminazione direttamente nello spazio di trama, in cui non si verificherà alcun filtro e il rendering dell'oggetto con una trama ombreggiata.</span><span class="sxs-lookup"><span data-stu-id="ea527-123">If the textures are low resolution non mip-mapped textures (ie: light maps), it is most likely more efficient to just compute the lighting directly in texture space - where no filtering will occur, and render the object with a shaded texture.</span></span> <span data-ttu-id="ea527-124">Si tratta essenzialmente di una mappa chiara dinamica che viene creata interamente nella GPU.</span><span class="sxs-lookup"><span data-stu-id="ea527-124">This is essentially a dynamic light map that is created entirely on the GPU.</span></span>
-   <span data-ttu-id="ea527-125">Se viene usato un Atlante di trama (vedere [uso di UVAtlas (Direct3D 9)](using-uvatlas.md)), è possibile raggruppare manualmente la scena perché tutti i vettori di trasferimento in un componente connesso nello spazio di trama si trovino nello stesso cluster.</span><span class="sxs-lookup"><span data-stu-id="ea527-125">If a texture atlas is used (see [Using UVAtlas (Direct3D 9)](using-uvatlas.md)), you could manually cluster the scene by having all transfer vectors in a connected component in texture space be in the same cluster.</span></span> <span data-ttu-id="ea527-126">In questo modo è possibile filtrare la trama perché tutti i Texel a cui si accede si trovino nello stesso cluster per costruzione.</span><span class="sxs-lookup"><span data-stu-id="ea527-126">This way you can filter the texture because all texels accessed would be in the same cluster by construction.</span></span> <span data-ttu-id="ea527-127">L'ID cluster per una determinata faccia può essere propagato dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="ea527-127">The cluster ID for a given face could be propagated from the vertex shader.</span></span>

<span data-ttu-id="ea527-128">I pixel shader hanno un numero molto inferiore di registri costanti che non possono essere indicizzati, pertanto il pixel shader è leggermente diverso da quello del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="ea527-128">Pixel shaders have much fewer constant registers that cannot be indexed, so the pixel shader is somewhat different than the vertex shader.</span></span> <span data-ttu-id="ea527-129">L'archiviazione dei singoli cluster funziona in una trama dinamica a bassa risoluzione e l'uso di caricamenti di trama costituisce il modo più efficiente per eseguire il rendering quando si usano più cluster.</span><span class="sxs-lookup"><span data-stu-id="ea527-129">Storing the per-cluster work in a low resolution dynamic texture and using texture loads would be the most efficient way to render when using multiple clusters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea527-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea527-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea527-131">Trasferimento Radiance pre-calcolato</span><span class="sxs-lookup"><span data-stu-id="ea527-131">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> <dt>

<span data-ttu-id="ea527-132">[Esempio di demo PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="ea527-132">[PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span></span>
</dt> <dt>

<span data-ttu-id="ea527-133">[Simulatore PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="ea527-133">[PRT Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 




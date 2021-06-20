---
description: Informazioni sul supporto delle trame in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Supporto delle trame in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404604"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="b8d95-105">Supporto delle trame in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b8d95-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="b8d95-106">D3DX è una libreria di utilità che fornisce servizi helper.</span><span class="sxs-lookup"><span data-stu-id="b8d95-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="b8d95-107">Si tratta di un livello sopra il componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b8d95-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="b8d95-108">Trame</span><span class="sxs-lookup"><span data-stu-id="b8d95-108">Textures</span></span>

<span data-ttu-id="b8d95-109">Negli argomenti seguenti sono supportate molte trame diverse.</span><span class="sxs-lookup"><span data-stu-id="b8d95-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="b8d95-110">Supporto standard per le trame mipmapped.</span><span class="sxs-lookup"><span data-stu-id="b8d95-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="b8d95-111">Vedere [Generazione automatica di mipmap (Direct3D 9).](automatic-generation-of-mipmaps.md)</span><span class="sxs-lookup"><span data-stu-id="b8d95-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="b8d95-112">Supporto delle mappe cubi.</span><span class="sxs-lookup"><span data-stu-id="b8d95-112">Cube map support.</span></span> <span data-ttu-id="b8d95-113">Vedere [Cubic Environment Mapping (Direct3D 9) ( Mapping dell'ambiente cubico - Direct3D 9).](cubic-environment-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="b8d95-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="b8d95-114">Supporto della trama del volume.</span><span class="sxs-lookup"><span data-stu-id="b8d95-114">Volume texture support.</span></span> <span data-ttu-id="b8d95-115">Vedere [Risorse trama del volume (Direct3D 9).](volume-texture-resources.md)</span><span class="sxs-lookup"><span data-stu-id="b8d95-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="b8d95-116">Supporto del mapping dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b8d95-116">Environment mapping support.</span></span> <span data-ttu-id="b8d95-117">Vedere [Environment Mapping (Direct3D 9) (Mapping dell'ambiente - Direct3D 9).](environment-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="b8d95-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="b8d95-118">Supporto del mapping di urti.</span><span class="sxs-lookup"><span data-stu-id="b8d95-118">Bump mapping support.</span></span> <span data-ttu-id="b8d95-119">Vedere [Bump Mapping (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="b8d95-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="b8d95-120">Conversione del colore della trama</span><span class="sxs-lookup"><span data-stu-id="b8d95-120">Texture Color Conversion</span></span>

<span data-ttu-id="b8d95-121">Quando si usa una delle funzioni D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, potrebbe essere necessario eseguire la conversione dei colori.</span><span class="sxs-lookup"><span data-stu-id="b8d95-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="b8d95-122">Ad esempio, una superficie potrebbe essere di tipo RGBA e l'altra potrebbe essere UVWQ.</span><span class="sxs-lookup"><span data-stu-id="b8d95-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="b8d95-123">Per i casi di formati diversi, la sequenza di conversione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b8d95-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="b8d95-124">Mapping di RGBA a UVWQ</span><span class="sxs-lookup"><span data-stu-id="b8d95-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="b8d95-125">R <-> U, il canale R viene mappato al canale U o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="b8d95-126">G <-> V, il canale G viene mappato al canale V o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="b8d95-127">B <-> W, il canale B viene mappato al canale W o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="b8d95-128">Un < di >, un canale viene mappato al canale Q o L (a seconda di quale è disponibile nel formato di destinazione) o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="b8d95-129">Mapping UV a RGBA</span><span class="sxs-lookup"><span data-stu-id="b8d95-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="b8d95-130">U <-> R, il canale U viene mappato al canale R o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="b8d95-131">V <-> G, il canale V viene mappato al canale G o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="b8d95-132">1 <-> B, 1 è mappato al canale B o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="b8d95-133">1 <-> A, 1 è mappato al canale A o viceversa.</span><span class="sxs-lookup"><span data-stu-id="b8d95-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="b8d95-134">Se non esiste un canale nell'origine, si presuppone che sia 1 (ad eccezione di A8, dove si presuppone che R,G,B sia 0).</span><span class="sxs-lookup"><span data-stu-id="b8d95-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="b8d95-135">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b8d95-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="b8d95-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8d95-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8d95-137">D3DX</span><span class="sxs-lookup"><span data-stu-id="b8d95-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 




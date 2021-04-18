---
description: D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Supporto della trama in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303672"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="5c283-104">Supporto della trama in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5c283-104">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="5c283-105">D3DX è una libreria di utilità che fornisce servizi di supporto.</span><span class="sxs-lookup"><span data-stu-id="5c283-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="5c283-106">Si tratta di un livello sopra il componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5c283-106">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="5c283-107">Trame</span><span class="sxs-lookup"><span data-stu-id="5c283-107">Textures</span></span>

<span data-ttu-id="5c283-108">Negli argomenti seguenti sono supportate molte trame diverse.</span><span class="sxs-lookup"><span data-stu-id="5c283-108">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="5c283-109">Supporto della trama mipmap standard.</span><span class="sxs-lookup"><span data-stu-id="5c283-109">Standard mipmapped texture support.</span></span> <span data-ttu-id="5c283-110">Vedere [generazione automatica di mipmap (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="5c283-110">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="5c283-111">Supporto della mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="5c283-111">Cube map support.</span></span> <span data-ttu-id="5c283-112">Vedere [mapping di ambienti cubici (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="5c283-112">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="5c283-113">Supporto della trama del volume.</span><span class="sxs-lookup"><span data-stu-id="5c283-113">Volume texture support.</span></span> <span data-ttu-id="5c283-114">Vedere [risorse di trama volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="5c283-114">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="5c283-115">Supporto del mapping dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="5c283-115">Environment mapping support.</span></span> <span data-ttu-id="5c283-116">Vedere [mapping dell'ambiente (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="5c283-116">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="5c283-117">Supporto del mapping di Bump.</span><span class="sxs-lookup"><span data-stu-id="5c283-117">Bump mapping support.</span></span> <span data-ttu-id="5c283-118">Vedere [bump mapping (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="5c283-118">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="5c283-119">Conversione colori trama</span><span class="sxs-lookup"><span data-stu-id="5c283-119">Texture Color Conversion</span></span>

<span data-ttu-id="5c283-120">Quando si usa una delle funzioni D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, potrebbe essere necessario eseguire la conversione dei colori.</span><span class="sxs-lookup"><span data-stu-id="5c283-120">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="5c283-121">Ad esempio, una superficie può essere di tipo RGBA e l'altra potrebbe essere UVWQ.</span><span class="sxs-lookup"><span data-stu-id="5c283-121">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="5c283-122">Per i casi di formati diversi, la sequenza di conversione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="5c283-122">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="5c283-123">Mapping di RGBA a UVWQ</span><span class="sxs-lookup"><span data-stu-id="5c283-123">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="5c283-124">R <-> U, il canale R è mappato al canale U o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-124">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="5c283-125">G <-> V, il canale G viene mappato al canale V o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-125">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="5c283-126">B <-> W, il canale B è mappato al canale W o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-126">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="5c283-127">Un <-> Q/L, viene eseguito il mapping di un canale al canale Q o L (a seconda di quale è disponibile nel formato di destinazione) o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-127">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="5c283-128">Mapping di UV a RGBA</span><span class="sxs-lookup"><span data-stu-id="5c283-128">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="5c283-129">U <-> R, U Channel è mappato al canale R o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-129">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="5c283-130">V <-> G, V Channel è mappato al canale G o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-130">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="5c283-131">1 <-> B, 1 viene mappato al canale B o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-131">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="5c283-132">1 <-> A, 1 viene mappato a un canale o viceversa.</span><span class="sxs-lookup"><span data-stu-id="5c283-132">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="5c283-133">Se un canale non esiste nell'origine, si presuppone che sia 1 (ad eccezione di A8, dove R, G, B si presuppone che sia 0).</span><span class="sxs-lookup"><span data-stu-id="5c283-133">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="5c283-134">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="5c283-134">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="5c283-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c283-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c283-136">D3DX</span><span class="sxs-lookup"><span data-stu-id="5c283-136">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 




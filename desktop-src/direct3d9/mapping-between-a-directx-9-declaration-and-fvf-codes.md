---
description: Questa tabella esegue il mapping dei membri di una dichiarazione D3DVERTEXELEMENT9 a un codice FVF.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124479"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="50474-103">Mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="50474-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="50474-104">Questa tabella esegue il mapping dei membri di una Dichiarazione [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a un codice FVF.</span><span class="sxs-lookup"><span data-stu-id="50474-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="50474-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="50474-105">Data type</span></span>             | <span data-ttu-id="50474-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="50474-106">Usage</span></span>                      | <span data-ttu-id="50474-107">Indice di utilizzo</span><span class="sxs-lookup"><span data-stu-id="50474-107">Usage index</span></span> | <span data-ttu-id="50474-108">FVF</span><span class="sxs-lookup"><span data-stu-id="50474-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="50474-109">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="50474-110">\_Posizione D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="50474-111">0</span><span class="sxs-lookup"><span data-stu-id="50474-111">0</span></span>           | <span data-ttu-id="50474-112">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="50474-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="50474-113">\_Float4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="50474-114">\_Posizione D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="50474-115">0</span><span class="sxs-lookup"><span data-stu-id="50474-115">0</span></span>           | <span data-ttu-id="50474-116">\_XYZRHW D3DFVF</span><span class="sxs-lookup"><span data-stu-id="50474-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="50474-117">D3DDECLTYPE \_ floatn</span><span class="sxs-lookup"><span data-stu-id="50474-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="50474-118">\_BLENDWEIGHT D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="50474-119">0</span><span class="sxs-lookup"><span data-stu-id="50474-119">0</span></span>           | <span data-ttu-id="50474-120">\_XYZBN D3DFVF</span><span class="sxs-lookup"><span data-stu-id="50474-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="50474-121">\_UBYTE4 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="50474-122">\_BLENDINDICES D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="50474-123">0</span><span class="sxs-lookup"><span data-stu-id="50474-123">0</span></span>           | <span data-ttu-id="50474-124">D3DFVF \_ XYZB (nWeights + 1)</span><span class="sxs-lookup"><span data-stu-id="50474-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="50474-125">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="50474-126">D3DDECLUSAGE \_ normale</span><span class="sxs-lookup"><span data-stu-id="50474-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="50474-127">0</span><span class="sxs-lookup"><span data-stu-id="50474-127">0</span></span>           | <span data-ttu-id="50474-128">D3DFVF \_ normale</span><span class="sxs-lookup"><span data-stu-id="50474-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="50474-129">\_FLOAT1 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="50474-130">\_PSIZE D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="50474-131">0</span><span class="sxs-lookup"><span data-stu-id="50474-131">0</span></span>           | <span data-ttu-id="50474-132">\_PSIZE D3DFVF</span><span class="sxs-lookup"><span data-stu-id="50474-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="50474-133">\_D3DCOLOR D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="50474-134">\_Colore D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="50474-135">0</span><span class="sxs-lookup"><span data-stu-id="50474-135">0</span></span>           | <span data-ttu-id="50474-136">D3DFVF \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="50474-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="50474-137">\_D3DCOLOR D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="50474-138">\_Colore D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="50474-139">1</span><span class="sxs-lookup"><span data-stu-id="50474-139">1</span></span>           | <span data-ttu-id="50474-140">D3DFVF \_ speculare</span><span class="sxs-lookup"><span data-stu-id="50474-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="50474-141">\_Float D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="50474-142">\_TEXCOORD D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="50474-143">n</span><span class="sxs-lookup"><span data-stu-id="50474-143">n</span></span>           | <span data-ttu-id="50474-144">D3DFVF \_ TEXCOORDSIZEm (n)</span><span class="sxs-lookup"><span data-stu-id="50474-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="50474-145">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="50474-146">\_Posizione D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="50474-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="50474-147">1</span><span class="sxs-lookup"><span data-stu-id="50474-147">1</span></span>           | <span data-ttu-id="50474-148">N/D</span><span class="sxs-lookup"><span data-stu-id="50474-148">N/A</span></span>                       |
| <span data-ttu-id="50474-149">\_FLOAT3 D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="50474-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="50474-150">D3DDECLUSAGE \_ normale</span><span class="sxs-lookup"><span data-stu-id="50474-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="50474-151">1</span><span class="sxs-lookup"><span data-stu-id="50474-151">1</span></span>           | <span data-ttu-id="50474-152">N/D</span><span class="sxs-lookup"><span data-stu-id="50474-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="50474-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50474-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50474-154">Dichiarazione vertici</span><span class="sxs-lookup"><span data-stu-id="50474-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




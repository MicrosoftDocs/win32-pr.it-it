---
title: DP3-PS
description: Calcola il prodotto del punto a tre componenti dei registri di origine. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981407"
---
# <a name="dp3---ps"></a><span data-ttu-id="a50ef-104">DP3-PS</span><span class="sxs-lookup"><span data-stu-id="a50ef-104">dp3 - ps</span></span>

<span data-ttu-id="a50ef-105">Calcola il prodotto del punto a tre componenti dei registri di origine.</span><span class="sxs-lookup"><span data-stu-id="a50ef-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a50ef-106">Syntax</span></span>



| <span data-ttu-id="a50ef-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a50ef-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a50ef-108">dove</span><span class="sxs-lookup"><span data-stu-id="a50ef-108">where</span></span>

-   <span data-ttu-id="a50ef-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a50ef-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a50ef-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="a50ef-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a50ef-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="a50ef-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a50ef-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a50ef-112">Remarks</span></span>



| <span data-ttu-id="a50ef-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a50ef-113">Pixel shader versions</span></span> | <span data-ttu-id="a50ef-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a50ef-114">1\_1</span></span> | <span data-ttu-id="a50ef-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="a50ef-115">1\_2</span></span> | <span data-ttu-id="a50ef-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a50ef-116">1\_3</span></span> | <span data-ttu-id="a50ef-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="a50ef-117">1\_4</span></span> | <span data-ttu-id="a50ef-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a50ef-118">2\_0</span></span> | <span data-ttu-id="a50ef-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a50ef-119">2\_x</span></span> | <span data-ttu-id="a50ef-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a50ef-120">2\_sw</span></span> | <span data-ttu-id="a50ef-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a50ef-121">3\_0</span></span> | <span data-ttu-id="a50ef-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a50ef-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a50ef-123">dp3</span><span class="sxs-lookup"><span data-stu-id="a50ef-123">dp3</span></span>                   | <span data-ttu-id="a50ef-124">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-124">x</span></span>    | <span data-ttu-id="a50ef-125">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-125">x</span></span>    | <span data-ttu-id="a50ef-126">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-126">x</span></span>    | <span data-ttu-id="a50ef-127">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-127">x</span></span>    | <span data-ttu-id="a50ef-128">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-128">x</span></span>    | <span data-ttu-id="a50ef-129">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-129">x</span></span>    | <span data-ttu-id="a50ef-130">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-130">x</span></span>     | <span data-ttu-id="a50ef-131">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-131">x</span></span>    | <span data-ttu-id="a50ef-132">x</span><span class="sxs-lookup"><span data-stu-id="a50ef-132">x</span></span>     |



 

<span data-ttu-id="a50ef-133">Il frammento di codice seguente mostra le operazioni eseguite:</span><span class="sxs-lookup"><span data-stu-id="a50ef-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="a50ef-134">Questa istruzione viene eseguita nella pipeline vettoriale, scrivendo sempre nei canali dei colori.</span><span class="sxs-lookup"><span data-stu-id="a50ef-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="a50ef-135">Per la versione 1 \_ 4, questa istruzione usa ancora la pipeline vettoriale ma può scrivere su qualsiasi canale.</span><span class="sxs-lookup"><span data-stu-id="a50ef-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="a50ef-136">Un'istruzione con una maschera di scrittura di destinazione Register. RGB (. xyz) può essere co-emessa con DP3, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a50ef-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="a50ef-137">L'istruzione DP3 può essere modificata tramite il modificatore dell'argomento di input del [Registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) applicato ai relativi argomenti di input se non sono già stati espansi nell'intervallo dinamico con segno.</span><span class="sxs-lookup"><span data-stu-id="a50ef-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="a50ef-138">Per uno shader di illuminazione, il modificatore dell'istruzione di saturazione ( \_ Sat) viene spesso usato per bloccare i valori negativi a nero, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="a50ef-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="a50ef-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a50ef-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a50ef-140">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a50ef-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





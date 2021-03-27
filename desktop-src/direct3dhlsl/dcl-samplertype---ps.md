---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Dichiarare un campionatore pixel shader.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046121"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="23cac-103">DCL \_ samplerType (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="23cac-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="23cac-104">Dichiarare un campionatore pixel shader.</span><span class="sxs-lookup"><span data-stu-id="23cac-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="23cac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23cac-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="23cac-106">samplerType di DCL \_\#</span><span class="sxs-lookup"><span data-stu-id="23cac-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="23cac-107">dove:</span><span class="sxs-lookup"><span data-stu-id="23cac-107">where:</span></span>

-   <span data-ttu-id="23cac-108">\_samplerType definisce il tipo di dati del campionatore.</span><span class="sxs-lookup"><span data-stu-id="23cac-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="23cac-109">Determina il numero di coordinate necessarie per ogni coordinata di trama durante il campionamento.</span><span class="sxs-lookup"><span data-stu-id="23cac-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="23cac-110">Sono definite le dimensioni delle coordinate di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="23cac-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="23cac-111">\_2D</span><span class="sxs-lookup"><span data-stu-id="23cac-111">\_2d</span></span>
    -   <span data-ttu-id="23cac-112">\_cubo</span><span class="sxs-lookup"><span data-stu-id="23cac-112">\_cube</span></span>
    -   <span data-ttu-id="23cac-113">\_volume</span><span class="sxs-lookup"><span data-stu-id="23cac-113">\_volume</span></span>
-   <span data-ttu-id="23cac-114">s \# identifica un campionatore dove s è un'abbreviazione del campionatore e \# è il numero di campionatore.</span><span class="sxs-lookup"><span data-stu-id="23cac-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="23cac-115">I sampler sono pseudo-registri perché non è possibile leggerli o scriverli direttamente.</span><span class="sxs-lookup"><span data-stu-id="23cac-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="23cac-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="23cac-116">Remarks</span></span>



| <span data-ttu-id="23cac-117">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="23cac-117">Pixel shader versions</span></span> | <span data-ttu-id="23cac-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="23cac-118">1\_1</span></span> | <span data-ttu-id="23cac-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="23cac-119">1\_2</span></span> | <span data-ttu-id="23cac-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="23cac-120">1\_3</span></span> | <span data-ttu-id="23cac-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="23cac-121">1\_4</span></span> | <span data-ttu-id="23cac-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="23cac-122">2\_0</span></span> | <span data-ttu-id="23cac-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="23cac-123">2\_x</span></span> | <span data-ttu-id="23cac-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="23cac-124">2\_sw</span></span> | <span data-ttu-id="23cac-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="23cac-125">3\_0</span></span> | <span data-ttu-id="23cac-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="23cac-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="23cac-127">\_samplerType DCL</span><span class="sxs-lookup"><span data-stu-id="23cac-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="23cac-128">x</span><span class="sxs-lookup"><span data-stu-id="23cac-128">x</span></span>    | <span data-ttu-id="23cac-129">x</span><span class="sxs-lookup"><span data-stu-id="23cac-129">x</span></span>    | <span data-ttu-id="23cac-130">x</span><span class="sxs-lookup"><span data-stu-id="23cac-130">x</span></span>     | <span data-ttu-id="23cac-131">x</span><span class="sxs-lookup"><span data-stu-id="23cac-131">x</span></span>    | <span data-ttu-id="23cac-132">x</span><span class="sxs-lookup"><span data-stu-id="23cac-132">x</span></span>     |



 

<span data-ttu-id="23cac-133">Tutte le \_ istruzioni samplerType di DCL devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="23cac-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="23cac-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="23cac-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="23cac-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23cac-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23cac-136">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="23cac-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: dcl_samplerType (sm2, sm3 - ps asm)
description: Dichiarare un pixel shader di esempio.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129668"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="e196c-103">dcl \_ samplerType (sm2, sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="e196c-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="e196c-104">Dichiarare un pixel shader di esempio.</span><span class="sxs-lookup"><span data-stu-id="e196c-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="e196c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e196c-105">Syntax</span></span>

<span data-ttu-id="e196c-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="e196c-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="e196c-107">dove:</span><span class="sxs-lookup"><span data-stu-id="e196c-107">where:</span></span>

-   <span data-ttu-id="e196c-108">\_samplerType definisce il tipo di dati sampler.</span><span class="sxs-lookup"><span data-stu-id="e196c-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="e196c-109">Questo determina il numero di coordinate richieste da ogni coordinata di trama durante il campionamento.</span><span class="sxs-lookup"><span data-stu-id="e196c-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="e196c-110">Vengono definite le dimensioni delle coordinate di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="e196c-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="e196c-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="e196c-111">\_2d</span></span>
    -   <span data-ttu-id="e196c-112">\_Cubo</span><span class="sxs-lookup"><span data-stu-id="e196c-112">\_cube</span></span>
    -   <span data-ttu-id="e196c-113">\_Volume</span><span class="sxs-lookup"><span data-stu-id="e196c-113">\_volume</span></span>
-   <span data-ttu-id="e196c-114">s \# identifica un campionatore dove s è un'abbreviazione del campionatore e \# è il numero del campionatore.</span><span class="sxs-lookup"><span data-stu-id="e196c-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="e196c-115">I campionatori sono pseudoregistri perché non è possibile leggerli o scrivervi direttamente.</span><span class="sxs-lookup"><span data-stu-id="e196c-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="e196c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e196c-116">Remarks</span></span>



| <span data-ttu-id="e196c-117">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e196c-117">Pixel shader versions</span></span> | <span data-ttu-id="e196c-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="e196c-118">1\_1</span></span> | <span data-ttu-id="e196c-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="e196c-119">1\_2</span></span> | <span data-ttu-id="e196c-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e196c-120">1\_3</span></span> | <span data-ttu-id="e196c-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="e196c-121">1\_4</span></span> | <span data-ttu-id="e196c-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e196c-122">2\_0</span></span> | <span data-ttu-id="e196c-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e196c-123">2\_x</span></span> | <span data-ttu-id="e196c-124">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e196c-124">2\_sw</span></span> | <span data-ttu-id="e196c-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e196c-125">3\_0</span></span> | <span data-ttu-id="e196c-126">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e196c-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e196c-127">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="e196c-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="e196c-128">x</span><span class="sxs-lookup"><span data-stu-id="e196c-128">x</span></span>    | <span data-ttu-id="e196c-129">x</span><span class="sxs-lookup"><span data-stu-id="e196c-129">x</span></span>    | <span data-ttu-id="e196c-130">x</span><span class="sxs-lookup"><span data-stu-id="e196c-130">x</span></span>     | <span data-ttu-id="e196c-131">x</span><span class="sxs-lookup"><span data-stu-id="e196c-131">x</span></span>    | <span data-ttu-id="e196c-132">x</span><span class="sxs-lookup"><span data-stu-id="e196c-132">x</span></span>     |



 

<span data-ttu-id="e196c-133">Tutte le istruzioni dcl \_ samplerType devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e196c-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="e196c-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="e196c-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="e196c-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e196c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e196c-136">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="e196c-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





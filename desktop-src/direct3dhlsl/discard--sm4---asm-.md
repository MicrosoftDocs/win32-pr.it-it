---
title: Ignora (SM4-ASM)
description: Contrassegnare in modo condizionale i risultati del pixel shader da scartare al raggiungimento della fine del programma.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956069"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="85ef1-103">Ignora (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="85ef1-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="85ef1-104">Contrassegnare in modo condizionale i risultati del pixel shader da scartare al raggiungimento della fine del programma.</span><span class="sxs-lookup"><span data-stu-id="85ef1-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="85ef1-105">Ignora { \_ z </span><span class="sxs-lookup"><span data-stu-id="85ef1-105">discard{\_z</span></span>\|<span data-ttu-id="85ef1-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="85ef1-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="85ef1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="85ef1-107">Item</span></span>                                                            | <span data-ttu-id="85ef1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85ef1-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ef1-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="85ef1-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="85ef1-110">\[nel \] valore che determina se annullare il pixel corrente in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="85ef1-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="85ef1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="85ef1-111">Remarks</span></span>

<span data-ttu-id="85ef1-112">Questa istruzione contrassegna il pixel corrente come terminato, continuando l'esecuzione, in modo che altri pixel in esecuzione in parallelo possano ottenere i derivati, se necessario.</span><span class="sxs-lookup"><span data-stu-id="85ef1-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="85ef1-113">Anche se l'esecuzione continua, tutte le scritture di output di pixel shader prima o dopo l'istruzione di **eliminazione** vengono scartate.</span><span class="sxs-lookup"><span data-stu-id="85ef1-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="85ef1-114">Per **scarto \_ z**, se tutti i bit in *src0. Select \_ Component* sono pari a zero, il pixel viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="85ef1-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="85ef1-115">Per **scarto \_ NZ**, se i bit nel *\_ componente src0. Select* sono diversi da zero, il pixel viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="85ef1-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="85ef1-116">Inoltre, l'istruzione di **eliminazione** può essere presente all'interno di qualsiasi costrutto di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="85ef1-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="85ef1-117">È possibile che in uno shader siano presenti più istruzioni di **eliminazione** e, in caso di esecuzione, il pixel viene terminato.</span><span class="sxs-lookup"><span data-stu-id="85ef1-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="85ef1-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="85ef1-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="85ef1-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="85ef1-119">Vertex Shader</span></span> | <span data-ttu-id="85ef1-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="85ef1-120">Geometry Shader</span></span> | <span data-ttu-id="85ef1-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="85ef1-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="85ef1-122">x</span><span class="sxs-lookup"><span data-stu-id="85ef1-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="85ef1-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="85ef1-123">Minimum Shader Model</span></span>

<span data-ttu-id="85ef1-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="85ef1-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="85ef1-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="85ef1-125">Shader Model</span></span>                                              | <span data-ttu-id="85ef1-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="85ef1-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="85ef1-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="85ef1-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="85ef1-128">sì</span><span class="sxs-lookup"><span data-stu-id="85ef1-128">yes</span></span>       |
| [<span data-ttu-id="85ef1-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="85ef1-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="85ef1-130">sì</span><span class="sxs-lookup"><span data-stu-id="85ef1-130">yes</span></span>       |
| [<span data-ttu-id="85ef1-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="85ef1-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="85ef1-132">sì</span><span class="sxs-lookup"><span data-stu-id="85ef1-132">yes</span></span>       |
| [<span data-ttu-id="85ef1-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85ef1-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="85ef1-134">no</span><span class="sxs-lookup"><span data-stu-id="85ef1-134">no</span></span>        |
| [<span data-ttu-id="85ef1-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85ef1-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="85ef1-136">no</span><span class="sxs-lookup"><span data-stu-id="85ef1-136">no</span></span>        |
| [<span data-ttu-id="85ef1-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85ef1-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="85ef1-138">no</span><span class="sxs-lookup"><span data-stu-id="85ef1-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="85ef1-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85ef1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85ef1-140">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85ef1-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






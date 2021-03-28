---
title: Label (SM4-ASM)
description: Indica l'inizio di una subroutine.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719417"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="531c7-103">Label (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="531c7-103">label (sm4 - asm)</span></span>

<span data-ttu-id="531c7-104">Indica l'inizio di una subroutine.</span><span class="sxs-lookup"><span data-stu-id="531c7-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="531c7-105">etichetta l\#</span><span class="sxs-lookup"><span data-stu-id="531c7-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="531c7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="531c7-106">Item</span></span>                                                       | <span data-ttu-id="531c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="531c7-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="531c7-108"><span id="l_"></span><span id="L_"></span>*l\#*</span><span class="sxs-lookup"><span data-stu-id="531c7-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="531c7-109">\[nel \] numero di etichetta.</span><span class="sxs-lookup"><span data-stu-id="531c7-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="531c7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="531c7-110">Remarks</span></span>

<span data-ttu-id="531c7-111">Un' **etichetta** può essere visualizzata solo immediatamente dopo un'istruzione [**ret**](ret--sm4---asm-.md) che non è annidata in alcuna istruzione di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="531c7-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="531c7-112">Il codice prima della prima **etichetta** in un programma è il programma principale.</span><span class="sxs-lookup"><span data-stu-id="531c7-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="531c7-113">Tutte le subroutine vengono visualizzate alla fine del programma, indicate dalle istruzioni **Label** .</span><span class="sxs-lookup"><span data-stu-id="531c7-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="531c7-114">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="531c7-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="531c7-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="531c7-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="531c7-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="531c7-116">Vertex Shader</span></span> | <span data-ttu-id="531c7-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="531c7-117">Geometry Shader</span></span> | <span data-ttu-id="531c7-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="531c7-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="531c7-119">x</span><span class="sxs-lookup"><span data-stu-id="531c7-119">x</span></span>             | <span data-ttu-id="531c7-120">x</span><span class="sxs-lookup"><span data-stu-id="531c7-120">x</span></span>               | <span data-ttu-id="531c7-121">x</span><span class="sxs-lookup"><span data-stu-id="531c7-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="531c7-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="531c7-122">Minimum Shader Model</span></span>

<span data-ttu-id="531c7-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="531c7-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="531c7-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="531c7-124">Shader Model</span></span>                                              | <span data-ttu-id="531c7-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="531c7-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="531c7-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="531c7-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="531c7-127">sì</span><span class="sxs-lookup"><span data-stu-id="531c7-127">yes</span></span>       |
| [<span data-ttu-id="531c7-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="531c7-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="531c7-129">sì</span><span class="sxs-lookup"><span data-stu-id="531c7-129">yes</span></span>       |
| [<span data-ttu-id="531c7-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="531c7-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="531c7-131">sì</span><span class="sxs-lookup"><span data-stu-id="531c7-131">yes</span></span>       |
| [<span data-ttu-id="531c7-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="531c7-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="531c7-133">no</span><span class="sxs-lookup"><span data-stu-id="531c7-133">no</span></span>        |
| [<span data-ttu-id="531c7-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="531c7-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="531c7-135">no</span><span class="sxs-lookup"><span data-stu-id="531c7-135">no</span></span>        |
| [<span data-ttu-id="531c7-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="531c7-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="531c7-137">no</span><span class="sxs-lookup"><span data-stu-id="531c7-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="531c7-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="531c7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531c7-139">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="531c7-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






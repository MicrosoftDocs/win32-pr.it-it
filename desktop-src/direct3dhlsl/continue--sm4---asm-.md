---
title: continua (SM4-ASM)
description: Continua l'esecuzione all'inizio del ciclo corrente.
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993064"
---
# <a name="continue-sm4---asm"></a><span data-ttu-id="4bdcf-103">continua (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4bdcf-103">continue (sm4 - asm)</span></span>

<span data-ttu-id="4bdcf-104">Continua l'esecuzione all'inizio del ciclo corrente.</span><span class="sxs-lookup"><span data-stu-id="4bdcf-104">Continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="4bdcf-105">continue</span><span class="sxs-lookup"><span data-stu-id="4bdcf-105">continue</span></span> |
|----------|



 

## <a name="remarks"></a><span data-ttu-id="4bdcf-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bdcf-106">Remarks</span></span>

<span data-ttu-id="4bdcf-107">**continue** può essere utilizzato solo all'interno di un [ciclo](loop--sm4---asm-.md) o di [EndLoop](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="4bdcf-107">**continue** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="4bdcf-108">Nell'esempio seguente viene illustrato come utilizzare l'istruzione **continue** .</span><span class="sxs-lookup"><span data-stu-id="4bdcf-108">The following example shows how to use the **continue** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



<span data-ttu-id="4bdcf-109">Il formato del token contiene l'offset dell'istruzione del ciclo corrispondente nello shader come praticità.</span><span class="sxs-lookup"><span data-stu-id="4bdcf-109">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="4bdcf-110">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4bdcf-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4bdcf-111">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="4bdcf-111">Vertex Shader</span></span> | <span data-ttu-id="4bdcf-112">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="4bdcf-112">Geometry Shader</span></span> | <span data-ttu-id="4bdcf-113">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="4bdcf-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4bdcf-114">x</span><span class="sxs-lookup"><span data-stu-id="4bdcf-114">x</span></span>             | <span data-ttu-id="4bdcf-115">x</span><span class="sxs-lookup"><span data-stu-id="4bdcf-115">x</span></span>               | <span data-ttu-id="4bdcf-116">x</span><span class="sxs-lookup"><span data-stu-id="4bdcf-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4bdcf-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4bdcf-117">Minimum Shader Model</span></span>

<span data-ttu-id="4bdcf-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4bdcf-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4bdcf-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4bdcf-119">Shader Model</span></span>                                              | <span data-ttu-id="4bdcf-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="4bdcf-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4bdcf-121">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4bdcf-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4bdcf-122">sì</span><span class="sxs-lookup"><span data-stu-id="4bdcf-122">yes</span></span>       |
| [<span data-ttu-id="4bdcf-123">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="4bdcf-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4bdcf-124">sì</span><span class="sxs-lookup"><span data-stu-id="4bdcf-124">yes</span></span>       |
| [<span data-ttu-id="4bdcf-125">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="4bdcf-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4bdcf-126">sì</span><span class="sxs-lookup"><span data-stu-id="4bdcf-126">yes</span></span>       |
| [<span data-ttu-id="4bdcf-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bdcf-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4bdcf-128">no</span><span class="sxs-lookup"><span data-stu-id="4bdcf-128">no</span></span>        |
| [<span data-ttu-id="4bdcf-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bdcf-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4bdcf-130">no</span><span class="sxs-lookup"><span data-stu-id="4bdcf-130">no</span></span>        |
| [<span data-ttu-id="4bdcf-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bdcf-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4bdcf-132">no</span><span class="sxs-lookup"><span data-stu-id="4bdcf-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4bdcf-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bdcf-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bdcf-134">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bdcf-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





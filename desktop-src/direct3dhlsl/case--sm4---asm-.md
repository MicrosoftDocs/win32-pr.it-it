---
title: caso (SM4-ASM)
description: Etichetta in un'istruzione switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976370"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="3a833-103">caso (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3a833-103">case (sm4 - asm)</span></span>

<span data-ttu-id="3a833-104">Etichetta in un'istruzione switch.</span><span class="sxs-lookup"><span data-stu-id="3a833-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="3a833-105">Case \[ 32-bit immediate\]</span><span class="sxs-lookup"><span data-stu-id="3a833-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="3a833-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a833-106">Remarks</span></span>

<span data-ttu-id="3a833-107">Poiché il passaggio attraverso i **case** è valido solo se non viene aggiunto codice, più **case** (incluso il [valore predefinito](default--sm4---asm-.md)) possono condividere lo stesso blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="3a833-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="3a833-108">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a833-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a833-109">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="3a833-109">Vertex Shader</span></span> | <span data-ttu-id="3a833-110">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="3a833-110">Geometry Shader</span></span> | <span data-ttu-id="3a833-111">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="3a833-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3a833-112">x</span><span class="sxs-lookup"><span data-stu-id="3a833-112">x</span></span>             | <span data-ttu-id="3a833-113">x</span><span class="sxs-lookup"><span data-stu-id="3a833-113">x</span></span>               | <span data-ttu-id="3a833-114">x</span><span class="sxs-lookup"><span data-stu-id="3a833-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a833-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3a833-115">Minimum Shader Model</span></span>

<span data-ttu-id="3a833-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a833-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a833-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3a833-117">Shader Model</span></span>                                              | <span data-ttu-id="3a833-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="3a833-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a833-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3a833-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a833-120">sì</span><span class="sxs-lookup"><span data-stu-id="3a833-120">yes</span></span>       |
| [<span data-ttu-id="3a833-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3a833-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a833-122">sì</span><span class="sxs-lookup"><span data-stu-id="3a833-122">yes</span></span>       |
| [<span data-ttu-id="3a833-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3a833-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a833-124">sì</span><span class="sxs-lookup"><span data-stu-id="3a833-124">yes</span></span>       |
| [<span data-ttu-id="3a833-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a833-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a833-126">no</span><span class="sxs-lookup"><span data-stu-id="3a833-126">no</span></span>        |
| [<span data-ttu-id="3a833-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a833-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a833-128">no</span><span class="sxs-lookup"><span data-stu-id="3a833-128">no</span></span>        |
| [<span data-ttu-id="3a833-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a833-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a833-130">no</span><span class="sxs-lookup"><span data-stu-id="3a833-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a833-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a833-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a833-132">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a833-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





---
title: impostazione predefinita (SM4-ASM)
description: Etichetta facoltativa in un'istruzione switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976338"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="fae9e-103">impostazione predefinita (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fae9e-103">default (sm4 - asm)</span></span>

<span data-ttu-id="fae9e-104">Etichetta facoltativa in un'istruzione [Switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="fae9e-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="fae9e-105">default</span><span class="sxs-lookup"><span data-stu-id="fae9e-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="fae9e-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="fae9e-106">Remarks</span></span>

<span data-ttu-id="fae9e-107">Questa istruzione funziona esattamente come l' **impostazione predefinita** in C. il passaggio a è valido solo se non è stato aggiunto codice, quindi più case (incluso il **valore predefinito**) possono condividere lo stesso blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="fae9e-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="fae9e-108">In un costrutto **Switch** è consentita una sola istruzione **default** .</span><span class="sxs-lookup"><span data-stu-id="fae9e-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="fae9e-109">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fae9e-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fae9e-110">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="fae9e-110">Vertex Shader</span></span> | <span data-ttu-id="fae9e-111">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="fae9e-111">Geometry Shader</span></span> | <span data-ttu-id="fae9e-112">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="fae9e-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fae9e-113">x</span><span class="sxs-lookup"><span data-stu-id="fae9e-113">x</span></span>             | <span data-ttu-id="fae9e-114">x</span><span class="sxs-lookup"><span data-stu-id="fae9e-114">x</span></span>               | <span data-ttu-id="fae9e-115">x</span><span class="sxs-lookup"><span data-stu-id="fae9e-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fae9e-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="fae9e-116">Minimum Shader Model</span></span>

<span data-ttu-id="fae9e-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="fae9e-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fae9e-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="fae9e-118">Shader Model</span></span>                                              | <span data-ttu-id="fae9e-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="fae9e-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fae9e-120">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fae9e-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fae9e-121">sì</span><span class="sxs-lookup"><span data-stu-id="fae9e-121">yes</span></span>       |
| [<span data-ttu-id="fae9e-122">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="fae9e-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fae9e-123">sì</span><span class="sxs-lookup"><span data-stu-id="fae9e-123">yes</span></span>       |
| [<span data-ttu-id="fae9e-124">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="fae9e-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fae9e-125">sì</span><span class="sxs-lookup"><span data-stu-id="fae9e-125">yes</span></span>       |
| [<span data-ttu-id="fae9e-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fae9e-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fae9e-127">no</span><span class="sxs-lookup"><span data-stu-id="fae9e-127">no</span></span>        |
| [<span data-ttu-id="fae9e-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fae9e-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fae9e-129">no</span><span class="sxs-lookup"><span data-stu-id="fae9e-129">no</span></span>        |
| [<span data-ttu-id="fae9e-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fae9e-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fae9e-131">no</span><span class="sxs-lookup"><span data-stu-id="fae9e-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fae9e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fae9e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fae9e-133">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fae9e-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





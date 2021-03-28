---
title: Negate
description: Capovolge il segno del valore di un operando di origine utilizzato in un'operazione aritmetica.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046072"
---
# <a name="negate"></a><span data-ttu-id="7ed19-103">Negate</span><span class="sxs-lookup"><span data-stu-id="7ed19-103">Negate</span></span>

<span data-ttu-id="7ed19-104">Capovolge il segno del valore di un operando di origine utilizzato in un'operazione aritmetica.</span><span class="sxs-lookup"><span data-stu-id="7ed19-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="7ed19-105">Per le istruzioni e i punti a virgola mobile a precisione singola e doppia, il modificatore negazioni capovolge il segno dei numeri nell'operando di origine, inclusi i valori INF.</span><span class="sxs-lookup"><span data-stu-id="7ed19-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="7ed19-106">L'applicazione di **negazione** in NaN conserva Nan, anche se il particolare modello di bit Nan che risulta non è definito.</span><span class="sxs-lookup"><span data-stu-id="7ed19-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="7ed19-107">Per le istruzioni Integer, il modificatore **negazioni** accetta il complemento 2 del numero o dei numeri nell'operando di origine.</span><span class="sxs-lookup"><span data-stu-id="7ed19-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="7ed19-108">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7ed19-108">Minimum Shader Model</span></span>

<span data-ttu-id="7ed19-109">Questo modificatore è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ed19-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="7ed19-110">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7ed19-110">Shader Model</span></span>                                              | <span data-ttu-id="7ed19-111">Supportato</span><span class="sxs-lookup"><span data-stu-id="7ed19-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7ed19-112">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7ed19-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7ed19-113">sì</span><span class="sxs-lookup"><span data-stu-id="7ed19-113">yes</span></span>       |
| [<span data-ttu-id="7ed19-114">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="7ed19-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7ed19-115">sì</span><span class="sxs-lookup"><span data-stu-id="7ed19-115">yes</span></span>       |
| [<span data-ttu-id="7ed19-116">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7ed19-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7ed19-117">sì</span><span class="sxs-lookup"><span data-stu-id="7ed19-117">yes</span></span>       |
| [<span data-ttu-id="7ed19-118">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ed19-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7ed19-119">no</span><span class="sxs-lookup"><span data-stu-id="7ed19-119">no</span></span>        |
| [<span data-ttu-id="7ed19-120">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ed19-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7ed19-121">no</span><span class="sxs-lookup"><span data-stu-id="7ed19-121">no</span></span>        |
| [<span data-ttu-id="7ed19-122">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ed19-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7ed19-123">no</span><span class="sxs-lookup"><span data-stu-id="7ed19-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7ed19-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ed19-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed19-125">Modificatori di istruzione</span><span class="sxs-lookup"><span data-stu-id="7ed19-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 





---
title: Valore assoluto
description: Assumere il valore assoluto di un operando di origine utilizzato in un'operazione aritmetica.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335615"
---
# <a name="absolute-value"></a><span data-ttu-id="59153-103">Valore assoluto</span><span class="sxs-lookup"><span data-stu-id="59153-103">Absolute Value</span></span>

<span data-ttu-id="59153-104">Assumere il valore assoluto di un operando di origine utilizzato in un'operazione aritmetica.</span><span class="sxs-lookup"><span data-stu-id="59153-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="59153-105">\_ABS</span><span class="sxs-lookup"><span data-stu-id="59153-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="59153-106">Questo modificatore viene utilizzato per solo istruzioni e virgola mobile a precisione singola e doppia.</span><span class="sxs-lookup"><span data-stu-id="59153-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="59153-107">Il modificatore **\_ ABS** forza il segno dei numeri sull'operando di origine positivo, inclusi i valori inf.</span><span class="sxs-lookup"><span data-stu-id="59153-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="59153-108">L'applicazione di **\_ ABS** su Nan conserva Nan, anche se il particolare modello di bit Nan che risulta non è definito.</span><span class="sxs-lookup"><span data-stu-id="59153-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="59153-109">Quando \_ ABS viene combinato con il modificatore [negazioni](negate.md) , la combinazione forza il segno a essere negativo, come se il modificatore **\_ ABS** venisse applicato per primo, quindi la **negazione**.</span><span class="sxs-lookup"><span data-stu-id="59153-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="59153-110">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="59153-110">Minimum Shader Model</span></span>

<span data-ttu-id="59153-111">Questo modificatore è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="59153-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="59153-112">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="59153-112">Shader Model</span></span>                                              | <span data-ttu-id="59153-113">Supportato</span><span class="sxs-lookup"><span data-stu-id="59153-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="59153-114">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="59153-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="59153-115">sì</span><span class="sxs-lookup"><span data-stu-id="59153-115">yes</span></span>       |
| [<span data-ttu-id="59153-116">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="59153-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="59153-117">sì</span><span class="sxs-lookup"><span data-stu-id="59153-117">yes</span></span>       |
| [<span data-ttu-id="59153-118">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="59153-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="59153-119">sì</span><span class="sxs-lookup"><span data-stu-id="59153-119">yes</span></span>       |
| [<span data-ttu-id="59153-120">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="59153-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="59153-121">no</span><span class="sxs-lookup"><span data-stu-id="59153-121">no</span></span>        |
| [<span data-ttu-id="59153-122">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="59153-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="59153-123">no</span><span class="sxs-lookup"><span data-stu-id="59153-123">no</span></span>        |
| [<span data-ttu-id="59153-124">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="59153-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="59153-125">no</span><span class="sxs-lookup"><span data-stu-id="59153-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="59153-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59153-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59153-127">Modificatori di istruzione</span><span class="sxs-lookup"><span data-stu-id="59153-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 





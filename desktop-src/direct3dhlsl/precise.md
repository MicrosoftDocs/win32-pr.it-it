---
title: Preciso
description: Disabilitazione per istruzione del refactoring aritmetico.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516477"
---
# <a name="precise"></a><span data-ttu-id="f67b8-103">Preciso</span><span class="sxs-lookup"><span data-stu-id="f67b8-103">Precise</span></span>

<span data-ttu-id="f67b8-104">Disabilitazione per istruzione del refactoring aritmetico.</span><span class="sxs-lookup"><span data-stu-id="f67b8-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="f67b8-105">preciso (maschera componenti)</span><span class="sxs-lookup"><span data-stu-id="f67b8-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="f67b8-106">Questo modificatore richiede il flag di shader globale "refactoring \_ allowed".</span><span class="sxs-lookup"><span data-stu-id="f67b8-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="f67b8-107">Quando è presente il refactoring \_ consentito, i risultati dei singoli componenti delle singole istruzioni possono essere costretti a rimanere precisi o non sottoposti a refactoring dai compilatori o dai driver.</span><span class="sxs-lookup"><span data-stu-id="f67b8-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="f67b8-108">Se i componenti di un'istruzione [**MAD**](mad--sm4---asm-.md) sono contrassegnati come **precisi**, l'hardware deve eseguire un'istruzione **MAD** o l'equivalente esatto e non può suddividerlo in una moltiplicazione seguita da un Add.</span><span class="sxs-lookup"><span data-stu-id="f67b8-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="f67b8-109">Viceversa, un valore Multiply seguito da un oggetto Add, in cui uno o entrambi i flag sono contrassegnati come **precisi**, non possono essere Uniti in un oggetto **MAD** con fusibile.</span><span class="sxs-lookup"><span data-stu-id="f67b8-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="f67b8-110">Se il refactoring \_ consentito non è stato specificato, il modificatore **preciso** non è consentito.</span><span class="sxs-lookup"><span data-stu-id="f67b8-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="f67b8-111">Non è necessario perché tutto è preciso.</span><span class="sxs-lookup"><span data-stu-id="f67b8-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="f67b8-112">Il modificatore **preciso** influiscono su qualsiasi operazione, non solo aritmetica.</span><span class="sxs-lookup"><span data-stu-id="f67b8-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f67b8-113">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f67b8-113">Minimum Shader Model</span></span>

<span data-ttu-id="f67b8-114">Questo modificatore è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f67b8-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="f67b8-115">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f67b8-115">Shader Model</span></span>                                              | <span data-ttu-id="f67b8-116">Supportato</span><span class="sxs-lookup"><span data-stu-id="f67b8-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f67b8-117">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f67b8-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f67b8-118">sì</span><span class="sxs-lookup"><span data-stu-id="f67b8-118">yes</span></span>       |
| [<span data-ttu-id="f67b8-119">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f67b8-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f67b8-120">no</span><span class="sxs-lookup"><span data-stu-id="f67b8-120">no</span></span>        |
| [<span data-ttu-id="f67b8-121">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f67b8-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f67b8-122">sì</span><span class="sxs-lookup"><span data-stu-id="f67b8-122">yes</span></span>       |
| [<span data-ttu-id="f67b8-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f67b8-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f67b8-124">no</span><span class="sxs-lookup"><span data-stu-id="f67b8-124">no</span></span>        |
| [<span data-ttu-id="f67b8-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f67b8-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f67b8-126">no</span><span class="sxs-lookup"><span data-stu-id="f67b8-126">no</span></span>        |
| [<span data-ttu-id="f67b8-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f67b8-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f67b8-128">no</span><span class="sxs-lookup"><span data-stu-id="f67b8-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f67b8-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f67b8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f67b8-130">Modificatori di istruzioni Model 5 shader</span><span class="sxs-lookup"><span data-stu-id="f67b8-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 





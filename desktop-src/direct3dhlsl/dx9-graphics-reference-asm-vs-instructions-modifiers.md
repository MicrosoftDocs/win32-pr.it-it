---
title: Modificatori di istruzioni (riferimento di HLSL VS)
description: Modificatori di istruzione
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104472075"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="41e86-103">Modificatori di istruzioni (riferimento di HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="41e86-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="41e86-104">I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41e86-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="41e86-105">\_Sat</span><span class="sxs-lookup"><span data-stu-id="41e86-105">\_sat</span></span>

<span data-ttu-id="41e86-106">Satura (o clamp) il risultato dell'istruzione in \[ 0, 1 \] intervallo prima della scrittura nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41e86-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="41e86-107">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="41e86-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="41e86-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="41e86-108">Where:</span></span>

<span data-ttu-id="41e86-109">DST = morsetto \_ compreso tra \_ 0 \_ e \_ 1 (src0 + src1)</span><span class="sxs-lookup"><span data-stu-id="41e86-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="41e86-110">Il \_ modificatore di istruzioni Sat non costa nessun slot di istruzione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="41e86-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="41e86-111">Se supportato, il \_ modificatore di istruzioni Sat può essere usato con qualsiasi istruzione tranne: [FRC-vs](frc---vs.md), [SinCos-vs](sincos---vs.md)e [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="41e86-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="41e86-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="41e86-112">Vertex shader versions</span></span> | <span data-ttu-id="41e86-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="41e86-113">1\_1</span></span> | <span data-ttu-id="41e86-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41e86-114">2\_0</span></span> | <span data-ttu-id="41e86-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="41e86-115">2\_x</span></span> | <span data-ttu-id="41e86-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41e86-116">2\_sw</span></span> | <span data-ttu-id="41e86-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41e86-117">3\_0</span></span> | <span data-ttu-id="41e86-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41e86-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="41e86-119">\_Sat</span><span class="sxs-lookup"><span data-stu-id="41e86-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="41e86-120">x</span><span class="sxs-lookup"><span data-stu-id="41e86-120">x</span></span>    | <span data-ttu-id="41e86-121">x</span><span class="sxs-lookup"><span data-stu-id="41e86-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="41e86-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41e86-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41e86-123">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="41e86-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





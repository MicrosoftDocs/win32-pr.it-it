---
title: ciclo-PS
description: Avvia un ciclo... blocco EndLoop-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046092"
---
# <a name="loop---ps"></a><span data-ttu-id="ea55a-103">ciclo-PS</span><span class="sxs-lookup"><span data-stu-id="ea55a-103">loop - ps</span></span>

<span data-ttu-id="ea55a-104">Avvia un ciclo... blocco [EndLoop-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="ea55a-104">Starts a loop...[endloop - ps](endloop---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea55a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea55a-105">Syntax</span></span>



| <span data-ttu-id="ea55a-106">ciclo aL, i\#</span><span class="sxs-lookup"><span data-stu-id="ea55a-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="ea55a-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="ea55a-107">Where:</span></span>

-   <span data-ttu-id="ea55a-108">aL è il [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) che contiene il numero di cicli corrente.</span><span class="sxs-lookup"><span data-stu-id="ea55a-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="ea55a-109">i \# è un [Registro di tipo Integer costante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="ea55a-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span> <span data-ttu-id="ea55a-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ea55a-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea55a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea55a-111">Remarks</span></span>



| <span data-ttu-id="ea55a-112">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea55a-112">Pixel shader versions</span></span> | <span data-ttu-id="ea55a-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ea55a-113">1\_1</span></span> | <span data-ttu-id="ea55a-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="ea55a-114">1\_2</span></span> | <span data-ttu-id="ea55a-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ea55a-115">1\_3</span></span> | <span data-ttu-id="ea55a-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="ea55a-116">1\_4</span></span> | <span data-ttu-id="ea55a-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea55a-117">2\_0</span></span> | <span data-ttu-id="ea55a-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ea55a-118">2\_x</span></span> | <span data-ttu-id="ea55a-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ea55a-119">2\_sw</span></span> | <span data-ttu-id="ea55a-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea55a-120">3\_0</span></span> | <span data-ttu-id="ea55a-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ea55a-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ea55a-122">loop</span><span class="sxs-lookup"><span data-stu-id="ea55a-122">loop</span></span>                  |      |      |      |      |      |      |       | <span data-ttu-id="ea55a-123">x</span><span class="sxs-lookup"><span data-stu-id="ea55a-123">x</span></span>    | <span data-ttu-id="ea55a-124">x</span><span class="sxs-lookup"><span data-stu-id="ea55a-124">x</span></span>     |



 

-   <span data-ttu-id="ea55a-125">Il [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) include il numero di cicli corrente e può essere usato per l'indirizzamento relativo nel [Registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) all'interno del blocco del ciclo.</span><span class="sxs-lookup"><span data-stu-id="ea55a-125">The [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) holds the current loop count and can be used for relative addressing into [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) inside the loop block.</span></span>
-   <span data-ttu-id="ea55a-126">i \# . x specifica il numero di iterazioni.</span><span class="sxs-lookup"><span data-stu-id="ea55a-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="ea55a-127">L'intervallo valido è \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="ea55a-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="ea55a-128">Si noti che questa istruzione non incrementa o decrementa il valore di i \# . x.</span><span class="sxs-lookup"><span data-stu-id="ea55a-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="ea55a-129">i \# . y specifica il valore iniziale del registro del [contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al).</span><span class="sxs-lookup"><span data-stu-id="ea55a-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="ea55a-130">L'intervallo valido è \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="ea55a-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="ea55a-131">Si noti che questa istruzione non incrementa o decrementa il valore di i \# . y.</span><span class="sxs-lookup"><span data-stu-id="ea55a-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="ea55a-132">i \# . z specifica la dimensione step/stride.</span><span class="sxs-lookup"><span data-stu-id="ea55a-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="ea55a-133">L'intervallo valido è \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="ea55a-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="ea55a-134">i \# . w non viene usato dal blocco del ciclo e deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="ea55a-134">i\#.w is not used by the loop block and has to be 0.</span></span>
-   <span data-ttu-id="ea55a-135">I blocchi di ciclo possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="ea55a-135">Loop blocks may be nested.</span></span> <span data-ttu-id="ea55a-136">Vedere [limitazioni del controllo di flusso](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="ea55a-136">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="ea55a-137">Quando nidificato, il valore del [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) si riferisce al blocco del ciclo di inclusione immediato.</span><span class="sxs-lookup"><span data-stu-id="ea55a-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="ea55a-138">I blocchi di ciclo possono trovarsi completamente all'interno di un \* blocco if o circondarli completamente.</span><span class="sxs-lookup"><span data-stu-id="ea55a-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="ea55a-139">Nessun a cavallo consentito.</span><span class="sxs-lookup"><span data-stu-id="ea55a-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="ea55a-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea55a-140">Example</span></span>


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="ea55a-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea55a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea55a-142">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="ea55a-142">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: ciclo-vs
description: Avvia un ciclo... blocco ENDLOOP.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993109"
---
# <a name="loop---vs"></a><span data-ttu-id="eb208-103">ciclo-vs</span><span class="sxs-lookup"><span data-stu-id="eb208-103">loop - vs</span></span>

<span data-ttu-id="eb208-104">Avvia un ciclo... blocco [EndLoop](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="eb208-104">Start a loop...[endloop](endloop---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb208-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb208-105">Syntax</span></span>



| <span data-ttu-id="eb208-106">ciclo aL, i\#</span><span class="sxs-lookup"><span data-stu-id="eb208-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="eb208-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="eb208-107">Where:</span></span>

-   <span data-ttu-id="eb208-108">aL è il [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) che contiene il numero di cicli corrente.</span><span class="sxs-lookup"><span data-stu-id="eb208-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="eb208-109">i \# è un [Registro di tipo Integer costante](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="eb208-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span> <span data-ttu-id="eb208-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="eb208-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb208-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb208-111">Remarks</span></span>



| <span data-ttu-id="eb208-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="eb208-112">Vertex shader versions</span></span> | <span data-ttu-id="eb208-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="eb208-113">1\_1</span></span> | <span data-ttu-id="eb208-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eb208-114">2\_0</span></span> | <span data-ttu-id="eb208-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="eb208-115">2\_x</span></span> | <span data-ttu-id="eb208-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eb208-116">2\_sw</span></span> | <span data-ttu-id="eb208-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eb208-117">3\_0</span></span> | <span data-ttu-id="eb208-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eb208-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="eb208-119">loop</span><span class="sxs-lookup"><span data-stu-id="eb208-119">loop</span></span>                   |      | <span data-ttu-id="eb208-120">x</span><span class="sxs-lookup"><span data-stu-id="eb208-120">x</span></span>    | <span data-ttu-id="eb208-121">x</span><span class="sxs-lookup"><span data-stu-id="eb208-121">x</span></span>    | <span data-ttu-id="eb208-122">x</span><span class="sxs-lookup"><span data-stu-id="eb208-122">x</span></span>     | <span data-ttu-id="eb208-123">x</span><span class="sxs-lookup"><span data-stu-id="eb208-123">x</span></span>    | <span data-ttu-id="eb208-124">x</span><span class="sxs-lookup"><span data-stu-id="eb208-124">x</span></span>     |



 

-   <span data-ttu-id="eb208-125">Il [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) include il numero di cicli corrente e può essere usato per l'indirizzamento relativo in un [Registro di tipo Integer costante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) o nei registri di [output](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) all'interno del blocco del ciclo.</span><span class="sxs-lookup"><span data-stu-id="eb208-125">The [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) holds the current loop count, and can be used for relative addressing into [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c\#) or [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) inside the loop block.</span></span>
-   <span data-ttu-id="eb208-126">i \# . x specifica il numero di iterazioni.</span><span class="sxs-lookup"><span data-stu-id="eb208-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="eb208-127">L'intervallo valido è \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="eb208-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="eb208-128">Si noti che questa istruzione non incrementa o decrementa il valore di i \# . x.</span><span class="sxs-lookup"><span data-stu-id="eb208-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="eb208-129">i \# . y specifica il valore iniziale del registro del [contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al).</span><span class="sxs-lookup"><span data-stu-id="eb208-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="eb208-130">L'intervallo valido è \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="eb208-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="eb208-131">Si noti che questa istruzione non incrementa o decrementa il valore di i \# . y.</span><span class="sxs-lookup"><span data-stu-id="eb208-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="eb208-132">i \# . z specifica la dimensione step/stride.</span><span class="sxs-lookup"><span data-stu-id="eb208-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="eb208-133">L'intervallo valido è \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="eb208-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="eb208-134">i \# . w non viene usato e deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="eb208-134">i\#.w is not used and must be set to 0.</span></span>
-   <span data-ttu-id="eb208-135">I blocchi di ciclo possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="eb208-135">Loop blocks may be nested.</span></span> <span data-ttu-id="eb208-136">Vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="eb208-136">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="eb208-137">Quando nidificato, il valore del [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) si riferisce al blocco del ciclo di inclusione immediato.</span><span class="sxs-lookup"><span data-stu-id="eb208-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="eb208-138">I blocchi di ciclo possono trovarsi completamente all'interno di un \* blocco if o circondarli completamente.</span><span class="sxs-lookup"><span data-stu-id="eb208-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="eb208-139">Nessun a cavallo consentito.</span><span class="sxs-lookup"><span data-stu-id="eb208-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="eb208-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="eb208-140">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="eb208-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb208-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb208-142">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="eb208-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





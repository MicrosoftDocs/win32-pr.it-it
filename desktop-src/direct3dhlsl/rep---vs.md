---
title: Rep-vs
description: Avvia una Rep... blocco endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398228"
---
# <a name="rep---vs"></a><span data-ttu-id="530ff-103">Rep-vs</span><span class="sxs-lookup"><span data-stu-id="530ff-103">rep - vs</span></span>

<span data-ttu-id="530ff-104">Avvia una Rep... blocco [endrep](endrep---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="530ff-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="530ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="530ff-105">Syntax</span></span>



| <span data-ttu-id="530ff-106">Rep i\#</span><span class="sxs-lookup"><span data-stu-id="530ff-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="530ff-107">dove i \# è un registro di tipo integer che specifica il numero di ripetizioni nel componente. x.</span><span class="sxs-lookup"><span data-stu-id="530ff-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="530ff-108">Vedere [registro integer costanti](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="530ff-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="530ff-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="530ff-109">Remarks</span></span>



| <span data-ttu-id="530ff-110">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="530ff-110">Vertex shader versions</span></span> | <span data-ttu-id="530ff-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="530ff-111">1\_1</span></span> | <span data-ttu-id="530ff-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="530ff-112">2\_0</span></span> | <span data-ttu-id="530ff-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="530ff-113">2\_x</span></span> | <span data-ttu-id="530ff-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="530ff-114">2\_sw</span></span> | <span data-ttu-id="530ff-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="530ff-115">3\_0</span></span> | <span data-ttu-id="530ff-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="530ff-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="530ff-117">Rep</span><span class="sxs-lookup"><span data-stu-id="530ff-117">rep</span></span>                    |      | <span data-ttu-id="530ff-118">x</span><span class="sxs-lookup"><span data-stu-id="530ff-118">x</span></span>    | <span data-ttu-id="530ff-119">x</span><span class="sxs-lookup"><span data-stu-id="530ff-119">x</span></span>    | <span data-ttu-id="530ff-120">x</span><span class="sxs-lookup"><span data-stu-id="530ff-120">x</span></span>     | <span data-ttu-id="530ff-121">x</span><span class="sxs-lookup"><span data-stu-id="530ff-121">x</span></span>    | <span data-ttu-id="530ff-122">x</span><span class="sxs-lookup"><span data-stu-id="530ff-122">x</span></span>     |



 

-   <span data-ttu-id="530ff-123">i \# . x specifica il numero di iterazioni.</span><span class="sxs-lookup"><span data-stu-id="530ff-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="530ff-124">L'intervallo valido è \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="530ff-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="530ff-125">Si noti che questa istruzione non incrementa o decrementa il valore di i \# . x.</span><span class="sxs-lookup"><span data-stu-id="530ff-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="530ff-126">i \# . yzw non vengono utilizzati dal blocco REPEAT.</span><span class="sxs-lookup"><span data-stu-id="530ff-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="530ff-127">I blocchi di ripetizione possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="530ff-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="530ff-128">Vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="530ff-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="530ff-129">I blocchi di ripetizione possono trovarsi completamente all'interno di un \* blocco if o circondarli completamente.</span><span class="sxs-lookup"><span data-stu-id="530ff-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="530ff-130">Nessun a cavallo consentito.</span><span class="sxs-lookup"><span data-stu-id="530ff-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="530ff-131">L'uso della stessa i \# per le istruzioni di rep diverse o nidificate è corretto. ogni ciclo viene iterato in base al numero specificato.</span><span class="sxs-lookup"><span data-stu-id="530ff-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="530ff-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="530ff-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="530ff-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="530ff-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="530ff-134">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="530ff-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





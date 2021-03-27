---
title: Rep-PS
description: Avvia una Rep... blocco endrep-PS.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719387"
---
# <a name="rep---ps"></a><span data-ttu-id="821df-103">Rep-PS</span><span class="sxs-lookup"><span data-stu-id="821df-103">rep - ps</span></span>

<span data-ttu-id="821df-104">Avvia una Rep... blocco [endrep-PS](endrep---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="821df-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="821df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="821df-105">Syntax</span></span>



| <span data-ttu-id="821df-106">Rep i\#</span><span class="sxs-lookup"><span data-stu-id="821df-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="821df-107">dove i \# è un registro di tipo integer che specifica il numero di ripetizioni nel componente. x.</span><span class="sxs-lookup"><span data-stu-id="821df-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="821df-108">Vedere [registro integer costanti](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="821df-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="821df-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="821df-109">Remarks</span></span>



| <span data-ttu-id="821df-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="821df-110">Pixel shader versions</span></span> | <span data-ttu-id="821df-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="821df-111">1\_1</span></span> | <span data-ttu-id="821df-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="821df-112">1\_2</span></span> | <span data-ttu-id="821df-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="821df-113">1\_3</span></span> | <span data-ttu-id="821df-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="821df-114">1\_4</span></span> | <span data-ttu-id="821df-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="821df-115">2\_0</span></span> | <span data-ttu-id="821df-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="821df-116">2\_x</span></span> | <span data-ttu-id="821df-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="821df-117">2\_sw</span></span> | <span data-ttu-id="821df-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="821df-118">3\_0</span></span> | <span data-ttu-id="821df-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="821df-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="821df-120">Rep</span><span class="sxs-lookup"><span data-stu-id="821df-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="821df-121">x</span><span class="sxs-lookup"><span data-stu-id="821df-121">x</span></span>    | <span data-ttu-id="821df-122">x</span><span class="sxs-lookup"><span data-stu-id="821df-122">x</span></span>     | <span data-ttu-id="821df-123">x</span><span class="sxs-lookup"><span data-stu-id="821df-123">x</span></span>    | <span data-ttu-id="821df-124">x</span><span class="sxs-lookup"><span data-stu-id="821df-124">x</span></span>     |



 

-   <span data-ttu-id="821df-125">i \# . x specifica il numero di iterazioni.</span><span class="sxs-lookup"><span data-stu-id="821df-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="821df-126">L'intervallo valido è \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="821df-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="821df-127">Si noti che questa istruzione non incrementa o decrementa il valore di i \# . x.</span><span class="sxs-lookup"><span data-stu-id="821df-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="821df-128">i \# . yzw non vengono utilizzati dal blocco REPEAT.</span><span class="sxs-lookup"><span data-stu-id="821df-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="821df-129">I blocchi di ripetizione possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="821df-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="821df-130">Vedere [limitazioni del controllo di flusso](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="821df-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="821df-131">I blocchi di ripetizione possono trovarsi completamente all'interno di un \* blocco if o circondarli completamente.</span><span class="sxs-lookup"><span data-stu-id="821df-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="821df-132">Nessun a cavallo consentito.</span><span class="sxs-lookup"><span data-stu-id="821df-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="821df-133">L'uso della stessa i \# per le istruzioni di rep diverse o nidificate è corretto. ogni ciclo viene iterato in base al numero specificato.</span><span class="sxs-lookup"><span data-stu-id="821df-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="821df-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="821df-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="821df-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="821df-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="821df-136">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="821df-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





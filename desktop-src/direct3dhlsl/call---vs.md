---
title: Call-vs
description: Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita. | Call-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969280"
---
# <a name="call---vs"></a><span data-ttu-id="06bd2-104">Call-vs</span><span class="sxs-lookup"><span data-stu-id="06bd2-104">call - vs</span></span>

<span data-ttu-id="06bd2-105">Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita.</span><span class="sxs-lookup"><span data-stu-id="06bd2-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="06bd2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06bd2-106">Syntax</span></span>



| <span data-ttu-id="06bd2-107">chiama l\#</span><span class="sxs-lookup"><span data-stu-id="06bd2-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="06bd2-108">dove l \# è un' [etichetta-vs](label---vs.md) che contrassegna l'inizio della subroutine da chiamare.</span><span class="sxs-lookup"><span data-stu-id="06bd2-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="06bd2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="06bd2-109">Remarks</span></span>



| <span data-ttu-id="06bd2-110">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="06bd2-110">Vertex shader versions</span></span> | <span data-ttu-id="06bd2-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="06bd2-111">1\_1</span></span> | <span data-ttu-id="06bd2-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="06bd2-112">2\_0</span></span> | <span data-ttu-id="06bd2-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="06bd2-113">2\_x</span></span> | <span data-ttu-id="06bd2-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="06bd2-114">2\_sw</span></span> | <span data-ttu-id="06bd2-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="06bd2-115">3\_0</span></span> | <span data-ttu-id="06bd2-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="06bd2-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="06bd2-117">chiamare</span><span class="sxs-lookup"><span data-stu-id="06bd2-117">call</span></span>                   |      | <span data-ttu-id="06bd2-118">x</span><span class="sxs-lookup"><span data-stu-id="06bd2-118">x</span></span>    | <span data-ttu-id="06bd2-119">x</span><span class="sxs-lookup"><span data-stu-id="06bd2-119">x</span></span>    | <span data-ttu-id="06bd2-120">x</span><span class="sxs-lookup"><span data-stu-id="06bd2-120">x</span></span>     | <span data-ttu-id="06bd2-121">x</span><span class="sxs-lookup"><span data-stu-id="06bd2-121">x</span></span>    | <span data-ttu-id="06bd2-122">x</span><span class="sxs-lookup"><span data-stu-id="06bd2-122">x</span></span>     |



 

<span data-ttu-id="06bd2-123">Questa istruzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="06bd2-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="06bd2-124">Indirizzo push dell'istruzione successiva allo stack di indirizzi restituito.</span><span class="sxs-lookup"><span data-stu-id="06bd2-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="06bd2-125">Continua l'esecuzione dall'istruzione contrassegnata dall'etichetta.</span><span class="sxs-lookup"><span data-stu-id="06bd2-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="06bd2-126">In vertex shader 2 \_ 0 non sono consentite chiamate di annidamento.</span><span class="sxs-lookup"><span data-stu-id="06bd2-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="06bd2-127">In vertex shader 2 \_ x la profondità di annidamento è limitata dall'elemento StaticFlowControlDepth della struttura [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) .</span><span class="sxs-lookup"><span data-stu-id="06bd2-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="06bd2-128">Per ulteriori informazioni, vedere [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span><span class="sxs-lookup"><span data-stu-id="06bd2-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="06bd2-129">In vertex shader 3 \_ 0 sono consentiti quattro livelli di annidamento delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="06bd2-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="06bd2-130">Sono consentite solo chiamate in diretta.</span><span class="sxs-lookup"><span data-stu-id="06bd2-130">Only forward calls are allowed.</span></span> <span data-ttu-id="06bd2-131">Ciò significa che la posizione dell'etichetta all'interno del vertex shader deve essere successiva all'istruzione di chiamata a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="06bd2-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="06bd2-132">Se un'istruzione di chiamata viene richiamata all'interno del [ciclo](loop---vs.md)... [EndLoop](endloop---vs.md) Block, il valore del [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) è accessibile all'interno della subroutine.</span><span class="sxs-lookup"><span data-stu-id="06bd2-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="06bd2-133">Se una subroutine fa riferimento al [registro del contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) che si trova all'esterno della subroutine, ogni istanza della chiamata a questa subroutine dovrebbe essere racchiusa da un [ciclo](loop---vs.md)... blocco [EndLoop](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="06bd2-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06bd2-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06bd2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06bd2-135">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="06bd2-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 

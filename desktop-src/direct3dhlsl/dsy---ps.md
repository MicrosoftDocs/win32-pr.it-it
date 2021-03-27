---
title: DSY-PS
description: Calcola il tasso di modifica nella direzione y della destinazione di rendering.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398218"
---
# <a name="dsy---ps"></a><span data-ttu-id="c8c5c-103">DSY-PS</span><span class="sxs-lookup"><span data-stu-id="c8c5c-103">dsy - ps</span></span>

<span data-ttu-id="c8c5c-104">Calcola il tasso di modifica nella direzione y della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="c8c5c-104">Compute the rate of change in the render target's y-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8c5c-105">Syntax</span></span>



| <span data-ttu-id="c8c5c-106">DSY DST, src</span><span class="sxs-lookup"><span data-stu-id="c8c5c-106">dsy dst, src</span></span> |
|--------------|



 

<span data-ttu-id="c8c5c-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="c8c5c-107">Where:</span></span>

-   <span data-ttu-id="c8c5c-108">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c8c5c-108">dst is a destination register.</span></span>
-   <span data-ttu-id="c8c5c-109">src è un registro di origine di input.</span><span class="sxs-lookup"><span data-stu-id="c8c5c-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c5c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8c5c-110">Remarks</span></span>



| <span data-ttu-id="c8c5c-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="c8c5c-111">Pixel shader versions</span></span> | <span data-ttu-id="c8c5c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="c8c5c-112">1\_1</span></span> | <span data-ttu-id="c8c5c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="c8c5c-113">1\_2</span></span> | <span data-ttu-id="c8c5c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c8c5c-114">1\_3</span></span> | <span data-ttu-id="c8c5c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="c8c5c-115">1\_4</span></span> | <span data-ttu-id="c8c5c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c8c5c-116">2\_0</span></span> | <span data-ttu-id="c8c5c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c8c5c-117">2\_x</span></span> | <span data-ttu-id="c8c5c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c8c5c-118">2\_sw</span></span> | <span data-ttu-id="c8c5c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c8c5c-119">3\_0</span></span> | <span data-ttu-id="c8c5c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c8c5c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c8c5c-121">DSY</span><span class="sxs-lookup"><span data-stu-id="c8c5c-121">dsy</span></span>                   |      |      |      |      |      | <span data-ttu-id="c8c5c-122">x</span><span class="sxs-lookup"><span data-stu-id="c8c5c-122">x</span></span>    | <span data-ttu-id="c8c5c-123">x</span><span class="sxs-lookup"><span data-stu-id="c8c5c-123">x</span></span>     | <span data-ttu-id="c8c5c-124">x</span><span class="sxs-lookup"><span data-stu-id="c8c5c-124">x</span></span>    | <span data-ttu-id="c8c5c-125">x</span><span class="sxs-lookup"><span data-stu-id="c8c5c-125">x</span></span>     |



 

<span data-ttu-id="c8c5c-126">La frequenza delle modifiche calcolate dal registro di origine è un'approssimazione del contenuto dello stesso registro in pixel adiacenti che eseguono il pixel shader in lock-step con il pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="c8c5c-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="c8c5c-127">Le istruzioni [DSX](dsx---ps.md) e DSY calcolano il risultato esaminando il contenuto corrente del registro di origine (per componente) per i diversi pixel nell'area locale in esecuzione nel passaggio di blocco.</span><span class="sxs-lookup"><span data-stu-id="c8c5c-127">The [dsx](dsx---ps.md) And dsy instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="c8c5c-128">La formula esatta utilizzata per calcolare la sfumatura varia in base all'hardware, ma deve essere coerente con il modo in cui l'hardware esegue le stesse operazioni come parte del processo di calcolo del livello di dettaglio per il campionamento della trama.</span><span class="sxs-lookup"><span data-stu-id="c8c5c-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8c5c-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8c5c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8c5c-130">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="c8c5c-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="c8c5c-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="c8c5c-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 





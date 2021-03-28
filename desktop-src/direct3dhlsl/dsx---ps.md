---
title: DSX-PS
description: Calcola il tasso di modifica nella direzione x della destinazione di rendering.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956081"
---
# <a name="dsx---ps"></a><span data-ttu-id="e608d-103">DSX-PS</span><span class="sxs-lookup"><span data-stu-id="e608d-103">dsx - ps</span></span>

<span data-ttu-id="e608d-104">Calcola il tasso di modifica nella direzione x della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e608d-104">Compute the rate of change in the render target's x-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e608d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e608d-105">Syntax</span></span>



| <span data-ttu-id="e608d-106">DSX DST, src</span><span class="sxs-lookup"><span data-stu-id="e608d-106">dsx dst, src</span></span> |
|--------------|



 

<span data-ttu-id="e608d-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="e608d-107">Where:</span></span>

-   <span data-ttu-id="e608d-108">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e608d-108">dst is a destination register.</span></span>
-   <span data-ttu-id="e608d-109">src è un registro di origine di input.</span><span class="sxs-lookup"><span data-stu-id="e608d-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e608d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e608d-110">Remarks</span></span>



| <span data-ttu-id="e608d-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e608d-111">Pixel shader versions</span></span> | <span data-ttu-id="e608d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e608d-112">1\_1</span></span> | <span data-ttu-id="e608d-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e608d-113">1\_2</span></span> | <span data-ttu-id="e608d-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e608d-114">1\_3</span></span> | <span data-ttu-id="e608d-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e608d-115">1\_4</span></span> | <span data-ttu-id="e608d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e608d-116">2\_0</span></span> | <span data-ttu-id="e608d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e608d-117">2\_x</span></span> | <span data-ttu-id="e608d-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e608d-118">2\_sw</span></span> | <span data-ttu-id="e608d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e608d-119">3\_0</span></span> | <span data-ttu-id="e608d-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e608d-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e608d-121">DSX</span><span class="sxs-lookup"><span data-stu-id="e608d-121">dsx</span></span>                   |      |      |      |      |      | <span data-ttu-id="e608d-122">x</span><span class="sxs-lookup"><span data-stu-id="e608d-122">x</span></span>    | <span data-ttu-id="e608d-123">x</span><span class="sxs-lookup"><span data-stu-id="e608d-123">x</span></span>     | <span data-ttu-id="e608d-124">x</span><span class="sxs-lookup"><span data-stu-id="e608d-124">x</span></span>    | <span data-ttu-id="e608d-125">x</span><span class="sxs-lookup"><span data-stu-id="e608d-125">x</span></span>     |



 

<span data-ttu-id="e608d-126">La frequenza delle modifiche calcolate dal registro di origine è un'approssimazione del contenuto dello stesso registro in pixel adiacenti che eseguono il pixel shader in lock-step con il pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="e608d-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="e608d-127">Le istruzioni DSX e [DSY](dsy---ps.md) calcolano il risultato esaminando il contenuto corrente del registro di origine (per componente) per i diversi pixel nell'area locale in esecuzione nel passaggio di blocco.</span><span class="sxs-lookup"><span data-stu-id="e608d-127">The dsx And [dsy](dsy---ps.md) instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="e608d-128">La formula esatta utilizzata per calcolare la sfumatura varia in base all'hardware, ma deve essere coerente con il modo in cui l'hardware esegue le stesse operazioni come parte del processo di calcolo del livello di dettaglio per il campionamento della trama.</span><span class="sxs-lookup"><span data-stu-id="e608d-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e608d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e608d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e608d-130">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e608d-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="e608d-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="e608d-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 





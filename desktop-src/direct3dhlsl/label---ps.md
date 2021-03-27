---
title: etichetta-PS
description: Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta. | etichetta-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995576"
---
# <a name="label---ps"></a><span data-ttu-id="978b8-104">etichetta-PS</span><span class="sxs-lookup"><span data-stu-id="978b8-104">label - ps</span></span>

<span data-ttu-id="978b8-105">Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta.</span><span class="sxs-lookup"><span data-stu-id="978b8-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="978b8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="978b8-106">Syntax</span></span>



| <span data-ttu-id="978b8-107">etichetta l\#</span><span class="sxs-lookup"><span data-stu-id="978b8-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="978b8-108">dove \# identifica il numero di etichetta.</span><span class="sxs-lookup"><span data-stu-id="978b8-108">where \# identifies the label number.</span></span>

<span data-ttu-id="978b8-109">Per PS \_ 2 \_ x, il numero di etichetta deve essere compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="978b8-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="978b8-110">Per PS \_ 2 \_ SW, PS \_ 3 \_ 0 e PS \_ 3 \_ SW, il numero di etichetta deve essere compreso tra 0 e 2047.</span><span class="sxs-lookup"><span data-stu-id="978b8-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="978b8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="978b8-111">Remarks</span></span>



| <span data-ttu-id="978b8-112">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="978b8-112">Pixel shader versions</span></span> | <span data-ttu-id="978b8-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="978b8-113">1\_1</span></span> | <span data-ttu-id="978b8-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="978b8-114">1\_2</span></span> | <span data-ttu-id="978b8-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="978b8-115">1\_3</span></span> | <span data-ttu-id="978b8-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="978b8-116">1\_4</span></span> | <span data-ttu-id="978b8-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="978b8-117">2\_0</span></span> | <span data-ttu-id="978b8-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="978b8-118">2\_x</span></span> | <span data-ttu-id="978b8-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="978b8-119">2\_sw</span></span> | <span data-ttu-id="978b8-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="978b8-120">3\_0</span></span> | <span data-ttu-id="978b8-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="978b8-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="978b8-122">label</span><span class="sxs-lookup"><span data-stu-id="978b8-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="978b8-123">x</span><span class="sxs-lookup"><span data-stu-id="978b8-123">x</span></span>    | <span data-ttu-id="978b8-124">x</span><span class="sxs-lookup"><span data-stu-id="978b8-124">x</span></span>     | <span data-ttu-id="978b8-125">x</span><span class="sxs-lookup"><span data-stu-id="978b8-125">x</span></span>    | <span data-ttu-id="978b8-126">x</span><span class="sxs-lookup"><span data-stu-id="978b8-126">x</span></span>     |



 

<span data-ttu-id="978b8-127">Questa istruzione definisce un'etichetta che si trova nella successiva istruzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="978b8-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="978b8-128">L'istruzione label può essere presente solo subito dopo un'istruzione [ret](ret---ps.md) (che definisce la fine della subroutine o del programma principale precedente).</span><span class="sxs-lookup"><span data-stu-id="978b8-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="978b8-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="978b8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="978b8-130">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="978b8-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





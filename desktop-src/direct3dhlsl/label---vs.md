---
title: etichetta-vs
description: Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta. | etichetta-vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995723"
---
# <a name="label---vs"></a><span data-ttu-id="24902-104">etichetta-vs</span><span class="sxs-lookup"><span data-stu-id="24902-104">label - vs</span></span>

<span data-ttu-id="24902-105">Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta.</span><span class="sxs-lookup"><span data-stu-id="24902-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="24902-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24902-106">Syntax</span></span>



| <span data-ttu-id="24902-107">etichetta l\#</span><span class="sxs-lookup"><span data-stu-id="24902-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="24902-108">dove \# identifica il numero di etichetta.</span><span class="sxs-lookup"><span data-stu-id="24902-108">where \# identifies the label number.</span></span>

<span data-ttu-id="24902-109">Per vs \_ 2 \_ 0 e vs \_ 2 \_ x, il numero di etichetta deve essere compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="24902-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="24902-110">Per vs \_ 2 \_ SW, vs \_ 3 \_ 0 e vs \_ 3 \_ SW, il numero di etichetta deve essere compreso tra 0 e 2047.</span><span class="sxs-lookup"><span data-stu-id="24902-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="24902-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="24902-111">Remarks</span></span>



| <span data-ttu-id="24902-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="24902-112">Vertex shader versions</span></span> | <span data-ttu-id="24902-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="24902-113">1\_1</span></span> | <span data-ttu-id="24902-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24902-114">2\_0</span></span> | <span data-ttu-id="24902-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="24902-115">2\_x</span></span> | <span data-ttu-id="24902-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="24902-116">2\_sw</span></span> | <span data-ttu-id="24902-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24902-117">3\_0</span></span> | <span data-ttu-id="24902-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="24902-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="24902-119">label</span><span class="sxs-lookup"><span data-stu-id="24902-119">label</span></span>                  |      | <span data-ttu-id="24902-120">x</span><span class="sxs-lookup"><span data-stu-id="24902-120">x</span></span>    | <span data-ttu-id="24902-121">x</span><span class="sxs-lookup"><span data-stu-id="24902-121">x</span></span>    | <span data-ttu-id="24902-122">x</span><span class="sxs-lookup"><span data-stu-id="24902-122">x</span></span>     | <span data-ttu-id="24902-123">x</span><span class="sxs-lookup"><span data-stu-id="24902-123">x</span></span>    | <span data-ttu-id="24902-124">x</span><span class="sxs-lookup"><span data-stu-id="24902-124">x</span></span>     |



 

<span data-ttu-id="24902-125">Questa istruzione definisce un'etichetta che si trova nella successiva istruzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="24902-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="24902-126">L'istruzione label può essere presente solo subito dopo un'istruzione [ret](ret---vs.md) (che definisce la fine della subroutine o del programma principale precedente).</span><span class="sxs-lookup"><span data-stu-id="24902-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24902-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24902-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24902-128">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="24902-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





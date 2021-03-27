---
title: chiamata a PS
description: Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita. | chiamata a PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995493"
---
# <a name="call---ps"></a><span data-ttu-id="1bd2b-104">chiamata a PS</span><span class="sxs-lookup"><span data-stu-id="1bd2b-104">call - ps</span></span>

<span data-ttu-id="1bd2b-105">Esegue una chiamata di funzione all'istruzione contrassegnata con l'etichetta fornita.</span><span class="sxs-lookup"><span data-stu-id="1bd2b-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd2b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bd2b-106">Syntax</span></span>



| <span data-ttu-id="1bd2b-107">chiama l\#</span><span class="sxs-lookup"><span data-stu-id="1bd2b-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="1bd2b-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="1bd2b-108">Where:</span></span>

-   <span data-ttu-id="1bd2b-109">l \# è un' [etichetta-PS](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.</span><span class="sxs-lookup"><span data-stu-id="1bd2b-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bd2b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bd2b-110">Remarks</span></span>



| <span data-ttu-id="1bd2b-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="1bd2b-111">Pixel shader versions</span></span> | <span data-ttu-id="1bd2b-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="1bd2b-112">1\_1</span></span> | <span data-ttu-id="1bd2b-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="1bd2b-113">1\_2</span></span> | <span data-ttu-id="1bd2b-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1bd2b-114">1\_3</span></span> | <span data-ttu-id="1bd2b-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="1bd2b-115">1\_4</span></span> | <span data-ttu-id="1bd2b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1bd2b-116">2\_0</span></span> | <span data-ttu-id="1bd2b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1bd2b-117">2\_x</span></span> | <span data-ttu-id="1bd2b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1bd2b-118">2\_sw</span></span> | <span data-ttu-id="1bd2b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1bd2b-119">3\_0</span></span> | <span data-ttu-id="1bd2b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1bd2b-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1bd2b-121">chiamare</span><span class="sxs-lookup"><span data-stu-id="1bd2b-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="1bd2b-122">x</span><span class="sxs-lookup"><span data-stu-id="1bd2b-122">x</span></span>    | <span data-ttu-id="1bd2b-123">x</span><span class="sxs-lookup"><span data-stu-id="1bd2b-123">x</span></span>     | <span data-ttu-id="1bd2b-124">x</span><span class="sxs-lookup"><span data-stu-id="1bd2b-124">x</span></span>    | <span data-ttu-id="1bd2b-125">x</span><span class="sxs-lookup"><span data-stu-id="1bd2b-125">x</span></span>     |



 

<span data-ttu-id="1bd2b-126">Questa istruzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1bd2b-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="1bd2b-127">Indirizzo push dell'istruzione successiva allo stack di indirizzi restituito.</span><span class="sxs-lookup"><span data-stu-id="1bd2b-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="1bd2b-128">Continua l'esecuzione dall'istruzione contrassegnata dall'etichetta.</span><span class="sxs-lookup"><span data-stu-id="1bd2b-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bd2b-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bd2b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd2b-130">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="1bd2b-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: dcl_samplerType (sm3 - vs asm)
description: Dichiarare un campionatore di vertex shader.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129869"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="53b2a-103">dcl \_ samplerType (sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="53b2a-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="53b2a-104">Dichiarare un campionatore di vertex shader.</span><span class="sxs-lookup"><span data-stu-id="53b2a-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b2a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53b2a-105">Syntax</span></span>

<span data-ttu-id="53b2a-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="53b2a-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="53b2a-107">dove:</span><span class="sxs-lookup"><span data-stu-id="53b2a-107">where:</span></span>

-   <span data-ttu-id="53b2a-108">\_samplerType definisce il tipo di dati sampler.</span><span class="sxs-lookup"><span data-stu-id="53b2a-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="53b2a-109">In questo modo viene determinato il numero di coordinate richieste da ogni coordinata di trama durante il campionamento.</span><span class="sxs-lookup"><span data-stu-id="53b2a-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="53b2a-110">Vengono definite le dimensioni delle coordinate di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="53b2a-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="53b2a-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="53b2a-111">\_2d</span></span>
    -   <span data-ttu-id="53b2a-112">\_Cubo</span><span class="sxs-lookup"><span data-stu-id="53b2a-112">\_cube</span></span>
    -   <span data-ttu-id="53b2a-113">\_Volume</span><span class="sxs-lookup"><span data-stu-id="53b2a-113">\_volume</span></span>
-   <span data-ttu-id="53b2a-114">s \# identifica un campionatore, dove s è un'abbreviazione del campionatore e \# è il numero del campionatore.</span><span class="sxs-lookup"><span data-stu-id="53b2a-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="53b2a-115">[I sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)sono pseudoregistri perché non è possibile leggerli o scriverli direttamente.</span><span class="sxs-lookup"><span data-stu-id="53b2a-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b2a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="53b2a-116">Remarks</span></span>



| <span data-ttu-id="53b2a-117">Versioni di vertex shader</span><span class="sxs-lookup"><span data-stu-id="53b2a-117">Vertex shader versions</span></span> | <span data-ttu-id="53b2a-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="53b2a-118">1\_1</span></span> | <span data-ttu-id="53b2a-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53b2a-119">2\_0</span></span> | <span data-ttu-id="53b2a-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53b2a-120">2\_x</span></span> | <span data-ttu-id="53b2a-121">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="53b2a-121">2\_sw</span></span> | <span data-ttu-id="53b2a-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53b2a-122">3\_0</span></span> | <span data-ttu-id="53b2a-123">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="53b2a-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="53b2a-124">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="53b2a-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="53b2a-125">x</span><span class="sxs-lookup"><span data-stu-id="53b2a-125">x</span></span>    | <span data-ttu-id="53b2a-126">x</span><span class="sxs-lookup"><span data-stu-id="53b2a-126">x</span></span>     |



 

<span data-ttu-id="53b2a-127">Tutte le istruzioni dcl \_ samplerType devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="53b2a-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53b2a-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53b2a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53b2a-129">Istruzioni per vertex shader</span><span class="sxs-lookup"><span data-stu-id="53b2a-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





---
title: dcl_samplerType (SM3-vs ASM)
description: Dichiarare un campionatore vertex shader.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993205"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="3957e-103">DCL \_ samplerType (SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="3957e-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="3957e-104">Dichiarare un campionatore vertex shader.</span><span class="sxs-lookup"><span data-stu-id="3957e-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="3957e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3957e-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="3957e-106">samplerType di DCL \_\#</span><span class="sxs-lookup"><span data-stu-id="3957e-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="3957e-107">dove:</span><span class="sxs-lookup"><span data-stu-id="3957e-107">where:</span></span>

-   <span data-ttu-id="3957e-108">\_samplerType definisce il tipo di dati del campionatore.</span><span class="sxs-lookup"><span data-stu-id="3957e-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="3957e-109">Determina il numero di coordinate necessarie per ogni coordinata di trama durante il campionamento.</span><span class="sxs-lookup"><span data-stu-id="3957e-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="3957e-110">Sono definite le dimensioni delle coordinate di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="3957e-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="3957e-111">\_2D</span><span class="sxs-lookup"><span data-stu-id="3957e-111">\_2d</span></span>
    -   <span data-ttu-id="3957e-112">\_cubo</span><span class="sxs-lookup"><span data-stu-id="3957e-112">\_cube</span></span>
    -   <span data-ttu-id="3957e-113">\_volume</span><span class="sxs-lookup"><span data-stu-id="3957e-113">\_volume</span></span>
-   <span data-ttu-id="3957e-114">s \# identifica un campionatore dove s è un'abbreviazione del campionatore e \# è il numero di campionatore.</span><span class="sxs-lookup"><span data-stu-id="3957e-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="3957e-115">[Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s sono pseudo-registri perché non è possibile leggere o scrivere direttamente.</span><span class="sxs-lookup"><span data-stu-id="3957e-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="3957e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3957e-116">Remarks</span></span>



| <span data-ttu-id="3957e-117">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="3957e-117">Vertex shader versions</span></span> | <span data-ttu-id="3957e-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="3957e-118">1\_1</span></span> | <span data-ttu-id="3957e-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3957e-119">2\_0</span></span> | <span data-ttu-id="3957e-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3957e-120">2\_x</span></span> | <span data-ttu-id="3957e-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3957e-121">2\_sw</span></span> | <span data-ttu-id="3957e-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3957e-122">3\_0</span></span> | <span data-ttu-id="3957e-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3957e-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3957e-124">\_samplerType DCL</span><span class="sxs-lookup"><span data-stu-id="3957e-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="3957e-125">x</span><span class="sxs-lookup"><span data-stu-id="3957e-125">x</span></span>    | <span data-ttu-id="3957e-126">x</span><span class="sxs-lookup"><span data-stu-id="3957e-126">x</span></span>     |



 

<span data-ttu-id="3957e-127">Tutte le \_ istruzioni samplerType di DCL devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="3957e-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3957e-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3957e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3957e-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="3957e-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





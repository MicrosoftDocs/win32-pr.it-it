---
title: dcl - (sm2, sm3 - ps asm)
description: Dichiarare un registro pixel shader di input.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130100"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="d39cd-103">dcl - (sm2, sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="d39cd-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="d39cd-104">Dichiarare un registro pixel shader di input.</span><span class="sxs-lookup"><span data-stu-id="d39cd-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d39cd-105">Syntax</span></span>

<span data-ttu-id="d39cd-106">dcl \[ \_ pp \] dest \[ .mask\]</span><span class="sxs-lookup"><span data-stu-id="d39cd-106">dcl\[\_pp\] dest\[.mask\]</span></span>



 

<span data-ttu-id="d39cd-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="d39cd-107">Where:</span></span>

-   <span data-ttu-id="d39cd-108">\[\_pp \] è una precisione parziale facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d39cd-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="d39cd-109">Vedere [Precisione parziale.](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)</span><span class="sxs-lookup"><span data-stu-id="d39cd-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="d39cd-110">dest è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d39cd-110">dest is a destination register.</span></span> <span data-ttu-id="d39cd-111">Deve essere un registro colori [di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) o un registro delle coordinate di [trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span><span class="sxs-lookup"><span data-stu-id="d39cd-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="d39cd-112">\[.mask è una maschera di scrittura facoltativa che controlla i componenti del registro di \] destinazione in cui è possibile scrivere.</span><span class="sxs-lookup"><span data-stu-id="d39cd-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="d39cd-113">Vedere [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="d39cd-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d39cd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d39cd-114">Remarks</span></span>



| <span data-ttu-id="d39cd-115">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="d39cd-115">Pixel shader versions</span></span> | <span data-ttu-id="d39cd-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="d39cd-116">1\_1</span></span> | <span data-ttu-id="d39cd-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="d39cd-117">1\_2</span></span> | <span data-ttu-id="d39cd-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d39cd-118">1\_3</span></span> | <span data-ttu-id="d39cd-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="d39cd-119">1\_4</span></span> | <span data-ttu-id="d39cd-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d39cd-120">2\_0</span></span> | <span data-ttu-id="d39cd-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d39cd-121">2\_x</span></span> | <span data-ttu-id="d39cd-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d39cd-122">2\_sw</span></span> | <span data-ttu-id="d39cd-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d39cd-123">3\_0</span></span> | <span data-ttu-id="d39cd-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d39cd-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d39cd-125">Dcl</span><span class="sxs-lookup"><span data-stu-id="d39cd-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="d39cd-126">x</span><span class="sxs-lookup"><span data-stu-id="d39cd-126">x</span></span>    | <span data-ttu-id="d39cd-127">x</span><span class="sxs-lookup"><span data-stu-id="d39cd-127">x</span></span>    | <span data-ttu-id="d39cd-128">x</span><span class="sxs-lookup"><span data-stu-id="d39cd-128">x</span></span>     | <span data-ttu-id="d39cd-129">x</span><span class="sxs-lookup"><span data-stu-id="d39cd-129">x</span></span>    | <span data-ttu-id="d39cd-130">x</span><span class="sxs-lookup"><span data-stu-id="d39cd-130">x</span></span>     |



 

<span data-ttu-id="d39cd-131">Tutte le istruzioni dcl devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="d39cd-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d39cd-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d39cd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d39cd-133">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="d39cd-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





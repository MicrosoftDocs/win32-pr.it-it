---
title: DCL-(SM2, SM3-PS ASM)
description: Dichiarare un registro pixel shader input.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398270"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="1ee06-103">DCL-(SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="1ee06-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="1ee06-104">Dichiarare un registro pixel shader input.</span><span class="sxs-lookup"><span data-stu-id="1ee06-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ee06-105">Syntax</span></span>



|                           |
|---------------------------|
| <span data-ttu-id="1ee06-106">\[ \_ \] dest \[ . mask di DCL PP\]</span><span class="sxs-lookup"><span data-stu-id="1ee06-106">dcl\[\_pp\] dest\[.mask\]</span></span> |



 

<span data-ttu-id="1ee06-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="1ee06-107">Where:</span></span>

-   <span data-ttu-id="1ee06-108">\[\_PP \] è una precisione parziale facoltativa.</span><span class="sxs-lookup"><span data-stu-id="1ee06-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="1ee06-109">Vedere [precisione parziale](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="1ee06-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="1ee06-110">dest è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1ee06-110">dest is a destination register.</span></span> <span data-ttu-id="1ee06-111">Deve essere un registro del [colore di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) o un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).</span><span class="sxs-lookup"><span data-stu-id="1ee06-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="1ee06-112">\[. mask \] è una maschera di scrittura facoltativa che controlla i componenti del registro di destinazione in cui è possibile scrivere.</span><span class="sxs-lookup"><span data-stu-id="1ee06-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="1ee06-113">Vedere la [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="1ee06-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ee06-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ee06-114">Remarks</span></span>



| <span data-ttu-id="1ee06-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="1ee06-115">Pixel shader versions</span></span> | <span data-ttu-id="1ee06-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="1ee06-116">1\_1</span></span> | <span data-ttu-id="1ee06-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="1ee06-117">1\_2</span></span> | <span data-ttu-id="1ee06-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1ee06-118">1\_3</span></span> | <span data-ttu-id="1ee06-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="1ee06-119">1\_4</span></span> | <span data-ttu-id="1ee06-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ee06-120">2\_0</span></span> | <span data-ttu-id="1ee06-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1ee06-121">2\_x</span></span> | <span data-ttu-id="1ee06-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1ee06-122">2\_sw</span></span> | <span data-ttu-id="1ee06-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ee06-123">3\_0</span></span> | <span data-ttu-id="1ee06-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1ee06-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1ee06-125">DCL</span><span class="sxs-lookup"><span data-stu-id="1ee06-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="1ee06-126">x</span><span class="sxs-lookup"><span data-stu-id="1ee06-126">x</span></span>    | <span data-ttu-id="1ee06-127">x</span><span class="sxs-lookup"><span data-stu-id="1ee06-127">x</span></span>    | <span data-ttu-id="1ee06-128">x</span><span class="sxs-lookup"><span data-stu-id="1ee06-128">x</span></span>     | <span data-ttu-id="1ee06-129">x</span><span class="sxs-lookup"><span data-stu-id="1ee06-129">x</span></span>    | <span data-ttu-id="1ee06-130">x</span><span class="sxs-lookup"><span data-stu-id="1ee06-130">x</span></span>     |



 

<span data-ttu-id="1ee06-131">Tutte le istruzioni di DCL devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="1ee06-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ee06-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ee06-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee06-133">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="1ee06-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





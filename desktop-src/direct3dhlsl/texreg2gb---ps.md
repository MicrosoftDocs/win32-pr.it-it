---
title: texreg2gb-PS
description: Interpreta i componenti di colore verde e blu del registro di origine come dati dell'indirizzo di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976690"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="a1ffe-103">texreg2gb-PS</span><span class="sxs-lookup"><span data-stu-id="a1ffe-103">texreg2gb - ps</span></span>

<span data-ttu-id="a1ffe-104">Interpreta i componenti di colore verde e blu del registro di origine come dati dell'indirizzo di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ffe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1ffe-105">Syntax</span></span>



| <span data-ttu-id="a1ffe-106">texreg2gb DST, src</span><span class="sxs-lookup"><span data-stu-id="a1ffe-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="a1ffe-107">dove</span><span class="sxs-lookup"><span data-stu-id="a1ffe-107">where</span></span>

-   <span data-ttu-id="a1ffe-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-108">dst is the destination register.</span></span>
-   <span data-ttu-id="a1ffe-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ffe-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1ffe-110">Remarks</span></span>



| <span data-ttu-id="a1ffe-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a1ffe-111">Pixel shader versions</span></span> | <span data-ttu-id="a1ffe-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="a1ffe-112">1\_1</span></span> | <span data-ttu-id="a1ffe-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="a1ffe-113">1\_2</span></span> | <span data-ttu-id="a1ffe-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a1ffe-114">1\_3</span></span> | <span data-ttu-id="a1ffe-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="a1ffe-115">1\_4</span></span> | <span data-ttu-id="a1ffe-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1ffe-116">2\_0</span></span> | <span data-ttu-id="a1ffe-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a1ffe-117">2\_x</span></span> | <span data-ttu-id="a1ffe-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1ffe-118">2\_sw</span></span> | <span data-ttu-id="a1ffe-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1ffe-119">3\_0</span></span> | <span data-ttu-id="a1ffe-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1ffe-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a1ffe-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="a1ffe-121">texreg2gb</span></span>             |      | <span data-ttu-id="a1ffe-122">x</span><span class="sxs-lookup"><span data-stu-id="a1ffe-122">x</span></span>    | <span data-ttu-id="a1ffe-123">x</span><span class="sxs-lookup"><span data-stu-id="a1ffe-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="a1ffe-124">Questa istruzione è utile per le operazioni di rimapping dello spazio colore.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="a1ffe-125">Di seguito è riportato un esempio della sequenza che segue l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="a1ffe-126">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="a1ffe-126">tex t(n)</span></span>  
<span data-ttu-id="a1ffe-127">texreg2gb t (m), t (n) dove m > n</span><span class="sxs-lookup"><span data-stu-id="a1ffe-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="a1ffe-128">La prima istruzione carica il colore della trama (RGBA)</span><span class="sxs-lookup"><span data-stu-id="a1ffe-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="a1ffe-129">in Register TN</span><span class="sxs-lookup"><span data-stu-id="a1ffe-129">// into register tn</span></span>  
<span data-ttu-id="a1ffe-130">Tex TN</span><span class="sxs-lookup"><span data-stu-id="a1ffe-130">tex tn</span></span>  
<span data-ttu-id="a1ffe-131">La seconda istruzione esegue il mapping del colore</span><span class="sxs-lookup"><span data-stu-id="a1ffe-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="a1ffe-132">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> usando t (n)<sub>GB</sub> come coordinate</span><span class="sxs-lookup"><span data-stu-id="a1ffe-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="a1ffe-133">\_non è possibile usare BX2 nel registro src per le istruzioni [texreg2ar-PS](texreg2ar---ps.md) o texreg2gb.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="a1ffe-134">Per questa istruzione, il registro di origine deve usare dati non firmati.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="a1ffe-135">L'utilizzo di dati firmati o misti nel registro di origine produrrà risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="a1ffe-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="a1ffe-136">Per ulteriori informazioni, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="a1ffe-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1ffe-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1ffe-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ffe-138">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="a1ffe-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
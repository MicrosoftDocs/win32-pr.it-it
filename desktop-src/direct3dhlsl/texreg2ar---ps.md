---
title: texreg2ar-PS
description: Interpreta i componenti di colore alfa e rosso del registro di origine come dati degli indirizzi di trama (u, v) per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473454"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="70b3a-104">texreg2ar-PS</span><span class="sxs-lookup"><span data-stu-id="70b3a-104">texreg2ar - ps</span></span>

<span data-ttu-id="70b3a-105">Interpreta i componenti di colore alfa e rosso del registro di origine come dati degli indirizzi di trama (u, v) per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="70b3a-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="70b3a-106">Il risultato viene archiviato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="70b3a-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b3a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70b3a-107">Syntax</span></span>



| <span data-ttu-id="70b3a-108">texreg2ar DST, src</span><span class="sxs-lookup"><span data-stu-id="70b3a-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="70b3a-109">dove</span><span class="sxs-lookup"><span data-stu-id="70b3a-109">where</span></span>

-   <span data-ttu-id="70b3a-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="70b3a-110">dst is the destination register.</span></span>
-   <span data-ttu-id="70b3a-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="70b3a-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="70b3a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="70b3a-112">Remarks</span></span>



| <span data-ttu-id="70b3a-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="70b3a-113">Pixel shader versions</span></span> | <span data-ttu-id="70b3a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="70b3a-114">1\_1</span></span> | <span data-ttu-id="70b3a-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="70b3a-115">1\_2</span></span> | <span data-ttu-id="70b3a-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="70b3a-116">1\_3</span></span> | <span data-ttu-id="70b3a-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="70b3a-117">1\_4</span></span> | <span data-ttu-id="70b3a-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70b3a-118">2\_0</span></span> | <span data-ttu-id="70b3a-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="70b3a-119">2\_x</span></span> | <span data-ttu-id="70b3a-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="70b3a-120">2\_sw</span></span> | <span data-ttu-id="70b3a-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70b3a-121">3\_0</span></span> | <span data-ttu-id="70b3a-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="70b3a-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="70b3a-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="70b3a-123">texreg2ar</span></span>             | <span data-ttu-id="70b3a-124">x</span><span class="sxs-lookup"><span data-stu-id="70b3a-124">x</span></span>    | <span data-ttu-id="70b3a-125">x</span><span class="sxs-lookup"><span data-stu-id="70b3a-125">x</span></span>    | <span data-ttu-id="70b3a-126">x</span><span class="sxs-lookup"><span data-stu-id="70b3a-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="70b3a-127">Questa istruzione è utile per le operazioni di rimapping dello spazio colore.</span><span class="sxs-lookup"><span data-stu-id="70b3a-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="70b3a-128">Ecco un esempio della sequenza seguita dall'istruzione:</span><span class="sxs-lookup"><span data-stu-id="70b3a-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="70b3a-129">Tex t (n)</span><span class="sxs-lookup"><span data-stu-id="70b3a-129">tex t(n)</span></span>  
<span data-ttu-id="70b3a-130">texreg2ar t (m), t (n) dove m > n</span><span class="sxs-lookup"><span data-stu-id="70b3a-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="70b3a-131">La prima istruzione carica il colore della trama (RGBA)</span><span class="sxs-lookup"><span data-stu-id="70b3a-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="70b3a-132">in Register TN</span><span class="sxs-lookup"><span data-stu-id="70b3a-132">// into register tn</span></span>  
<span data-ttu-id="70b3a-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="70b3a-133">tex tn</span></span>  
<span data-ttu-id="70b3a-134">La seconda istruzione esegue il mapping del colore</span><span class="sxs-lookup"><span data-stu-id="70b3a-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="70b3a-135">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> utilizzo di t (n)<sub>AR</sub> come coordinate</span><span class="sxs-lookup"><span data-stu-id="70b3a-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="70b3a-136">\_non è possibile usare BX2 nel registro src per le istruzioni texreg2ar o [texreg2gb-PS](texreg2gb---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="70b3a-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="70b3a-137">Per questa istruzione, il registro di origine deve usare dati non firmati.</span><span class="sxs-lookup"><span data-stu-id="70b3a-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="70b3a-138">L'utilizzo di dati firmati o misti nel registro di origine produrrà risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="70b3a-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="70b3a-139">Per ulteriori informazioni, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="70b3a-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70b3a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70b3a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70b3a-141">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="70b3a-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
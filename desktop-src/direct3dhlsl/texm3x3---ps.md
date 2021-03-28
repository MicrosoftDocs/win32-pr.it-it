---
title: texm3x3-PS
description: Esegue una moltiplicazione di matrice 3x3 quando viene usata insieme a due istruzioni texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976354"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="e1bd5-103">texm3x3-PS</span><span class="sxs-lookup"><span data-stu-id="e1bd5-103">texm3x3 - ps</span></span>

<span data-ttu-id="e1bd5-104">Esegue una moltiplicazione di matrice 3x3 quando viene usata insieme a due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="e1bd5-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1bd5-105">Syntax</span></span>



| <span data-ttu-id="e1bd5-106">texm3x3 DST, src</span><span class="sxs-lookup"><span data-stu-id="e1bd5-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="e1bd5-107">dove</span><span class="sxs-lookup"><span data-stu-id="e1bd5-107">where</span></span>

-   <span data-ttu-id="e1bd5-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e1bd5-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bd5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1bd5-110">Remarks</span></span>



| <span data-ttu-id="e1bd5-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e1bd5-111">Pixel shader versions</span></span> | <span data-ttu-id="e1bd5-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e1bd5-112">1\_1</span></span> | <span data-ttu-id="e1bd5-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e1bd5-113">1\_2</span></span> | <span data-ttu-id="e1bd5-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e1bd5-114">1\_3</span></span> | <span data-ttu-id="e1bd5-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e1bd5-115">1\_4</span></span> | <span data-ttu-id="e1bd5-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1bd5-116">2\_0</span></span> | <span data-ttu-id="e1bd5-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e1bd5-117">2\_x</span></span> | <span data-ttu-id="e1bd5-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e1bd5-118">2\_sw</span></span> | <span data-ttu-id="e1bd5-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1bd5-119">3\_0</span></span> | <span data-ttu-id="e1bd5-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e1bd5-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e1bd5-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="e1bd5-121">texm3x3</span></span>               |      | <span data-ttu-id="e1bd5-122">x</span><span class="sxs-lookup"><span data-stu-id="e1bd5-122">x</span></span>    | <span data-ttu-id="e1bd5-123">x</span><span class="sxs-lookup"><span data-stu-id="e1bd5-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="e1bd5-124">Questa istruzione è identica a quella dell'istruzione [texm3x3tex-PS](texm3x3tex---ps.md) , senza la ricerca della trama.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="e1bd5-125">Questa istruzione viene usata come finale di tre istruzioni che rappresentano un'operazione di moltiplicazione della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="e1bd5-126">La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="e1bd5-127">Qualsiasi trama assegnata a una qualsiasi delle tre fasi della trama viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="e1bd5-128">Questa istruzione deve essere utilizzata con due istruzioni texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="e1bd5-129">I registri di trama devono seguire la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="e1bd5-130">Di seguito sono riportati altri dettagli su come viene eseguita la moltiplicazione 3x3.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="e1bd5-131">La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup></span><span class="sxs-lookup"><span data-stu-id="e1bd5-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="e1bd5-132">u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e1bd5-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e1bd5-133">La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup></span><span class="sxs-lookup"><span data-stu-id="e1bd5-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="e1bd5-134">v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e1bd5-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e1bd5-135">L'istruzione texm3x3tex esegue la terza riga del moltiplicatore per<sup>trovare w.</sup></span><span class="sxs-lookup"><span data-stu-id="e1bd5-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="e1bd5-136">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e1bd5-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e1bd5-137">Posizionare il risultato della moltiplicazione della matrice nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1bd5-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="e1bd5-138">t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span><span class="sxs-lookup"><span data-stu-id="e1bd5-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1bd5-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1bd5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1bd5-140">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e1bd5-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





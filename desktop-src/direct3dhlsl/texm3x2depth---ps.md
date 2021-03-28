---
title: texm3x2depth-PS
description: Calcolare il valore di profondità da usare per il test di profondità per questo pixel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976386"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="84bd2-103">texm3x2depth-PS</span><span class="sxs-lookup"><span data-stu-id="84bd2-103">texm3x2depth - ps</span></span>

<span data-ttu-id="84bd2-104">Calcolare il valore di profondità da usare per il test di profondità per questo pixel.</span><span class="sxs-lookup"><span data-stu-id="84bd2-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="84bd2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84bd2-105">Syntax</span></span>



| <span data-ttu-id="84bd2-106">texm3x2depth DST, src</span><span class="sxs-lookup"><span data-stu-id="84bd2-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="84bd2-107">dove</span><span class="sxs-lookup"><span data-stu-id="84bd2-107">where</span></span>

-   <span data-ttu-id="84bd2-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="84bd2-108">dst is the destination register.</span></span>
-   <span data-ttu-id="84bd2-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="84bd2-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="84bd2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="84bd2-110">Remarks</span></span>



| <span data-ttu-id="84bd2-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="84bd2-111">Pixel shader versions</span></span> | <span data-ttu-id="84bd2-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="84bd2-112">1\_1</span></span> | <span data-ttu-id="84bd2-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="84bd2-113">1\_2</span></span> | <span data-ttu-id="84bd2-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="84bd2-114">1\_3</span></span> | <span data-ttu-id="84bd2-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="84bd2-115">1\_4</span></span> | <span data-ttu-id="84bd2-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84bd2-116">2\_0</span></span> | <span data-ttu-id="84bd2-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="84bd2-117">2\_x</span></span> | <span data-ttu-id="84bd2-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="84bd2-118">2\_sw</span></span> | <span data-ttu-id="84bd2-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84bd2-119">3\_0</span></span> | <span data-ttu-id="84bd2-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="84bd2-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="84bd2-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="84bd2-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="84bd2-122">x</span><span class="sxs-lookup"><span data-stu-id="84bd2-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="84bd2-123">Questa istruzione deve essere usata con l'istruzione [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="84bd2-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="84bd2-124">Quando si usano queste due istruzioni, i registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="84bd2-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="84bd2-125">Il calcolo della profondità viene eseguito dopo l'utilizzo di un'operazione del prodotto punto per trovare z e w.</span><span class="sxs-lookup"><span data-stu-id="84bd2-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="84bd2-126">Ecco altri dettagli sul modo in cui viene eseguito il calcolo della profondità.</span><span class="sxs-lookup"><span data-stu-id="84bd2-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="84bd2-127">L'istruzione texm3x2pad calcola z.</span><span class="sxs-lookup"><span data-stu-id="84bd2-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="84bd2-128">z = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="84bd2-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="84bd2-129">L'istruzione texm3x2depth calcola w.</span><span class="sxs-lookup"><span data-stu-id="84bd2-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="84bd2-130">w = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="84bd2-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="84bd2-131">Calcolare la profondità e archiviare il risultato in t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="84bd2-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="84bd2-132">La profondità calcolata è contrassegnata per essere usata nel test di profondità per il pixel, sostituendo il valore del test di profondità esistente per il pixel.</span><span class="sxs-lookup"><span data-stu-id="84bd2-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="84bd2-133">Assicurarsi di bloccare z/w nell'intervallo (0-1).</span><span class="sxs-lookup"><span data-stu-id="84bd2-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="84bd2-134">Se z/w è esterno a questo intervallo, il risultato archiviato nel buffer di profondità sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="84bd2-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="84bd2-135">Dopo l'esecuzione di texm3x2depth, il registro t (m + 1) non è più disponibile per l'uso nello shader.</span><span class="sxs-lookup"><span data-stu-id="84bd2-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="84bd2-136">Quando si esegue il campionamento multiplo, l'utilizzo di questa istruzione Elimina la maggior parte del vantaggio del buffer di profondità di risoluzione superiore.</span><span class="sxs-lookup"><span data-stu-id="84bd2-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="84bd2-137">Poiché il pixel shader viene eseguito una volta per pixel, viene usato il valore di profondità singola restituito da texm3x2depth o [texdepth-PS](texdepth---ps.md) per ogni test di confronto di profondità dei sottopixel.</span><span class="sxs-lookup"><span data-stu-id="84bd2-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84bd2-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84bd2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84bd2-139">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="84bd2-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





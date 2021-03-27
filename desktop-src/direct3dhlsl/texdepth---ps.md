---
title: texdepth-PS
description: Calcola i valori di profondità da usare nel test di confronto del buffer di profondità per questo pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857754"
---
# <a name="texdepth---ps"></a><span data-ttu-id="8c503-103">texdepth-PS</span><span class="sxs-lookup"><span data-stu-id="8c503-103">texdepth - ps</span></span>

<span data-ttu-id="8c503-104">Calcola i valori di profondità da usare nel test di confronto del buffer di profondità per questo pixel.</span><span class="sxs-lookup"><span data-stu-id="8c503-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c503-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c503-105">Syntax</span></span>



| <span data-ttu-id="8c503-106">texdepth DST</span><span class="sxs-lookup"><span data-stu-id="8c503-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="8c503-107">dove</span><span class="sxs-lookup"><span data-stu-id="8c503-107">where</span></span>

-   <span data-ttu-id="8c503-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8c503-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c503-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c503-109">Remarks</span></span>



| <span data-ttu-id="8c503-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="8c503-110">Pixel shader versions</span></span> | <span data-ttu-id="8c503-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="8c503-111">1\_1</span></span> | <span data-ttu-id="8c503-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="8c503-112">1\_2</span></span> | <span data-ttu-id="8c503-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8c503-113">1\_3</span></span> | <span data-ttu-id="8c503-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="8c503-114">1\_4</span></span> | <span data-ttu-id="8c503-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c503-115">2\_0</span></span> | <span data-ttu-id="8c503-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8c503-116">2\_x</span></span> | <span data-ttu-id="8c503-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8c503-117">2\_sw</span></span> | <span data-ttu-id="8c503-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c503-118">3\_0</span></span> | <span data-ttu-id="8c503-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8c503-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8c503-120">texdepth</span><span class="sxs-lookup"><span data-stu-id="8c503-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="8c503-121">x</span><span class="sxs-lookup"><span data-stu-id="8c503-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="8c503-122">Questa istruzione USA R5. r/R5. g nel test di confronto del buffer di profondità per questo pixel.</span><span class="sxs-lookup"><span data-stu-id="8c503-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="8c503-123">I dati nei canali blu e alfa vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="8c503-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="8c503-124">Se R5. g = 0, il risultato di R5. r/R5. g = 1,0.</span><span class="sxs-lookup"><span data-stu-id="8c503-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="8c503-125">Il registro temporaneo R5 è l'unico registro che questa istruzione può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8c503-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="8c503-126">Dopo l'esecuzione di questa istruzione, il registro temporaneo R5 non è disponibile per un uso aggiuntivo nello shader.</span><span class="sxs-lookup"><span data-stu-id="8c503-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="8c503-127">Quando si esegue il campionamento multiplo, l'utilizzo di questa istruzione Elimina la maggior parte del vantaggio del buffer di profondità di risoluzione superiore.</span><span class="sxs-lookup"><span data-stu-id="8c503-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="8c503-128">Poiché il pixel shader viene eseguito una volta per ogni pixel, viene usato il valore di profondità singola restituito da [texm3x2depth-PS](texm3x2depth---ps.md) o texdepth per ogni test di confronto di profondità dei sottopixel.</span><span class="sxs-lookup"><span data-stu-id="8c503-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="8c503-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c503-129">Examples</span></span>

<span data-ttu-id="8c503-130">Di seguito è riportato un esempio che usa texdepth.</span><span class="sxs-lookup"><span data-stu-id="8c503-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="8c503-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c503-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c503-132">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="8c503-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: texdp3-PS
description: Esegue un prodotto punto a tre componenti tra i dati nel numero di registro della trama e il set di coordinate di trama corrispondente al numero di registro di destinazione.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335452"
---
# <a name="texdp3---ps"></a><span data-ttu-id="af86c-103">texdp3-PS</span><span class="sxs-lookup"><span data-stu-id="af86c-103">texdp3 - ps</span></span>

<span data-ttu-id="af86c-104">Esegue un prodotto punto a tre componenti tra i dati nel numero di registro della trama e il set di coordinate di trama corrispondente al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af86c-104">Performs a three-component dot product between data in the texture register number and the texture coordinate set corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="af86c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af86c-105">Syntax</span></span>



| <span data-ttu-id="af86c-106">texdp3 DST, src</span><span class="sxs-lookup"><span data-stu-id="af86c-106">texdp3 dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="af86c-107">dove</span><span class="sxs-lookup"><span data-stu-id="af86c-107">where</span></span>

-   <span data-ttu-id="af86c-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af86c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="af86c-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="af86c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="af86c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="af86c-110">Remarks</span></span>



| <span data-ttu-id="af86c-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="af86c-111">Pixel shader versions</span></span> | <span data-ttu-id="af86c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="af86c-112">1\_1</span></span> | <span data-ttu-id="af86c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="af86c-113">1\_2</span></span> | <span data-ttu-id="af86c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="af86c-114">1\_3</span></span> | <span data-ttu-id="af86c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="af86c-115">1\_4</span></span> | <span data-ttu-id="af86c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af86c-116">2\_0</span></span> | <span data-ttu-id="af86c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="af86c-117">2\_x</span></span> | <span data-ttu-id="af86c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af86c-118">2\_sw</span></span> | <span data-ttu-id="af86c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af86c-119">3\_0</span></span> | <span data-ttu-id="af86c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af86c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="af86c-121">texdp3</span><span class="sxs-lookup"><span data-stu-id="af86c-121">texdp3</span></span>                |      | <span data-ttu-id="af86c-122">x</span><span class="sxs-lookup"><span data-stu-id="af86c-122">x</span></span>    | <span data-ttu-id="af86c-123">x</span><span class="sxs-lookup"><span data-stu-id="af86c-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="af86c-124">I registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="af86c-124">Texture registers must use the following sequence.</span></span>


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



<span data-ttu-id="af86c-125">Di seguito sono riportate informazioni più dettagliate sul modo in cui viene eseguito il prodotto punto.</span><span class="sxs-lookup"><span data-stu-id="af86c-125">Here is more detail about how the dot product is accomplished.</span></span>

<span data-ttu-id="af86c-126">L'istruzione texdp3 esegue un prodotto punto a tre componenti e lo replica in tutti e quattro i canali colori.</span><span class="sxs-lookup"><span data-stu-id="af86c-126">The texdp3 instruction performs a three-component dot product and replicates it to all four color channels.</span></span>

<span data-ttu-id="af86c-127">t (m)<sub>RGBA</sub> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="af86c-127">t(m)<sub>RGBA</sub> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

## <a name="related-topics"></a><span data-ttu-id="af86c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af86c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af86c-129">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="af86c-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





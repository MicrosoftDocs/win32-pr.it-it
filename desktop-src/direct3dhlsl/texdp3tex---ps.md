---
title: texdp3tex-PS
description: Esegue un prodotto punto a tre componenti e usa il risultato per eseguire una ricerca di trama 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992976"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="e4add-103">texdp3tex-PS</span><span class="sxs-lookup"><span data-stu-id="e4add-103">texdp3tex - ps</span></span>

<span data-ttu-id="e4add-104">Esegue un prodotto punto a tre componenti e usa il risultato per eseguire una ricerca di trama 1D.</span><span class="sxs-lookup"><span data-stu-id="e4add-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4add-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4add-105">Syntax</span></span>



| <span data-ttu-id="e4add-106">texdp3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="e4add-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="e4add-107">dove</span><span class="sxs-lookup"><span data-stu-id="e4add-107">where</span></span>

-   <span data-ttu-id="e4add-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e4add-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e4add-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="e4add-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4add-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4add-110">Remarks</span></span>



| <span data-ttu-id="e4add-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e4add-111">Pixel shader versions</span></span> | <span data-ttu-id="e4add-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e4add-112">1\_1</span></span> | <span data-ttu-id="e4add-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e4add-113">1\_2</span></span> | <span data-ttu-id="e4add-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e4add-114">1\_3</span></span> | <span data-ttu-id="e4add-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e4add-115">1\_4</span></span> | <span data-ttu-id="e4add-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4add-116">2\_0</span></span> | <span data-ttu-id="e4add-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e4add-117">2\_x</span></span> | <span data-ttu-id="e4add-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4add-118">2\_sw</span></span> | <span data-ttu-id="e4add-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4add-119">3\_0</span></span> | <span data-ttu-id="e4add-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4add-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e4add-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="e4add-121">texdp3tex</span></span>             |      | <span data-ttu-id="e4add-122">x</span><span class="sxs-lookup"><span data-stu-id="e4add-122">x</span></span>    | <span data-ttu-id="e4add-123">x</span><span class="sxs-lookup"><span data-stu-id="e4add-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="e4add-124">I registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="e4add-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="e4add-125">Di seguito sono illustrati in modo più dettagliato il modo in cui vengono eseguiti il prodotto e la ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="e4add-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="e4add-126">L'istruzione texdp3tex esegue un prodotto dot a tre componenti.</span><span class="sxs-lookup"><span data-stu-id="e4add-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="e4add-127">u ' = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e4add-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e4add-128">Il risultato viene usato per campionare la trama in fase di trama m eseguendo una ricerca 1D.</span><span class="sxs-lookup"><span data-stu-id="e4add-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="e4add-129">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> using (u ',0, 0) As coordinates</span><span class="sxs-lookup"><span data-stu-id="e4add-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4add-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4add-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4add-131">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e4add-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





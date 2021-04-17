---
title: NRM-PS
description: Normalizzare un vettore 3D. | NRM-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352861"
---
# <a name="nrm---ps"></a><span data-ttu-id="bf398-104">NRM-PS</span><span class="sxs-lookup"><span data-stu-id="bf398-104">nrm - ps</span></span>

<span data-ttu-id="bf398-105">Normalizzare un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="bf398-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf398-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf398-106">Syntax</span></span>



| <span data-ttu-id="bf398-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="bf398-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="bf398-108">dove</span><span class="sxs-lookup"><span data-stu-id="bf398-108">where</span></span>

-   <span data-ttu-id="bf398-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf398-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bf398-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="bf398-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf398-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf398-111">Remarks</span></span>



| <span data-ttu-id="bf398-112">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="bf398-112">Pixel shader versions</span></span> | <span data-ttu-id="bf398-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="bf398-113">1\_1</span></span> | <span data-ttu-id="bf398-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="bf398-114">1\_2</span></span> | <span data-ttu-id="bf398-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bf398-115">1\_3</span></span> | <span data-ttu-id="bf398-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="bf398-116">1\_4</span></span> | <span data-ttu-id="bf398-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf398-117">2\_0</span></span> | <span data-ttu-id="bf398-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bf398-118">2\_x</span></span> | <span data-ttu-id="bf398-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf398-119">2\_sw</span></span> | <span data-ttu-id="bf398-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf398-120">3\_0</span></span> | <span data-ttu-id="bf398-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf398-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bf398-122">NRM</span><span class="sxs-lookup"><span data-stu-id="bf398-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="bf398-123">x</span><span class="sxs-lookup"><span data-stu-id="bf398-123">x</span></span>    | <span data-ttu-id="bf398-124">x</span><span class="sxs-lookup"><span data-stu-id="bf398-124">x</span></span>    | <span data-ttu-id="bf398-125">x</span><span class="sxs-lookup"><span data-stu-id="bf398-125">x</span></span>     | <span data-ttu-id="bf398-126">x</span><span class="sxs-lookup"><span data-stu-id="bf398-126">x</span></span>    | <span data-ttu-id="bf398-127">x</span><span class="sxs-lookup"><span data-stu-id="bf398-127">x</span></span>     |



 

<span data-ttu-id="bf398-128">Questa istruzione funziona concettualmente, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="bf398-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="bf398-129">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="bf398-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="bf398-130">I registri dest e src non possono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="bf398-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="bf398-131">Il registro dest deve essere un registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="bf398-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="bf398-132">Questa istruzione esegue l'interpolazione lineare in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="bf398-132">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="bf398-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf398-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf398-134">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="bf398-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





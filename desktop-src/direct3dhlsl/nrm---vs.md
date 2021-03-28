---
title: NRM-vs
description: Normalizzare un vettore 3D. | NRM-vs
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234760"
---
# <a name="nrm---vs"></a><span data-ttu-id="be9d9-104">NRM-vs</span><span class="sxs-lookup"><span data-stu-id="be9d9-104">nrm - vs</span></span>

<span data-ttu-id="be9d9-105">Normalizzare un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="be9d9-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9d9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be9d9-106">Syntax</span></span>



| <span data-ttu-id="be9d9-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="be9d9-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="be9d9-108">dove</span><span class="sxs-lookup"><span data-stu-id="be9d9-108">where</span></span>

-   <span data-ttu-id="be9d9-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be9d9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="be9d9-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="be9d9-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9d9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="be9d9-111">Remarks</span></span>



| <span data-ttu-id="be9d9-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="be9d9-112">Vertex shader versions</span></span> | <span data-ttu-id="be9d9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="be9d9-113">1\_1</span></span> | <span data-ttu-id="be9d9-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="be9d9-114">2\_0</span></span> | <span data-ttu-id="be9d9-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="be9d9-115">2\_x</span></span> | <span data-ttu-id="be9d9-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="be9d9-116">2\_sw</span></span> | <span data-ttu-id="be9d9-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="be9d9-117">3\_0</span></span> | <span data-ttu-id="be9d9-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="be9d9-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="be9d9-119">NRM</span><span class="sxs-lookup"><span data-stu-id="be9d9-119">nrm</span></span>                    |      | <span data-ttu-id="be9d9-120">x</span><span class="sxs-lookup"><span data-stu-id="be9d9-120">x</span></span>    | <span data-ttu-id="be9d9-121">x</span><span class="sxs-lookup"><span data-stu-id="be9d9-121">x</span></span>    | <span data-ttu-id="be9d9-122">x</span><span class="sxs-lookup"><span data-stu-id="be9d9-122">x</span></span>     | <span data-ttu-id="be9d9-123">x</span><span class="sxs-lookup"><span data-stu-id="be9d9-123">x</span></span>    | <span data-ttu-id="be9d9-124">x</span><span class="sxs-lookup"><span data-stu-id="be9d9-124">x</span></span>     |



 

<span data-ttu-id="be9d9-125">Questa istruzione funziona concettualmente, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="be9d9-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="be9d9-126">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="be9d9-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="be9d9-127">I registri dest e src non possono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="be9d9-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="be9d9-128">Il registro dest deve essere un registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="be9d9-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="be9d9-129">Questa istruzione esegue l'interpolazione lineare in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="be9d9-129">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="be9d9-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be9d9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be9d9-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="be9d9-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





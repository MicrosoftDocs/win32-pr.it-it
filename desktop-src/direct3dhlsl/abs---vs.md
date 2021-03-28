---
title: ABS-vs
description: Calcola il valore assoluto. | ABS-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234632"
---
# <a name="abs---vs"></a><span data-ttu-id="5cec0-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="5cec0-104">abs - vs</span></span>

<span data-ttu-id="5cec0-105">Calcola il valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="5cec0-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cec0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cec0-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="5cec0-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="5cec0-107">abs dst, src</span></span> |



 

<span data-ttu-id="5cec0-108">dove</span><span class="sxs-lookup"><span data-stu-id="5cec0-108">where</span></span>

-   <span data-ttu-id="5cec0-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5cec0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5cec0-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="5cec0-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cec0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cec0-111">Remarks</span></span>



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5cec0-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="5cec0-112">Vertex shader versions</span></span> | <span data-ttu-id="5cec0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5cec0-113">1\_1</span></span> | <span data-ttu-id="5cec0-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5cec0-114">2\_0</span></span> | <span data-ttu-id="5cec0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5cec0-115">2\_x</span></span> | <span data-ttu-id="5cec0-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5cec0-116">2\_sw</span></span> | <span data-ttu-id="5cec0-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5cec0-117">3\_0</span></span> | <span data-ttu-id="5cec0-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5cec0-118">3\_sw</span></span> |
| <span data-ttu-id="5cec0-119">abs</span><span class="sxs-lookup"><span data-stu-id="5cec0-119">abs</span></span>                    |      | <span data-ttu-id="5cec0-120">x</span><span class="sxs-lookup"><span data-stu-id="5cec0-120">x</span></span>    | <span data-ttu-id="5cec0-121">x</span><span class="sxs-lookup"><span data-stu-id="5cec0-121">x</span></span>    | <span data-ttu-id="5cec0-122">x</span><span class="sxs-lookup"><span data-stu-id="5cec0-122">x</span></span>     | <span data-ttu-id="5cec0-123">x</span><span class="sxs-lookup"><span data-stu-id="5cec0-123">x</span></span>    | <span data-ttu-id="5cec0-124">x</span><span class="sxs-lookup"><span data-stu-id="5cec0-124">x</span></span>     |



 

<span data-ttu-id="5cec0-125">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5cec0-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="5cec0-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cec0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cec0-127">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="5cec0-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





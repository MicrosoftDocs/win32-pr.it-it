---
title: DP3-vs
description: Calcola il prodotto del punto a tre componenti dei registri di origine. | DP3-vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81580401f25ddcf7ce1c1d53475d0c3beba74a89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234631"
---
# <a name="dp3---vs"></a><span data-ttu-id="a5343-104">DP3-vs</span><span class="sxs-lookup"><span data-stu-id="a5343-104">dp3 - vs</span></span>

<span data-ttu-id="a5343-105">Calcola il prodotto del punto a tre componenti dei registri di origine.</span><span class="sxs-lookup"><span data-stu-id="a5343-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5343-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5343-106">Syntax</span></span>



| <span data-ttu-id="a5343-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a5343-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a5343-108">dove</span><span class="sxs-lookup"><span data-stu-id="a5343-108">where</span></span>

-   <span data-ttu-id="a5343-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a5343-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a5343-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="a5343-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a5343-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="a5343-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5343-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5343-112">Remarks</span></span>



| <span data-ttu-id="a5343-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="a5343-113">Vertex shader versions</span></span> | <span data-ttu-id="a5343-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a5343-114">1\_1</span></span> | <span data-ttu-id="a5343-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5343-115">2\_0</span></span> | <span data-ttu-id="a5343-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a5343-116">2\_x</span></span> | <span data-ttu-id="a5343-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a5343-117">2\_sw</span></span> | <span data-ttu-id="a5343-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5343-118">3\_0</span></span> | <span data-ttu-id="a5343-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a5343-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a5343-120">dp3</span><span class="sxs-lookup"><span data-stu-id="a5343-120">dp3</span></span>                    | <span data-ttu-id="a5343-121">x</span><span class="sxs-lookup"><span data-stu-id="a5343-121">x</span></span>    | <span data-ttu-id="a5343-122">x</span><span class="sxs-lookup"><span data-stu-id="a5343-122">x</span></span>    | <span data-ttu-id="a5343-123">x</span><span class="sxs-lookup"><span data-stu-id="a5343-123">x</span></span>    | <span data-ttu-id="a5343-124">x</span><span class="sxs-lookup"><span data-stu-id="a5343-124">x</span></span>     | <span data-ttu-id="a5343-125">x</span><span class="sxs-lookup"><span data-stu-id="a5343-125">x</span></span>    | <span data-ttu-id="a5343-126">x</span><span class="sxs-lookup"><span data-stu-id="a5343-126">x</span></span>     |



 

<span data-ttu-id="a5343-127">Il frammento di codice seguente mostra le operazioni eseguite:</span><span class="sxs-lookup"><span data-stu-id="a5343-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="a5343-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5343-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5343-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="a5343-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





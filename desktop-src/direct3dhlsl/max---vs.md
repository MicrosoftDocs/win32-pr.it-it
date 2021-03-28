---
title: Max-vs
description: Calcola il numero massimo di origini. | Max-vs
ms.assetid: 93fb8fb2-c722-43e5-bfe4-a2e9d3cd2049
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 923da795210fe2be62a6dd84a53f0127fef21077
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981746"
---
# <a name="max---vs"></a><span data-ttu-id="5e1d8-104">Max-vs</span><span class="sxs-lookup"><span data-stu-id="5e1d8-104">max - vs</span></span>

<span data-ttu-id="5e1d8-105">Calcola il numero massimo di origini.</span><span class="sxs-lookup"><span data-stu-id="5e1d8-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e1d8-106">Syntax</span></span>



| <span data-ttu-id="5e1d8-107">Max DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="5e1d8-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5e1d8-108">dove</span><span class="sxs-lookup"><span data-stu-id="5e1d8-108">where</span></span>

-   <span data-ttu-id="5e1d8-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5e1d8-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5e1d8-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="5e1d8-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5e1d8-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="5e1d8-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e1d8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e1d8-112">Remarks</span></span>



| <span data-ttu-id="5e1d8-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="5e1d8-113">Vertex shader versions</span></span> | <span data-ttu-id="5e1d8-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5e1d8-114">1\_1</span></span> | <span data-ttu-id="5e1d8-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e1d8-115">2\_0</span></span> | <span data-ttu-id="5e1d8-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-116">2\_x</span></span> | <span data-ttu-id="5e1d8-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5e1d8-117">2\_sw</span></span> | <span data-ttu-id="5e1d8-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5e1d8-118">3\_0</span></span> | <span data-ttu-id="5e1d8-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5e1d8-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5e1d8-120">max</span><span class="sxs-lookup"><span data-stu-id="5e1d8-120">max</span></span>                    | <span data-ttu-id="5e1d8-121">x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-121">x</span></span>    | <span data-ttu-id="5e1d8-122">x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-122">x</span></span>    | <span data-ttu-id="5e1d8-123">x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-123">x</span></span>    | <span data-ttu-id="5e1d8-124">x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-124">x</span></span>     | <span data-ttu-id="5e1d8-125">x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-125">x</span></span>    | <span data-ttu-id="5e1d8-126">x</span><span class="sxs-lookup"><span data-stu-id="5e1d8-126">x</span></span>     |



 

<span data-ttu-id="5e1d8-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="5e1d8-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="5e1d8-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e1d8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e1d8-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="5e1d8-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





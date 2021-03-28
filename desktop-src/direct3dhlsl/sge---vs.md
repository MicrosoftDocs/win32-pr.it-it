---
title: SGE-vs
description: Calcola il segno se la prima origine è maggiore o uguale alla seconda origine.
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7bad8816b87a32c5f10c73df27beb3cc2aef7716
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398248"
---
# <a name="sge---vs"></a><span data-ttu-id="30cc9-103">SGE-vs</span><span class="sxs-lookup"><span data-stu-id="30cc9-103">sge - vs</span></span>

<span data-ttu-id="30cc9-104">Calcola il segno se la prima origine è maggiore o uguale alla seconda origine.</span><span class="sxs-lookup"><span data-stu-id="30cc9-104">Computes the sign if the first source is greater than or equal to the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cc9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30cc9-105">Syntax</span></span>



| <span data-ttu-id="30cc9-106">SGE DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="30cc9-106">sge dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="30cc9-107">dove</span><span class="sxs-lookup"><span data-stu-id="30cc9-107">where</span></span>

-   <span data-ttu-id="30cc9-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="30cc9-108">dst is the destination register.</span></span>
-   <span data-ttu-id="30cc9-109">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="30cc9-109">src0 is a source register.</span></span>
-   <span data-ttu-id="30cc9-110">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="30cc9-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="30cc9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="30cc9-111">Remarks</span></span>



| <span data-ttu-id="30cc9-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="30cc9-112">Vertex shader versions</span></span> | <span data-ttu-id="30cc9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="30cc9-113">1\_1</span></span> | <span data-ttu-id="30cc9-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30cc9-114">2\_0</span></span> | <span data-ttu-id="30cc9-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="30cc9-115">2\_x</span></span> | <span data-ttu-id="30cc9-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30cc9-116">2\_sw</span></span> | <span data-ttu-id="30cc9-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30cc9-117">3\_0</span></span> | <span data-ttu-id="30cc9-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30cc9-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="30cc9-119">SGE</span><span class="sxs-lookup"><span data-stu-id="30cc9-119">sge</span></span>                    | <span data-ttu-id="30cc9-120">x</span><span class="sxs-lookup"><span data-stu-id="30cc9-120">x</span></span>    | <span data-ttu-id="30cc9-121">x</span><span class="sxs-lookup"><span data-stu-id="30cc9-121">x</span></span>    | <span data-ttu-id="30cc9-122">x</span><span class="sxs-lookup"><span data-stu-id="30cc9-122">x</span></span>    | <span data-ttu-id="30cc9-123">x</span><span class="sxs-lookup"><span data-stu-id="30cc9-123">x</span></span>     | <span data-ttu-id="30cc9-124">x</span><span class="sxs-lookup"><span data-stu-id="30cc9-124">x</span></span>    | <span data-ttu-id="30cc9-125">x</span><span class="sxs-lookup"><span data-stu-id="30cc9-125">x</span></span>     |



 

<span data-ttu-id="30cc9-126">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="30cc9-126">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="30cc9-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30cc9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30cc9-128">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="30cc9-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





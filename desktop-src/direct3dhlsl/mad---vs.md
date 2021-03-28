---
title: MAD-vs
description: Moltiplica e aggiunge origini.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01e96bb63395fe9e5dd27a17fbb5c0ddd9bf3c17
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335519"
---
# <a name="mad---vs"></a><span data-ttu-id="36db8-103">MAD-vs</span><span class="sxs-lookup"><span data-stu-id="36db8-103">mad - vs</span></span>

<span data-ttu-id="36db8-104">Moltiplica e aggiunge origini.</span><span class="sxs-lookup"><span data-stu-id="36db8-104">Multiplies and adds sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="36db8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36db8-105">Syntax</span></span>



| <span data-ttu-id="36db8-106">MAD DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="36db8-106">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="36db8-107">dove</span><span class="sxs-lookup"><span data-stu-id="36db8-107">where</span></span>

-   <span data-ttu-id="36db8-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="36db8-108">dst is the destination register.</span></span>
-   <span data-ttu-id="36db8-109">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="36db8-109">src0 is a source register.</span></span>
-   <span data-ttu-id="36db8-110">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="36db8-110">src1 is a source register.</span></span>
-   <span data-ttu-id="36db8-111">src2 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="36db8-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="36db8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="36db8-112">Remarks</span></span>



| <span data-ttu-id="36db8-113">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="36db8-113">Vertex shader versions</span></span> | <span data-ttu-id="36db8-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="36db8-114">1\_1</span></span> | <span data-ttu-id="36db8-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="36db8-115">2\_0</span></span> | <span data-ttu-id="36db8-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="36db8-116">2\_x</span></span> | <span data-ttu-id="36db8-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="36db8-117">2\_sw</span></span> | <span data-ttu-id="36db8-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="36db8-118">3\_0</span></span> | <span data-ttu-id="36db8-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="36db8-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="36db8-120">pazzo</span><span class="sxs-lookup"><span data-stu-id="36db8-120">mad</span></span>                    | <span data-ttu-id="36db8-121">x</span><span class="sxs-lookup"><span data-stu-id="36db8-121">x</span></span>    | <span data-ttu-id="36db8-122">x</span><span class="sxs-lookup"><span data-stu-id="36db8-122">x</span></span>    | <span data-ttu-id="36db8-123">x</span><span class="sxs-lookup"><span data-stu-id="36db8-123">x</span></span>    | <span data-ttu-id="36db8-124">x</span><span class="sxs-lookup"><span data-stu-id="36db8-124">x</span></span>     | <span data-ttu-id="36db8-125">x</span><span class="sxs-lookup"><span data-stu-id="36db8-125">x</span></span>    | <span data-ttu-id="36db8-126">x</span><span class="sxs-lookup"><span data-stu-id="36db8-126">x</span></span>     |



 

<span data-ttu-id="36db8-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="36db8-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="36db8-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36db8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36db8-129">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="36db8-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





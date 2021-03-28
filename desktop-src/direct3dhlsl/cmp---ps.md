---
title: CMP-PS
description: Scegliere src1 se src0 0. In caso contrario, scegliere src2. Il confronto viene eseguito per canale.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046081"
---
# <a name="cmp---ps"></a><span data-ttu-id="6ea58-105">CMP-PS</span><span class="sxs-lookup"><span data-stu-id="6ea58-105">cmp - ps</span></span>

<span data-ttu-id="6ea58-106">Scegliere src1 se src0 >= 0.</span><span class="sxs-lookup"><span data-stu-id="6ea58-106">Choose src1 if src0 >= 0.</span></span> <span data-ttu-id="6ea58-107">In caso contrario, scegliere src2.</span><span class="sxs-lookup"><span data-stu-id="6ea58-107">Otherwise, choose src2.</span></span> <span data-ttu-id="6ea58-108">Il confronto viene eseguito per canale.</span><span class="sxs-lookup"><span data-stu-id="6ea58-108">The comparison is done per channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea58-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ea58-109">Syntax</span></span>



| <span data-ttu-id="6ea58-110">CMP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="6ea58-110">cmp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="6ea58-111">dove</span><span class="sxs-lookup"><span data-stu-id="6ea58-111">where</span></span>

-   <span data-ttu-id="6ea58-112">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6ea58-112">dst is the destination register.</span></span>
-   <span data-ttu-id="6ea58-113">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6ea58-113">src0 is a source register.</span></span>
-   <span data-ttu-id="6ea58-114">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6ea58-114">src1 is a source register.</span></span>
-   <span data-ttu-id="6ea58-115">src2 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6ea58-115">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea58-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ea58-116">Remarks</span></span>



| <span data-ttu-id="6ea58-117">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6ea58-117">Pixel shader versions</span></span> | <span data-ttu-id="6ea58-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ea58-118">1\_1</span></span> | <span data-ttu-id="6ea58-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="6ea58-119">1\_2</span></span> | <span data-ttu-id="6ea58-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6ea58-120">1\_3</span></span> | <span data-ttu-id="6ea58-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ea58-121">1\_4</span></span> | <span data-ttu-id="6ea58-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ea58-122">2\_0</span></span> | <span data-ttu-id="6ea58-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ea58-123">2\_x</span></span> | <span data-ttu-id="6ea58-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ea58-124">2\_sw</span></span> | <span data-ttu-id="6ea58-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ea58-125">3\_0</span></span> | <span data-ttu-id="6ea58-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ea58-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6ea58-127">CMP</span><span class="sxs-lookup"><span data-stu-id="6ea58-127">cmp</span></span>                   |      | <span data-ttu-id="6ea58-128">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-128">x</span></span>    | <span data-ttu-id="6ea58-129">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-129">x</span></span>    | <span data-ttu-id="6ea58-130">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-130">x</span></span>    | <span data-ttu-id="6ea58-131">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-131">x</span></span>    | <span data-ttu-id="6ea58-132">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-132">x</span></span>    | <span data-ttu-id="6ea58-133">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-133">x</span></span>     | <span data-ttu-id="6ea58-134">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-134">x</span></span>    | <span data-ttu-id="6ea58-135">x</span><span class="sxs-lookup"><span data-stu-id="6ea58-135">x</span></span>     |



 

<span data-ttu-id="6ea58-136">Esistono alcune limitazioni aggiuntive per le versioni 1 \_ 2 e 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="6ea58-136">There are a few additional limitations for versions 1\_2 and 1\_3:</span></span>

-   <span data-ttu-id="6ea58-137">Ogni shader può utilizzare fino a un massimo di tre istruzioni CMP.</span><span class="sxs-lookup"><span data-stu-id="6ea58-137">Each shader can use up to a maximum of three cmp instructions.</span></span>
-   <span data-ttu-id="6ea58-138">Il registro di destinazione non può essere uguale a uno dei registri di origine.</span><span class="sxs-lookup"><span data-stu-id="6ea58-138">The destination register cannot be the same as any of the source registers.</span></span>

<span data-ttu-id="6ea58-139">Questo esempio esegue un confronto a quattro canali.</span><span class="sxs-lookup"><span data-stu-id="6ea58-139">This example does a four-channel comparison.</span></span>


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a><span data-ttu-id="6ea58-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ea58-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ea58-141">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6ea58-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





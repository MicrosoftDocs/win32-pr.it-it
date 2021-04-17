---
title: SGN-vs
description: Calcola il segno dell'input.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398247"
---
# <a name="sgn---vs"></a><span data-ttu-id="4fadf-103">SGN-vs</span><span class="sxs-lookup"><span data-stu-id="4fadf-103">sgn - vs</span></span>

<span data-ttu-id="4fadf-104">Calcola il segno dell'input.</span><span class="sxs-lookup"><span data-stu-id="4fadf-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fadf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fadf-105">Syntax</span></span>



| <span data-ttu-id="4fadf-106">SGN DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="4fadf-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="4fadf-107">dove</span><span class="sxs-lookup"><span data-stu-id="4fadf-107">where</span></span>

-   <span data-ttu-id="4fadf-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4fadf-108">dst is the destination register.</span></span>
-   <span data-ttu-id="4fadf-109">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="4fadf-109">src0 is a source register.</span></span>
-   <span data-ttu-id="4fadf-110">src1 è un registro temporaneo che include risultati intermedi.</span><span class="sxs-lookup"><span data-stu-id="4fadf-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="4fadf-111">In seguito all'esecuzione, il contenuto non è definito.</span><span class="sxs-lookup"><span data-stu-id="4fadf-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="4fadf-112">src2 è un registro temporaneo che include risultati intermedi.</span><span class="sxs-lookup"><span data-stu-id="4fadf-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="4fadf-113">In seguito all'esecuzione, il contenuto non è definito.</span><span class="sxs-lookup"><span data-stu-id="4fadf-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fadf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fadf-114">Remarks</span></span>



| <span data-ttu-id="4fadf-115">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4fadf-115">Vertex shader versions</span></span> | <span data-ttu-id="4fadf-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="4fadf-116">1\_1</span></span> | <span data-ttu-id="4fadf-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fadf-117">2\_0</span></span> | <span data-ttu-id="4fadf-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4fadf-118">2\_x</span></span> | <span data-ttu-id="4fadf-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4fadf-119">2\_sw</span></span> | <span data-ttu-id="4fadf-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fadf-120">3\_0</span></span> | <span data-ttu-id="4fadf-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4fadf-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4fadf-122">SGN</span><span class="sxs-lookup"><span data-stu-id="4fadf-122">sgn</span></span>                    |      | <span data-ttu-id="4fadf-123">x</span><span class="sxs-lookup"><span data-stu-id="4fadf-123">x</span></span>    | <span data-ttu-id="4fadf-124">x</span><span class="sxs-lookup"><span data-stu-id="4fadf-124">x</span></span>    | <span data-ttu-id="4fadf-125">x</span><span class="sxs-lookup"><span data-stu-id="4fadf-125">x</span></span>     | <span data-ttu-id="4fadf-126">x</span><span class="sxs-lookup"><span data-stu-id="4fadf-126">x</span></span>    | <span data-ttu-id="4fadf-127">x</span><span class="sxs-lookup"><span data-stu-id="4fadf-127">x</span></span>     |



 

<span data-ttu-id="4fadf-128">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4fadf-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="4fadf-129">src1 e src2 devono essere [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)diversi.</span><span class="sxs-lookup"><span data-stu-id="4fadf-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fadf-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fadf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fadf-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4fadf-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





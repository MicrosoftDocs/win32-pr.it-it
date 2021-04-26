---
title: abs - vs
description: Calcola il valore assoluto. | abs - vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994748"
---
# <a name="abs---vs"></a><span data-ttu-id="192a0-104">abs - vs</span><span class="sxs-lookup"><span data-stu-id="192a0-104">abs - vs</span></span>

<span data-ttu-id="192a0-105">Calcola il valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="192a0-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="192a0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="192a0-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="192a0-107">abs dst, src</span><span class="sxs-lookup"><span data-stu-id="192a0-107">abs dst, src</span></span> |



 

<span data-ttu-id="192a0-108">dove</span><span class="sxs-lookup"><span data-stu-id="192a0-108">where</span></span>

-   <span data-ttu-id="192a0-109">dst è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="192a0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="192a0-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="192a0-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="192a0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="192a0-111">Remarks</span></span>



| <span data-ttu-id="192a0-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="192a0-112">Vertex shader versions</span></span> | <span data-ttu-id="192a0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="192a0-113">1\_1</span></span> | <span data-ttu-id="192a0-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="192a0-114">2\_0</span></span> | <span data-ttu-id="192a0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="192a0-115">2\_x</span></span> | <span data-ttu-id="192a0-116">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="192a0-116">2\_sw</span></span> | <span data-ttu-id="192a0-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="192a0-117">3\_0</span></span> | <span data-ttu-id="192a0-118">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="192a0-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="192a0-119">abs</span><span class="sxs-lookup"><span data-stu-id="192a0-119">abs</span></span>                    |      | <span data-ttu-id="192a0-120">x</span><span class="sxs-lookup"><span data-stu-id="192a0-120">x</span></span>    | <span data-ttu-id="192a0-121">x</span><span class="sxs-lookup"><span data-stu-id="192a0-121">x</span></span>    | <span data-ttu-id="192a0-122">x</span><span class="sxs-lookup"><span data-stu-id="192a0-122">x</span></span>     | <span data-ttu-id="192a0-123">x</span><span class="sxs-lookup"><span data-stu-id="192a0-123">x</span></span>    | <span data-ttu-id="192a0-124">x</span><span class="sxs-lookup"><span data-stu-id="192a0-124">x</span></span>     |



 

<span data-ttu-id="192a0-125">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="192a0-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="192a0-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="192a0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="192a0-127">Istruzioni per vertex shader</span><span class="sxs-lookup"><span data-stu-id="192a0-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





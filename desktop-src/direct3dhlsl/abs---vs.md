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
ms.openlocfilehash: 612ed14fb538a419a0e7f0b1cf07904d654bb010
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343316"
---
# <a name="abs---vs"></a><span data-ttu-id="88ea6-104">abs - vs</span><span class="sxs-lookup"><span data-stu-id="88ea6-104">abs - vs</span></span>

<span data-ttu-id="88ea6-105">Calcola il valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="88ea6-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ea6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88ea6-106">Syntax</span></span>

<span data-ttu-id="88ea6-107">**abs dst, src**</span><span class="sxs-lookup"><span data-stu-id="88ea6-107">**abs dst, src**</span></span>

<span data-ttu-id="88ea6-108">dove</span><span class="sxs-lookup"><span data-stu-id="88ea6-108">where</span></span>

- <span data-ttu-id="88ea6-109">dst è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="88ea6-109">dst is the destination register.</span></span>
- <span data-ttu-id="88ea6-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="88ea6-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ea6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="88ea6-111">Remarks</span></span>



| <span data-ttu-id="88ea6-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="88ea6-112">Vertex shader versions</span></span> | <span data-ttu-id="88ea6-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="88ea6-113">1\_1</span></span> | <span data-ttu-id="88ea6-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="88ea6-114">2\_0</span></span> | <span data-ttu-id="88ea6-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="88ea6-115">2\_x</span></span> | <span data-ttu-id="88ea6-116">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="88ea6-116">2\_sw</span></span> | <span data-ttu-id="88ea6-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="88ea6-117">3\_0</span></span> | <span data-ttu-id="88ea6-118">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="88ea6-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="88ea6-119">abs</span><span class="sxs-lookup"><span data-stu-id="88ea6-119">abs</span></span>                    |      | <span data-ttu-id="88ea6-120">x</span><span class="sxs-lookup"><span data-stu-id="88ea6-120">x</span></span>    | <span data-ttu-id="88ea6-121">x</span><span class="sxs-lookup"><span data-stu-id="88ea6-121">x</span></span>    | <span data-ttu-id="88ea6-122">x</span><span class="sxs-lookup"><span data-stu-id="88ea6-122">x</span></span>     | <span data-ttu-id="88ea6-123">x</span><span class="sxs-lookup"><span data-stu-id="88ea6-123">x</span></span>    | <span data-ttu-id="88ea6-124">x</span><span class="sxs-lookup"><span data-stu-id="88ea6-124">x</span></span>     |



 

<span data-ttu-id="88ea6-125">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="88ea6-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="88ea6-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88ea6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ea6-127">Istruzioni per vertex shader</span><span class="sxs-lookup"><span data-stu-id="88ea6-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





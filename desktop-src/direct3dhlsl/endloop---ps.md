---
title: endloop-PS
description: Fine di un ciclo-PS... blocco ENDLOOP.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956067"
---
# <a name="endloop---ps"></a><span data-ttu-id="76788-103">endloop-PS</span><span class="sxs-lookup"><span data-stu-id="76788-103">endloop - ps</span></span>

<span data-ttu-id="76788-104">Fine di un [ciclo-PS](loop---ps.md)... blocco ENDLOOP.</span><span class="sxs-lookup"><span data-stu-id="76788-104">End of a [loop - ps](loop---ps.md)...endloop block.</span></span>

## <a name="remarks"></a><span data-ttu-id="76788-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="76788-105">Remarks</span></span>



| <span data-ttu-id="76788-106">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="76788-106">Pixel shader versions</span></span> | <span data-ttu-id="76788-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="76788-107">1\_1</span></span> | <span data-ttu-id="76788-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="76788-108">1\_2</span></span> | <span data-ttu-id="76788-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="76788-109">1\_3</span></span> | <span data-ttu-id="76788-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="76788-110">1\_4</span></span> | <span data-ttu-id="76788-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76788-111">2\_0</span></span> | <span data-ttu-id="76788-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="76788-112">2\_x</span></span> | <span data-ttu-id="76788-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76788-113">2\_sw</span></span> | <span data-ttu-id="76788-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76788-114">3\_0</span></span> | <span data-ttu-id="76788-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76788-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="76788-116">endloop</span><span class="sxs-lookup"><span data-stu-id="76788-116">endloop</span></span>               |      |      |      |      |      |      |       | <span data-ttu-id="76788-117">x</span><span class="sxs-lookup"><span data-stu-id="76788-117">x</span></span>    | <span data-ttu-id="76788-118">x</span><span class="sxs-lookup"><span data-stu-id="76788-118">x</span></span>     |



 

<span data-ttu-id="76788-119">endloop deve seguire l'ultima istruzione di un blocco [loop-PS](loop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="76788-119">endloop must follow the last instruction of a [loop - ps](loop---ps.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="76788-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="76788-120">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="76788-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76788-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76788-122">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="76788-122">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





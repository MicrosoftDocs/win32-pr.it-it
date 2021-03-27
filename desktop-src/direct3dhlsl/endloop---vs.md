---
title: endloop-vs
description: Fine di un ciclo... blocco ENDLOOP.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398190"
---
# <a name="endloop---vs"></a><span data-ttu-id="bbb8a-103">endloop-vs</span><span class="sxs-lookup"><span data-stu-id="bbb8a-103">endloop - vs</span></span>

<span data-ttu-id="bbb8a-104">Fine di un [ciclo](loop---vs.md)... blocco ENDLOOP.</span><span class="sxs-lookup"><span data-stu-id="bbb8a-104">End of a [loop](loop---vs.md)...endloop block.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbb8a-105">Syntax</span></span>



| <span data-ttu-id="bbb8a-106">endloop</span><span class="sxs-lookup"><span data-stu-id="bbb8a-106">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="bbb8a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbb8a-107">Remarks</span></span>



| <span data-ttu-id="bbb8a-108">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="bbb8a-108">Vertex shader versions</span></span> | <span data-ttu-id="bbb8a-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="bbb8a-109">1\_1</span></span> | <span data-ttu-id="bbb8a-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbb8a-110">2\_0</span></span> | <span data-ttu-id="bbb8a-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bbb8a-111">2\_x</span></span> | <span data-ttu-id="bbb8a-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bbb8a-112">2\_sw</span></span> | <span data-ttu-id="bbb8a-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbb8a-113">3\_0</span></span> | <span data-ttu-id="bbb8a-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bbb8a-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bbb8a-115">endloop</span><span class="sxs-lookup"><span data-stu-id="bbb8a-115">endloop</span></span>                |      | <span data-ttu-id="bbb8a-116">x</span><span class="sxs-lookup"><span data-stu-id="bbb8a-116">x</span></span>    | <span data-ttu-id="bbb8a-117">x</span><span class="sxs-lookup"><span data-stu-id="bbb8a-117">x</span></span>    | <span data-ttu-id="bbb8a-118">x</span><span class="sxs-lookup"><span data-stu-id="bbb8a-118">x</span></span>     | <span data-ttu-id="bbb8a-119">x</span><span class="sxs-lookup"><span data-stu-id="bbb8a-119">x</span></span>    | <span data-ttu-id="bbb8a-120">x</span><span class="sxs-lookup"><span data-stu-id="bbb8a-120">x</span></span>     |



 

<span data-ttu-id="bbb8a-121">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="bbb8a-121">This instruction works as shown here.</span></span>


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



<span data-ttu-id="bbb8a-122">endloop deve seguire l'ultima istruzione di un blocco [loop-vs](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb8a-122">endloop must follow the last instruction of a [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="bbb8a-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="bbb8a-123">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="bbb8a-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbb8a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbb8a-125">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="bbb8a-125">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





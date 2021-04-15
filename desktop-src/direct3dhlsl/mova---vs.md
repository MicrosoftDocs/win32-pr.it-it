---
title: mova-vs
description: Spostare i dati da un registro a virgola mobile nel registro degli indirizzi, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976474"
---
# <a name="mova---vs"></a><span data-ttu-id="70374-103">mova-vs</span><span class="sxs-lookup"><span data-stu-id="70374-103">mova - vs</span></span>

<span data-ttu-id="70374-104">Spostare i dati da un registro a virgola mobile nel [Registro degli indirizzi](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="70374-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="70374-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70374-105">Syntax</span></span>



| <span data-ttu-id="70374-106">mova DST, src</span><span class="sxs-lookup"><span data-stu-id="70374-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="70374-107">dove</span><span class="sxs-lookup"><span data-stu-id="70374-107">where</span></span>

-   <span data-ttu-id="70374-108">DST deve essere il [Registro degli indirizzi](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="70374-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="70374-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="70374-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="70374-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="70374-110">Remarks</span></span>



| <span data-ttu-id="70374-111">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="70374-111">Vertex shader versions</span></span> | <span data-ttu-id="70374-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="70374-112">1\_1</span></span> | <span data-ttu-id="70374-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70374-113">2\_0</span></span> | <span data-ttu-id="70374-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="70374-114">2\_x</span></span> | <span data-ttu-id="70374-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="70374-115">2\_sw</span></span> | <span data-ttu-id="70374-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70374-116">3\_0</span></span> | <span data-ttu-id="70374-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="70374-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="70374-118">mova</span><span class="sxs-lookup"><span data-stu-id="70374-118">mova</span></span>                   |      | <span data-ttu-id="70374-119">x</span><span class="sxs-lookup"><span data-stu-id="70374-119">x</span></span>    | <span data-ttu-id="70374-120">x</span><span class="sxs-lookup"><span data-stu-id="70374-120">x</span></span>    | <span data-ttu-id="70374-121">x</span><span class="sxs-lookup"><span data-stu-id="70374-121">x</span></span>     | <span data-ttu-id="70374-122">x</span><span class="sxs-lookup"><span data-stu-id="70374-122">x</span></span>    | <span data-ttu-id="70374-123">x</span><span class="sxs-lookup"><span data-stu-id="70374-123">x</span></span>     |



 

<span data-ttu-id="70374-124">Sposta i dati a virgola mobile in un registro di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="70374-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="70374-125">I valori vengono convertiti da virgola mobile usando l'arrotondamento al più vicino.</span><span class="sxs-lookup"><span data-stu-id="70374-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="70374-126">Il registro indirizzi è l'unico registro di destinazione consentito.</span><span class="sxs-lookup"><span data-stu-id="70374-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="70374-127">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="70374-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="70374-128">Per le versioni 2 \_ x e successive, il registro degli indirizzi è un vettore di componenti.</span><span class="sxs-lookup"><span data-stu-id="70374-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="70374-129">Pertanto, qualsiasi maschera di scrittura è consentita.</span><span class="sxs-lookup"><span data-stu-id="70374-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="70374-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70374-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70374-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="70374-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





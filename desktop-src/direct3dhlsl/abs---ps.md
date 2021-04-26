---
title: abs - ps
description: Calcola il valore assoluto. | abs - ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3e7af7b2d30e9d9f2092cb6671610f008ec781d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994878"
---
# <a name="abs---ps"></a><span data-ttu-id="3522b-104">abs - ps</span><span class="sxs-lookup"><span data-stu-id="3522b-104">abs - ps</span></span>

<span data-ttu-id="3522b-105">Calcola il valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="3522b-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3522b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3522b-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="3522b-107">abs dst, src</span><span class="sxs-lookup"><span data-stu-id="3522b-107">abs dst, src</span></span> |



 

<span data-ttu-id="3522b-108">dove</span><span class="sxs-lookup"><span data-stu-id="3522b-108">where</span></span>

-   <span data-ttu-id="3522b-109">dst è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3522b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3522b-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="3522b-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3522b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3522b-111">Remarks</span></span>



| <span data-ttu-id="3522b-112">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3522b-112">Pixel shader versions</span></span> | <span data-ttu-id="3522b-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="3522b-113">1\_1</span></span> | <span data-ttu-id="3522b-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="3522b-114">1\_2</span></span> | <span data-ttu-id="3522b-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3522b-115">1\_3</span></span> | <span data-ttu-id="3522b-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="3522b-116">1\_4</span></span> | <span data-ttu-id="3522b-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3522b-117">2\_0</span></span> | <span data-ttu-id="3522b-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3522b-118">2\_x</span></span> | <span data-ttu-id="3522b-119">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3522b-119">2\_sw</span></span> | <span data-ttu-id="3522b-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3522b-120">3\_0</span></span> | <span data-ttu-id="3522b-121">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3522b-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3522b-122">abs</span><span class="sxs-lookup"><span data-stu-id="3522b-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="3522b-123">x</span><span class="sxs-lookup"><span data-stu-id="3522b-123">x</span></span>    | <span data-ttu-id="3522b-124">x</span><span class="sxs-lookup"><span data-stu-id="3522b-124">x</span></span>    | <span data-ttu-id="3522b-125">x</span><span class="sxs-lookup"><span data-stu-id="3522b-125">x</span></span>     | <span data-ttu-id="3522b-126">x</span><span class="sxs-lookup"><span data-stu-id="3522b-126">x</span></span>    | <span data-ttu-id="3522b-127">x</span><span class="sxs-lookup"><span data-stu-id="3522b-127">x</span></span>     |



 

<span data-ttu-id="3522b-128">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3522b-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="3522b-129">Informazioni sulle istruzioni</span><span class="sxs-lookup"><span data-stu-id="3522b-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="3522b-130">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="3522b-130">Minimum operating system</span></span> | <span data-ttu-id="3522b-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3522b-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3522b-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3522b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3522b-133">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="3522b-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





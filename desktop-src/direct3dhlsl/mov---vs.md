---
title: MOV-vs
description: Spostare i dati a virgola mobile tra i registri.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719453"
---
# <a name="mov---vs"></a><span data-ttu-id="dc338-103">MOV-vs</span><span class="sxs-lookup"><span data-stu-id="dc338-103">mov - vs</span></span>

<span data-ttu-id="dc338-104">Spostare i dati a virgola mobile tra i registri.</span><span class="sxs-lookup"><span data-stu-id="dc338-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc338-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc338-105">Syntax</span></span>



| <span data-ttu-id="dc338-106">MOV DST, src</span><span class="sxs-lookup"><span data-stu-id="dc338-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="dc338-107">dove</span><span class="sxs-lookup"><span data-stu-id="dc338-107">where</span></span>

-   <span data-ttu-id="dc338-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dc338-108">dst is the destination register.</span></span>
-   <span data-ttu-id="dc338-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="dc338-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc338-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc338-110">Remarks</span></span>



| <span data-ttu-id="dc338-111">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="dc338-111">Vertex shader versions</span></span> | <span data-ttu-id="dc338-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="dc338-112">1\_1</span></span> | <span data-ttu-id="dc338-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc338-113">2\_0</span></span> | <span data-ttu-id="dc338-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="dc338-114">2\_x</span></span> | <span data-ttu-id="dc338-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dc338-115">2\_sw</span></span> | <span data-ttu-id="dc338-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc338-116">3\_0</span></span> | <span data-ttu-id="dc338-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dc338-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="dc338-118">MOV</span><span class="sxs-lookup"><span data-stu-id="dc338-118">mov</span></span>                    | <span data-ttu-id="dc338-119">x</span><span class="sxs-lookup"><span data-stu-id="dc338-119">x</span></span>    | <span data-ttu-id="dc338-120">x</span><span class="sxs-lookup"><span data-stu-id="dc338-120">x</span></span>    | <span data-ttu-id="dc338-121">x</span><span class="sxs-lookup"><span data-stu-id="dc338-121">x</span></span>    | <span data-ttu-id="dc338-122">x</span><span class="sxs-lookup"><span data-stu-id="dc338-122">x</span></span>     | <span data-ttu-id="dc338-123">x</span><span class="sxs-lookup"><span data-stu-id="dc338-123">x</span></span>    | <span data-ttu-id="dc338-124">x</span><span class="sxs-lookup"><span data-stu-id="dc338-124">x</span></span>     |



 

<span data-ttu-id="dc338-125">Può essere usato per i dati a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="dc338-125">Can be used for floating point data.</span></span> <span data-ttu-id="dc338-126">Per la versione di Visual Studio \_ 1 \_ , può essere usata anche per scrivere il registro degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="dc338-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="dc338-127">Quando viene usato per aggiornare i registri indirizzi, i valori vengono convertiti da virgola mobile usando l'arrotondamento al più vicino.</span><span class="sxs-lookup"><span data-stu-id="dc338-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="dc338-128">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="dc338-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="dc338-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc338-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc338-130">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="dc338-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





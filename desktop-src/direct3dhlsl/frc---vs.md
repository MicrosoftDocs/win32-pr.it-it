---
title: FRC-vs
description: Restituisce la parte frazionaria di ogni componente di input. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353411"
---
# <a name="frc---vs"></a><span data-ttu-id="7cbec-104">FRC-vs</span><span class="sxs-lookup"><span data-stu-id="7cbec-104">frc - vs</span></span>

<span data-ttu-id="7cbec-105">Restituisce la parte frazionaria di ogni componente di input.</span><span class="sxs-lookup"><span data-stu-id="7cbec-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cbec-106">Syntax</span></span>



| <span data-ttu-id="7cbec-107">FRC DST, src</span><span class="sxs-lookup"><span data-stu-id="7cbec-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="7cbec-108">dove</span><span class="sxs-lookup"><span data-stu-id="7cbec-108">where</span></span>

-   <span data-ttu-id="7cbec-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7cbec-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7cbec-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="7cbec-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cbec-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cbec-111">Remarks</span></span>



| <span data-ttu-id="7cbec-112">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="7cbec-112">Vertex shader versions</span></span> | <span data-ttu-id="7cbec-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="7cbec-113">1\_1</span></span> | <span data-ttu-id="7cbec-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cbec-114">2\_0</span></span> | <span data-ttu-id="7cbec-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7cbec-115">2\_x</span></span> | <span data-ttu-id="7cbec-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cbec-116">2\_sw</span></span> | <span data-ttu-id="7cbec-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cbec-117">3\_0</span></span> | <span data-ttu-id="7cbec-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cbec-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7cbec-119">FRC</span><span class="sxs-lookup"><span data-stu-id="7cbec-119">frc</span></span>                    | <span data-ttu-id="7cbec-120">x</span><span class="sxs-lookup"><span data-stu-id="7cbec-120">x</span></span>    | <span data-ttu-id="7cbec-121">x</span><span class="sxs-lookup"><span data-stu-id="7cbec-121">x</span></span>    | <span data-ttu-id="7cbec-122">x</span><span class="sxs-lookup"><span data-stu-id="7cbec-122">x</span></span>    | <span data-ttu-id="7cbec-123">x</span><span class="sxs-lookup"><span data-stu-id="7cbec-123">x</span></span>     | <span data-ttu-id="7cbec-124">x</span><span class="sxs-lookup"><span data-stu-id="7cbec-124">x</span></span>    | <span data-ttu-id="7cbec-125">x</span><span class="sxs-lookup"><span data-stu-id="7cbec-125">x</span></span>     |



 

<span data-ttu-id="7cbec-126">Il frammento di codice seguente mostra concettualmente il funzionamento dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="7cbec-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="7cbec-127">La funzione floor converte l'argomento passato all'intero più grande che è minore o uguale all'argomento.</span><span class="sxs-lookup"><span data-stu-id="7cbec-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="7cbec-128">Viene convertito in un valore float, quindi viene sottratto il valore originale.</span><span class="sxs-lookup"><span data-stu-id="7cbec-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="7cbec-129">Il valore frazionario risultante è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="7cbec-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="7cbec-130">Per la versione 1 \_ , le maschere di scrittura consentite sono. y e. XY (. x non è consentito).</span><span class="sxs-lookup"><span data-stu-id="7cbec-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cbec-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cbec-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cbec-132">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="7cbec-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





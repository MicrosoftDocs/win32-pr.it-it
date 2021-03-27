---
title: texm3x2pad-PS
description: Esegue la moltiplicazione della prima riga di una matrice a due righe. Questa istruzione deve essere combinata con texm3x2tex-PS o texm3x2depth-PS. Per informazioni dettagliate sull'uso di texmpad, fare riferimento a una di queste istruzioni.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857786"
---
# <a name="texm3x2pad---ps"></a><span data-ttu-id="375ac-105">texm3x2pad-PS</span><span class="sxs-lookup"><span data-stu-id="375ac-105">texm3x2pad - ps</span></span>

<span data-ttu-id="375ac-106">Esegue la moltiplicazione della prima riga di una matrice a due righe.</span><span class="sxs-lookup"><span data-stu-id="375ac-106">Performs the first row multiplication of a two-row matrix multiply.</span></span> <span data-ttu-id="375ac-107">Questa istruzione deve essere combinata con [texm3x2tex-PS](texm3x2tex---ps.md) o [texm3x2depth-PS](texm3x2depth---ps.md).</span><span class="sxs-lookup"><span data-stu-id="375ac-107">This instruction must be combined with either [texm3x2tex - ps](texm3x2tex---ps.md) or [texm3x2depth - ps](texm3x2depth---ps.md).</span></span> <span data-ttu-id="375ac-108">Per informazioni dettagliate sull'uso di texmpad, fare riferimento a una di queste istruzioni.</span><span class="sxs-lookup"><span data-stu-id="375ac-108">Refer to either of these instructions for details on using texmpad.</span></span>

## <a name="syntax"></a><span data-ttu-id="375ac-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="375ac-109">Syntax</span></span>



| <span data-ttu-id="375ac-110">tex3x2pad DST, src</span><span class="sxs-lookup"><span data-stu-id="375ac-110">tex3x2pad dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="375ac-111">dove</span><span class="sxs-lookup"><span data-stu-id="375ac-111">where</span></span>

-   <span data-ttu-id="375ac-112">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="375ac-112">dst is the destination register.</span></span>
-   <span data-ttu-id="375ac-113">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="375ac-113">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="375ac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="375ac-114">Remarks</span></span>



| <span data-ttu-id="375ac-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="375ac-115">Pixel shader versions</span></span> | <span data-ttu-id="375ac-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="375ac-116">1\_1</span></span> | <span data-ttu-id="375ac-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="375ac-117">1\_2</span></span> | <span data-ttu-id="375ac-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="375ac-118">1\_3</span></span> | <span data-ttu-id="375ac-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="375ac-119">1\_4</span></span> | <span data-ttu-id="375ac-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="375ac-120">2\_0</span></span> | <span data-ttu-id="375ac-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="375ac-121">2\_x</span></span> | <span data-ttu-id="375ac-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="375ac-122">2\_sw</span></span> | <span data-ttu-id="375ac-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="375ac-123">3\_0</span></span> | <span data-ttu-id="375ac-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="375ac-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="375ac-125">texm3x2pad</span><span class="sxs-lookup"><span data-stu-id="375ac-125">texm3x2pad</span></span>            | <span data-ttu-id="375ac-126">x</span><span class="sxs-lookup"><span data-stu-id="375ac-126">x</span></span>    | <span data-ttu-id="375ac-127">x</span><span class="sxs-lookup"><span data-stu-id="375ac-127">x</span></span>    | <span data-ttu-id="375ac-128">x</span><span class="sxs-lookup"><span data-stu-id="375ac-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="375ac-129">Questa istruzione non può essere usata da sola.</span><span class="sxs-lookup"><span data-stu-id="375ac-129">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="375ac-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="375ac-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="375ac-131">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="375ac-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





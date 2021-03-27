---
title: texm3x3pad-PS
description: Esegue la prima o la seconda moltiplicazione di riga di una matrice a tre righe di moltiplicazione. Questa istruzione deve essere usata in combinazione con texm3x3-PS, texm3x3spec-PS, texm3x3vspec-PS o texm3x3tex-PS.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0013c4d2baf9a404406982b5a8e984698a964f33
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398235"
---
# <a name="texm3x3pad---ps"></a><span data-ttu-id="0edc3-104">texm3x3pad-PS</span><span class="sxs-lookup"><span data-stu-id="0edc3-104">texm3x3pad - ps</span></span>

<span data-ttu-id="0edc3-105">Esegue la prima o la seconda moltiplicazione di riga di una matrice a tre righe di moltiplicazione.</span><span class="sxs-lookup"><span data-stu-id="0edc3-105">Performs the first or second row multiply of a three-row matrix multiply.</span></span> <span data-ttu-id="0edc3-106">Questa istruzione deve essere usata in combinazione con [texm3x3-PS](texm3x3---ps.md), [texm3x3spec-PS](texm3x3spec---ps.md), [texm3x3vspec-PS](texm3x3vspec---ps.md)o [texm3x3tex-PS](texm3x3tex---ps.md).</span><span class="sxs-lookup"><span data-stu-id="0edc3-106">This instruction must be used in combination with [texm3x3 - ps](texm3x3---ps.md), [texm3x3spec - ps](texm3x3spec---ps.md), [texm3x3vspec - ps](texm3x3vspec---ps.md), or [texm3x3tex - ps](texm3x3tex---ps.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0edc3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0edc3-107">Syntax</span></span>



| <span data-ttu-id="0edc3-108">texm3x3pad DST, src</span><span class="sxs-lookup"><span data-stu-id="0edc3-108">texm3x3pad dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="0edc3-109">dove</span><span class="sxs-lookup"><span data-stu-id="0edc3-109">where</span></span>

-   <span data-ttu-id="0edc3-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0edc3-110">dst is the destination register.</span></span>
-   <span data-ttu-id="0edc3-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="0edc3-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0edc3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0edc3-112">Remarks</span></span>



| <span data-ttu-id="0edc3-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0edc3-113">Pixel shader versions</span></span> | <span data-ttu-id="0edc3-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0edc3-114">1\_1</span></span> | <span data-ttu-id="0edc3-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0edc3-115">1\_2</span></span> | <span data-ttu-id="0edc3-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0edc3-116">1\_3</span></span> | <span data-ttu-id="0edc3-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0edc3-117">1\_4</span></span> | <span data-ttu-id="0edc3-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0edc3-118">2\_0</span></span> | <span data-ttu-id="0edc3-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0edc3-119">2\_x</span></span> | <span data-ttu-id="0edc3-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0edc3-120">2\_sw</span></span> | <span data-ttu-id="0edc3-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0edc3-121">3\_0</span></span> | <span data-ttu-id="0edc3-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0edc3-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0edc3-123">texm3x3pad</span><span class="sxs-lookup"><span data-stu-id="0edc3-123">texm3x3pad</span></span>            | <span data-ttu-id="0edc3-124">x</span><span class="sxs-lookup"><span data-stu-id="0edc3-124">x</span></span>    | <span data-ttu-id="0edc3-125">x</span><span class="sxs-lookup"><span data-stu-id="0edc3-125">x</span></span>    | <span data-ttu-id="0edc3-126">x</span><span class="sxs-lookup"><span data-stu-id="0edc3-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0edc3-127">Questa istruzione non può essere usata da sola.</span><span class="sxs-lookup"><span data-stu-id="0edc3-127">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0edc3-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0edc3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0edc3-129">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0edc3-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





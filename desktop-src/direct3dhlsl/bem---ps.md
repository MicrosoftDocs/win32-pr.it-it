---
title: bem - ps
description: Applicare una trasformazione mappa dell'ambiente di urto fittizia.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129930"
---
# <a name="bem---ps"></a><span data-ttu-id="de5d8-103">bem - ps</span><span class="sxs-lookup"><span data-stu-id="de5d8-103">bem - ps</span></span>

<span data-ttu-id="de5d8-104">Applicare una trasformazione mappa dell'ambiente di urto fittizia.</span><span class="sxs-lookup"><span data-stu-id="de5d8-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de5d8-105">Syntax</span></span>



| <span data-ttu-id="de5d8-106">bem dst.rg, src0, src1</span><span class="sxs-lookup"><span data-stu-id="de5d8-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="de5d8-107">dove</span><span class="sxs-lookup"><span data-stu-id="de5d8-107">where</span></span>

-   <span data-ttu-id="de5d8-108">dst.rg dst è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="de5d8-109">È necessario usare la maschera di scrittura del componente rosso e verde.</span><span class="sxs-lookup"><span data-stu-id="de5d8-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="de5d8-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="de5d8-110">src0 is a source register.</span></span>
-   <span data-ttu-id="de5d8-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="de5d8-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5d8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="de5d8-112">Remarks</span></span>



| <span data-ttu-id="de5d8-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="de5d8-113">Pixel shader versions</span></span> | <span data-ttu-id="de5d8-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="de5d8-114">1\_1</span></span> | <span data-ttu-id="de5d8-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="de5d8-115">1\_2</span></span> | <span data-ttu-id="de5d8-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="de5d8-116">1\_3</span></span> | <span data-ttu-id="de5d8-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="de5d8-117">1\_4</span></span> | <span data-ttu-id="de5d8-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de5d8-118">2\_0</span></span> | <span data-ttu-id="de5d8-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="de5d8-119">2\_x</span></span> | <span data-ttu-id="de5d8-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="de5d8-120">2\_sw</span></span> | <span data-ttu-id="de5d8-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de5d8-121">3\_0</span></span> | <span data-ttu-id="de5d8-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="de5d8-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="de5d8-123">Bem</span><span class="sxs-lookup"><span data-stu-id="de5d8-123">bem</span></span>                   |      |      |      | <span data-ttu-id="de5d8-124">x</span><span class="sxs-lookup"><span data-stu-id="de5d8-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="de5d8-125">Questa istruzione esegue il calcolo seguente.</span><span class="sxs-lookup"><span data-stu-id="de5d8-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="de5d8-126">Regole per l'uso di bem:</span><span class="sxs-lookup"><span data-stu-id="de5d8-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="de5d8-127">bem deve essere visualizzato nella prima fase di uno shader, ovvero prima di un marcatore di fase.</span><span class="sxs-lookup"><span data-stu-id="de5d8-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="de5d8-128">bem utilizza due slot di istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="de5d8-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="de5d8-129">È consentito un solo uso di questa istruzione per shader.</span><span class="sxs-lookup"><span data-stu-id="de5d8-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="de5d8-130">La maschera di scrittura di destinazione deve essere .rg /.xy.</span><span class="sxs-lookup"><span data-stu-id="de5d8-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="de5d8-131">Questa istruzione non può essere co-rilasciata.</span><span class="sxs-lookup"><span data-stu-id="de5d8-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="de5d8-132">A parte la restrizione che destination write mask è rg, i modificatori di origine src0, src1 e i modificatori di istruzione non sono vincolati.</span><span class="sxs-lookup"><span data-stu-id="de5d8-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="de5d8-133">Informazioni sulle istruzioni</span><span class="sxs-lookup"><span data-stu-id="de5d8-133">Instruction Information</span></span>



| <span data-ttu-id="de5d8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5d8-134">Requirement</span></span>                         | <span data-ttu-id="de5d8-135">Valore</span><span class="sxs-lookup"><span data-stu-id="de5d8-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="de5d8-136">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="de5d8-136">Minimum operating system</span></span> | <span data-ttu-id="de5d8-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="de5d8-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="de5d8-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de5d8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de5d8-139">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="de5d8-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





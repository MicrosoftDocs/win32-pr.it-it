---
title: bem-PS
description: Applicare una trasformazione della mappa dell'ambiente di Bump Fake.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398264"
---
# <a name="bem---ps"></a><span data-ttu-id="8cab1-103">bem-PS</span><span class="sxs-lookup"><span data-stu-id="8cab1-103">bem - ps</span></span>

<span data-ttu-id="8cab1-104">Applicare una trasformazione della mappa dell'ambiente di Bump Fake.</span><span class="sxs-lookup"><span data-stu-id="8cab1-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cab1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8cab1-105">Syntax</span></span>



| <span data-ttu-id="8cab1-106">bem DST. RG, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8cab1-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="8cab1-107">dove</span><span class="sxs-lookup"><span data-stu-id="8cab1-107">where</span></span>

-   <span data-ttu-id="8cab1-108">DST. RG DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cab1-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="8cab1-109">È necessario utilizzare la maschera di scrittura del componente rosso e verde.</span><span class="sxs-lookup"><span data-stu-id="8cab1-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="8cab1-110">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="8cab1-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8cab1-111">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="8cab1-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cab1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cab1-112">Remarks</span></span>



| <span data-ttu-id="8cab1-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="8cab1-113">Pixel shader versions</span></span> | <span data-ttu-id="8cab1-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8cab1-114">1\_1</span></span> | <span data-ttu-id="8cab1-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="8cab1-115">1\_2</span></span> | <span data-ttu-id="8cab1-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8cab1-116">1\_3</span></span> | <span data-ttu-id="8cab1-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="8cab1-117">1\_4</span></span> | <span data-ttu-id="8cab1-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8cab1-118">2\_0</span></span> | <span data-ttu-id="8cab1-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8cab1-119">2\_x</span></span> | <span data-ttu-id="8cab1-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8cab1-120">2\_sw</span></span> | <span data-ttu-id="8cab1-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8cab1-121">3\_0</span></span> | <span data-ttu-id="8cab1-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8cab1-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8cab1-123">bem</span><span class="sxs-lookup"><span data-stu-id="8cab1-123">bem</span></span>                   |      |      |      | <span data-ttu-id="8cab1-124">x</span><span class="sxs-lookup"><span data-stu-id="8cab1-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="8cab1-125">Questa istruzione esegue il calcolo seguente.</span><span class="sxs-lookup"><span data-stu-id="8cab1-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="8cab1-126">Regole per l'uso di bem:</span><span class="sxs-lookup"><span data-stu-id="8cab1-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="8cab1-127">il bem deve essere visualizzato nella prima fase di uno shader, ovvero prima di un marcatore di fase.</span><span class="sxs-lookup"><span data-stu-id="8cab1-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="8cab1-128">bem usa due slot di istruzione aritmetici.</span><span class="sxs-lookup"><span data-stu-id="8cab1-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="8cab1-129">È consentito un solo utilizzo di questa istruzione per shader.</span><span class="sxs-lookup"><span data-stu-id="8cab1-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="8cab1-130">Il writemask di destinazione deve essere. RG/.XY.</span><span class="sxs-lookup"><span data-stu-id="8cab1-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="8cab1-131">Questa istruzione non può essere rilasciata.</span><span class="sxs-lookup"><span data-stu-id="8cab1-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="8cab1-132">A parte la restrizione, la maschera di scrittura della destinazione è. RG, i modificatori nei modificatori di origine src0, src1 e istruzioni non sono vincolati.</span><span class="sxs-lookup"><span data-stu-id="8cab1-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="8cab1-133">Informazioni istruzioni</span><span class="sxs-lookup"><span data-stu-id="8cab1-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="8cab1-134">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="8cab1-134">Minimum operating system</span></span> | <span data-ttu-id="8cab1-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8cab1-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8cab1-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cab1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cab1-137">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="8cab1-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





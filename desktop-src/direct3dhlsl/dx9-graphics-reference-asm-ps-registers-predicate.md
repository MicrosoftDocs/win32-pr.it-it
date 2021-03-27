---
title: Registro predicato (riferimenti per HLSL PS)
description: Questo pixel shader registro di output contiene un valore booleano per canale.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719531"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="299f3-103">Registro predicato (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="299f3-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="299f3-104">Questo pixel shader registro di output contiene un valore booleano per canale.</span><span class="sxs-lookup"><span data-stu-id="299f3-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="299f3-105">Un registro predicato è supportato dalle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="299f3-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="299f3-106">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="299f3-106">Pixel shader versions</span></span> | <span data-ttu-id="299f3-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="299f3-107">1\_1</span></span> | <span data-ttu-id="299f3-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="299f3-108">1\_2</span></span> | <span data-ttu-id="299f3-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="299f3-109">1\_3</span></span> | <span data-ttu-id="299f3-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="299f3-110">1\_4</span></span> | <span data-ttu-id="299f3-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="299f3-111">2\_0</span></span> | <span data-ttu-id="299f3-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="299f3-112">2\_sw</span></span> | <span data-ttu-id="299f3-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="299f3-113">2\_x</span></span> | <span data-ttu-id="299f3-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="299f3-114">3\_0</span></span> | <span data-ttu-id="299f3-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="299f3-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="299f3-116">registro predicato</span><span class="sxs-lookup"><span data-stu-id="299f3-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="299f3-117">x</span><span class="sxs-lookup"><span data-stu-id="299f3-117">x</span></span>    | <span data-ttu-id="299f3-118">x</span><span class="sxs-lookup"><span data-stu-id="299f3-118">x</span></span>    | <span data-ttu-id="299f3-119">x</span><span class="sxs-lookup"><span data-stu-id="299f3-119">x</span></span>     |



 

<span data-ttu-id="299f3-120">Di seguito sono riportate le proprietà Register.</span><span class="sxs-lookup"><span data-stu-id="299f3-120">Here are the register properties.</span></span>



| <span data-ttu-id="299f3-121">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="299f3-121">Register type</span></span> | <span data-ttu-id="299f3-122">Conteggio</span><span class="sxs-lookup"><span data-stu-id="299f3-122">Count</span></span> | <span data-ttu-id="299f3-123">L/S</span><span class="sxs-lookup"><span data-stu-id="299f3-123">R/W</span></span> | <span data-ttu-id="299f3-124">\# Leggere le porte</span><span class="sxs-lookup"><span data-stu-id="299f3-124">\# Read ports</span></span> | <span data-ttu-id="299f3-125">\# Letture/Inst</span><span class="sxs-lookup"><span data-stu-id="299f3-125">\# Reads/inst</span></span> | <span data-ttu-id="299f3-126">Dimension</span><span class="sxs-lookup"><span data-stu-id="299f3-126">Dimension</span></span> | <span data-ttu-id="299f3-127">Relannr</span><span class="sxs-lookup"><span data-stu-id="299f3-127">RelAddr</span></span> | <span data-ttu-id="299f3-128">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="299f3-128">Defaults</span></span> | <span data-ttu-id="299f3-129">Richiede DCL</span><span class="sxs-lookup"><span data-stu-id="299f3-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="299f3-130">Predicato (p)</span><span class="sxs-lookup"><span data-stu-id="299f3-130">Predicate(p)</span></span>  | <span data-ttu-id="299f3-131">1</span><span class="sxs-lookup"><span data-stu-id="299f3-131">1</span></span>     | <span data-ttu-id="299f3-132">L/S</span><span class="sxs-lookup"><span data-stu-id="299f3-132">R/W</span></span> | <span data-ttu-id="299f3-133">1</span><span class="sxs-lookup"><span data-stu-id="299f3-133">1</span></span>             | <span data-ttu-id="299f3-134">1</span><span class="sxs-lookup"><span data-stu-id="299f3-134">1</span></span>             | <span data-ttu-id="299f3-135">4</span><span class="sxs-lookup"><span data-stu-id="299f3-135">4</span></span>         | <span data-ttu-id="299f3-136">N/D</span><span class="sxs-lookup"><span data-stu-id="299f3-136">N/A</span></span>     | <span data-ttu-id="299f3-137">nessuno</span><span class="sxs-lookup"><span data-stu-id="299f3-137">None</span></span>     | <span data-ttu-id="299f3-138">N</span><span class="sxs-lookup"><span data-stu-id="299f3-138">N</span></span>            |



 

<span data-ttu-id="299f3-139">Il registro del predicato può essere modificato con [setp \_ comp-PS](setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="299f3-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="299f3-140">Nessun valore predefinito per questo registro. un'applicazione deve impostare il registro prima che venga usato.</span><span class="sxs-lookup"><span data-stu-id="299f3-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="299f3-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="299f3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="299f3-142">Registri</span><span class="sxs-lookup"><span data-stu-id="299f3-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





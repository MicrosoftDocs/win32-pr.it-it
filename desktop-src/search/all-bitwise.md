---
description: TUTTE le parole chiave bit per bit and bit per bit vengono usate per il testing dei bit in un tipo integrale.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ALL bit per bit e SOME bit per bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525471"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="0f652-103">ALL bit per bit e SOME bit per bit</span><span class="sxs-lookup"><span data-stu-id="0f652-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="0f652-104">**Tutte** le parole chiave bit per bit **and bit per** bit vengono usate per il testing dei bit in un tipo integrale.</span><span class="sxs-lookup"><span data-stu-id="0f652-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="0f652-105">Se tutti i bit impostati in una proprietà corrispondono alla maschera, **All bit per bit** è true.</span><span class="sxs-lookup"><span data-stu-id="0f652-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="0f652-106">Se almeno uno dei bit impostati in una proprietà corrisponde alla maschera, **some bit per bit** è true.</span><span class="sxs-lookup"><span data-stu-id="0f652-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="0f652-107">Gli operatori possono essere applicati sia alle proprietà scalari (a valore singolo) che alle proprietà Vector (multiple-value).</span><span class="sxs-lookup"><span data-stu-id="0f652-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="0f652-108">Nell'esempio di codice seguente viene illustrato come testare i valori delle proprietà con **tutti gli operatori bit per bit** e **bit per bit**.</span><span class="sxs-lookup"><span data-stu-id="0f652-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="0f652-109">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="0f652-109">Comparison Operators</span></span>

<span data-ttu-id="0f652-110">Nella tabella seguente sono elencati gli operatori di confronto supportati per i test bit per bit.</span><span class="sxs-lookup"><span data-stu-id="0f652-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="0f652-111">Operatore di confronto</span><span class="sxs-lookup"><span data-stu-id="0f652-111">Comparison operator</span></span> | <span data-ttu-id="0f652-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f652-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="0f652-113">Uguale a</span><span class="sxs-lookup"><span data-stu-id="0f652-113">Equal to</span></span>     |
| <span data-ttu-id="0f652-114">! = o <></span><span class="sxs-lookup"><span data-stu-id="0f652-114">!= or <></span></span>      | <span data-ttu-id="0f652-115">Diverso da</span><span class="sxs-lookup"><span data-stu-id="0f652-115">Not equal to</span></span> |



 

<span data-ttu-id="0f652-116">La logica dei test bit per bit è elencata nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0f652-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="0f652-117">Operatore di confronto e test bit per bit</span><span class="sxs-lookup"><span data-stu-id="0f652-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="0f652-118">Logica</span><span class="sxs-lookup"><span data-stu-id="0f652-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="0f652-119">= TUTTO BIT PER BIT</span><span class="sxs-lookup"><span data-stu-id="0f652-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="0f652-120">Proprietà & mask = mask</span><span class="sxs-lookup"><span data-stu-id="0f652-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="0f652-121">= SOME BIT PER BIT</span><span class="sxs-lookup"><span data-stu-id="0f652-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="0f652-122">Proprietà & mask! = 0</span><span class="sxs-lookup"><span data-stu-id="0f652-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="0f652-123"><> BIT PER BIT</span><span class="sxs-lookup"><span data-stu-id="0f652-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="0f652-124">Proprietà & mask! = mask</span><span class="sxs-lookup"><span data-stu-id="0f652-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="0f652-125"><> BIT PER BIT</span><span class="sxs-lookup"><span data-stu-id="0f652-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="0f652-126">Proprietà & mask = 0</span><span class="sxs-lookup"><span data-stu-id="0f652-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="0f652-127">La tabella di verità seguente usa i valori binari e esadecimali di esempio per demonstate la logica dei test bit per bit.</span><span class="sxs-lookup"><span data-stu-id="0f652-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="0f652-128">Property in Binary (hex)</span><span class="sxs-lookup"><span data-stu-id="0f652-128">Property in binary (hex)</span></span> | <span data-ttu-id="0f652-129">Maschera in binario (esadecimale)</span><span class="sxs-lookup"><span data-stu-id="0f652-129">Mask in binary (hex)</span></span> | <span data-ttu-id="0f652-130">Property & mask = Binary (hex)</span><span class="sxs-lookup"><span data-stu-id="0f652-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="0f652-131">= SOME BIT PER BIT</span><span class="sxs-lookup"><span data-stu-id="0f652-131">= SOME BITWISE</span></span> | <span data-ttu-id="0f652-132">= TUTTO BIT PER BIT</span><span class="sxs-lookup"><span data-stu-id="0f652-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="0f652-133">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-133">0001 (0x1)</span></span>               | <span data-ttu-id="0f652-134">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-134">0001 (0x1)</span></span>           | <span data-ttu-id="0f652-135">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-135">0001 (0x1)</span></span>                     | <span data-ttu-id="0f652-136">True</span><span class="sxs-lookup"><span data-stu-id="0f652-136">True</span></span>           | <span data-ttu-id="0f652-137">True</span><span class="sxs-lookup"><span data-stu-id="0f652-137">True</span></span>          |
| <span data-ttu-id="0f652-138">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-138">0001 (0x1)</span></span>               | <span data-ttu-id="0f652-139">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="0f652-139">0011 (0x3)</span></span>           | <span data-ttu-id="0f652-140">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-140">0001 (0x1)</span></span>                     | <span data-ttu-id="0f652-141">Vero</span><span class="sxs-lookup"><span data-stu-id="0f652-141">True</span></span>           | <span data-ttu-id="0f652-142">Falso</span><span class="sxs-lookup"><span data-stu-id="0f652-142">False</span></span>         |
| <span data-ttu-id="0f652-143">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="0f652-143">0011 (0x3)</span></span>               | <span data-ttu-id="0f652-144">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-144">0001 (0x1)</span></span>           | <span data-ttu-id="0f652-145">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-145">0001 (0x1)</span></span>                     | <span data-ttu-id="0f652-146">True</span><span class="sxs-lookup"><span data-stu-id="0f652-146">True</span></span>           | <span data-ttu-id="0f652-147">True</span><span class="sxs-lookup"><span data-stu-id="0f652-147">True</span></span>          |
| <span data-ttu-id="0f652-148">0010 (0x2)</span><span class="sxs-lookup"><span data-stu-id="0f652-148">0010 (0x2)</span></span>               | <span data-ttu-id="0f652-149">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0f652-149">0001 (0x1)</span></span>           | <span data-ttu-id="0f652-150">0000 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0f652-150">0000 (0x0)</span></span>                     | <span data-ttu-id="0f652-151">False</span><span class="sxs-lookup"><span data-stu-id="0f652-151">False</span></span>          | <span data-ttu-id="0f652-152">False</span><span class="sxs-lookup"><span data-stu-id="0f652-152">False</span></span>         |
| <span data-ttu-id="0f652-153">11110000 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="0f652-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="0f652-154">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="0f652-154">00000011 (0x03)</span></span>      | <span data-ttu-id="0f652-155">00000000 (0x00)</span><span class="sxs-lookup"><span data-stu-id="0f652-155">00000000 (0x00)</span></span>                | <span data-ttu-id="0f652-156">False</span><span class="sxs-lookup"><span data-stu-id="0f652-156">False</span></span>          | <span data-ttu-id="0f652-157">False</span><span class="sxs-lookup"><span data-stu-id="0f652-157">False</span></span>         |
| <span data-ttu-id="0f652-158">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="0f652-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="0f652-159">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="0f652-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="0f652-160">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="0f652-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="0f652-161">True</span><span class="sxs-lookup"><span data-stu-id="0f652-161">True</span></span>           | <span data-ttu-id="0f652-162">True</span><span class="sxs-lookup"><span data-stu-id="0f652-162">True</span></span>          |
| <span data-ttu-id="0f652-163">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="0f652-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="0f652-164">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="0f652-164">00000011 (0x03)</span></span>      | <span data-ttu-id="0f652-165">00000010 (0x02)</span><span class="sxs-lookup"><span data-stu-id="0f652-165">00000010 (0x02)</span></span>                | <span data-ttu-id="0f652-166">Vero</span><span class="sxs-lookup"><span data-stu-id="0f652-166">True</span></span>           | <span data-ttu-id="0f652-167">Falso</span><span class="sxs-lookup"><span data-stu-id="0f652-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="0f652-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f652-168">Example</span></span>

<span data-ttu-id="0f652-169">Di seguito è riportato un esempio del predicato **All bit per bit** .</span><span class="sxs-lookup"><span data-stu-id="0f652-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="0f652-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f652-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0f652-171">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0f652-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f652-172">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="0f652-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="0f652-173">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="0f652-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




---
description: ICEM02 verifica che tutte le dipendenze ed esclusioni dei moduli siano correlate al modulo corrente.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226448"
---
# <a name="icem02"></a><span data-ttu-id="8328b-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="8328b-103">ICEM02</span></span>

<span data-ttu-id="8328b-104">ICEM02 verifica che tutte le dipendenze ed esclusioni dei moduli siano correlate al modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="8328b-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="8328b-105">I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8328b-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="8328b-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="8328b-106">Result</span></span>

<span data-ttu-id="8328b-107">ICEM02 invia messaggi di errore se il database del modulo tenta di specificare dipendenze o esclusioni che non sono correlate al modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="8328b-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="8328b-108">ICEM02 Invia un messaggio di errore se il database del modulo tenta di specificare il modulo corrente come dipendente o escluso da solo.</span><span class="sxs-lookup"><span data-stu-id="8328b-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="8328b-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="8328b-109">Example</span></span>

<span data-ttu-id="8328b-110">ICEM02 invierà i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="8328b-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="8328b-111">Tabella ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="8328b-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="8328b-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8328b-112">ModuleID</span></span>         | <span data-ttu-id="8328b-113">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="8328b-113">Language</span></span> | <span data-ttu-id="8328b-114">Versione</span><span class="sxs-lookup"><span data-stu-id="8328b-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="8328b-115">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="8328b-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="8328b-116">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-116">1033</span></span>     | <span data-ttu-id="8328b-117">1.0</span><span class="sxs-lookup"><span data-stu-id="8328b-117">1.0</span></span>     |



 

[<span data-ttu-id="8328b-118">Tabella ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="8328b-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="8328b-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8328b-119">ModuleID</span></span>            | <span data-ttu-id="8328b-120">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="8328b-120">ModuleLanguage</span></span> | <span data-ttu-id="8328b-121">RequiredID</span><span class="sxs-lookup"><span data-stu-id="8328b-121">RequiredID</span></span>          | <span data-ttu-id="8328b-122">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="8328b-122">RequiredLanguage</span></span> | <span data-ttu-id="8328b-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="8328b-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="8328b-124">OtherModule. *Guid2*</span><span class="sxs-lookup"><span data-stu-id="8328b-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="8328b-125">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-125">1033</span></span>           | <span data-ttu-id="8328b-126">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="8328b-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="8328b-127">0</span><span class="sxs-lookup"><span data-stu-id="8328b-127">0</span></span>                | <span data-ttu-id="8328b-128">1.0</span><span class="sxs-lookup"><span data-stu-id="8328b-128">1.0</span></span>             |
| <span data-ttu-id="8328b-129">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="8328b-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="8328b-130">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-130">1033</span></span>           | <span data-ttu-id="8328b-131">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="8328b-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="8328b-132">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-132">1033</span></span>             | <span data-ttu-id="8328b-133">1.2</span><span class="sxs-lookup"><span data-stu-id="8328b-133">1.2</span></span>             |



 

<span data-ttu-id="8328b-134">[Tabella ModuleExclusion](moduleexclusion-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8328b-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="8328b-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8328b-135">ModuleID</span></span>            | <span data-ttu-id="8328b-136">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="8328b-136">ModuleLanguage</span></span> | <span data-ttu-id="8328b-137">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="8328b-137">ExcludedID</span></span>          | <span data-ttu-id="8328b-138">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="8328b-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="8328b-139">OtherModule. *Guid2*</span><span class="sxs-lookup"><span data-stu-id="8328b-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="8328b-140">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-140">1033</span></span>           | <span data-ttu-id="8328b-141">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="8328b-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="8328b-142">0</span><span class="sxs-lookup"><span data-stu-id="8328b-142">0</span></span>                |
| <span data-ttu-id="8328b-143">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="8328b-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="8328b-144">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-144">1033</span></span>           | <span data-ttu-id="8328b-145">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="8328b-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="8328b-146">1033</span><span class="sxs-lookup"><span data-stu-id="8328b-146">1033</span></span>             |



 

<span data-ttu-id="8328b-147">Il modulo merge ICE registra il primo errore perché la della prima riga nella tabella ModuleDependency, che non specifica una dipendenza obbligatoria per il modulo corrente specificato nella tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="8328b-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="8328b-148">Le dipendenze di un modulo possono essere specificate solo nella propria tabella ModuleDependency.</span><span class="sxs-lookup"><span data-stu-id="8328b-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="8328b-149">Se OtherModule. *GUID3* è richiesto dal modulo corrente, sostituire le prime due colonne della riga con i dati della tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="8328b-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="8328b-150">Se OtherModule. *GUID3* non è richiesto da questo modulo, eliminare questa riga.</span><span class="sxs-lookup"><span data-stu-id="8328b-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="8328b-151">Il modulo merge ICE registra il secondo errore perché un modulo non può specificare una dipendenza su se stesso.</span><span class="sxs-lookup"><span data-stu-id="8328b-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="8328b-152">Il modulo merge ICE inserisce il terzo errore a causa della prima riga nella tabella ModuleExclusion, che non specifica un'esclusione obbligatoria per il modulo corrente specificato nella tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="8328b-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="8328b-153">Le esclusioni di un modulo possono essere specificate solo nella propria tabella ModuleExclusion.</span><span class="sxs-lookup"><span data-stu-id="8328b-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="8328b-154">Se il modulo corrente esclude OtherModule. *GUID3*, sostituire le prime due colonne della riga con i dati della tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="8328b-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="8328b-155">Se il modulo corrente non esclude OtherModule. *GUID3*, eliminare questa riga.</span><span class="sxs-lookup"><span data-stu-id="8328b-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="8328b-156">Il modulo merge ICE inserisce il quarto errore perché un modulo non è in grado di specificare che escluda se stesso.</span><span class="sxs-lookup"><span data-stu-id="8328b-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8328b-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8328b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8328b-158">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="8328b-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 




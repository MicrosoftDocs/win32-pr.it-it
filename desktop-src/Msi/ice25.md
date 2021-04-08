---
description: ICE25 verifica che un file con estensione msi soddisfi tutte le dipendenze ed esclusioni dei moduli di merge interni.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882938"
---
# <a name="ice25"></a><span data-ttu-id="a830d-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="a830d-103">ICE25</span></span>

<span data-ttu-id="a830d-104">ICE25 verifica che un file con estensione msi soddisfi tutte le dipendenze ed esclusioni dei [moduli di merge](merge-modules.md) interni.</span><span class="sxs-lookup"><span data-stu-id="a830d-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="a830d-105">ICE convalida quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a830d-105">ICE validates the following:</span></span>

-   <span data-ttu-id="a830d-106">Tutte le dipendenze del modulo merge indicate nella [tabella ModuleDependency](moduledependency-table.md) del file con estensione msi vengono soddisfatte da almeno un modulo merge elencato nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a830d-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="a830d-107">Nessuno dei moduli unione esclusi nella [tabella ModuleExclusion](moduleexclusion-table.md) non è compatibile con i moduli unione elencati nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a830d-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="a830d-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="a830d-108">Result</span></span>

<span data-ttu-id="a830d-109">ICE25 Invia un messaggio di errore se il file con estensione msi è stato precedentemente Unito a un modulo merge non compatibile o se non è stato unito a un modulo Merge necessario.</span><span class="sxs-lookup"><span data-stu-id="a830d-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="a830d-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="a830d-110">Example</span></span>

<span data-ttu-id="a830d-111">ICE25 invia gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="a830d-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="a830d-112">Tabella ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="a830d-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="a830d-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="a830d-113">ModuleID</span></span> | <span data-ttu-id="a830d-114">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="a830d-114">Language</span></span> | <span data-ttu-id="a830d-115">Versione</span><span class="sxs-lookup"><span data-stu-id="a830d-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="a830d-116">Modulo a</span><span class="sxs-lookup"><span data-stu-id="a830d-116">ModuleA</span></span>  | <span data-ttu-id="a830d-117">0</span><span class="sxs-lookup"><span data-stu-id="a830d-117">0</span></span>        | <span data-ttu-id="a830d-118">1.0</span><span class="sxs-lookup"><span data-stu-id="a830d-118">1.0</span></span>     |
| <span data-ttu-id="a830d-119">ModuleB</span><span class="sxs-lookup"><span data-stu-id="a830d-119">ModuleB</span></span>  | <span data-ttu-id="a830d-120">1033</span><span class="sxs-lookup"><span data-stu-id="a830d-120">1033</span></span>     | <span data-ttu-id="a830d-121">1.0</span><span class="sxs-lookup"><span data-stu-id="a830d-121">1.0</span></span>     |



 

[<span data-ttu-id="a830d-122">Tabella ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="a830d-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="a830d-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="a830d-123">ModuleID</span></span> | <span data-ttu-id="a830d-124">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="a830d-124">ModuleLanguage</span></span> | <span data-ttu-id="a830d-125">RequiredID</span><span class="sxs-lookup"><span data-stu-id="a830d-125">RequiredID</span></span> | <span data-ttu-id="a830d-126">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="a830d-126">RequiredLanguage</span></span> | <span data-ttu-id="a830d-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="a830d-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="a830d-128">Modulo a</span><span class="sxs-lookup"><span data-stu-id="a830d-128">ModuleA</span></span>  | <span data-ttu-id="a830d-129">0</span><span class="sxs-lookup"><span data-stu-id="a830d-129">0</span></span>              | <span data-ttu-id="a830d-130">ModuleX</span><span class="sxs-lookup"><span data-stu-id="a830d-130">ModuleX</span></span>    | <span data-ttu-id="a830d-131">0</span><span class="sxs-lookup"><span data-stu-id="a830d-131">0</span></span>                | <span data-ttu-id="a830d-132">2.0</span><span class="sxs-lookup"><span data-stu-id="a830d-132">2.0</span></span>             |



 

[<span data-ttu-id="a830d-133">Tabella ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="a830d-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="a830d-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="a830d-134">ModuleID</span></span> | <span data-ttu-id="a830d-135">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="a830d-135">ModuleLanguage</span></span> | <span data-ttu-id="a830d-136">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="a830d-136">ExcludedID</span></span> | <span data-ttu-id="a830d-137">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="a830d-137">ExcludedLanguage</span></span> | <span data-ttu-id="a830d-138">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="a830d-138">ExcludedMinVersion</span></span> | <span data-ttu-id="a830d-139">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="a830d-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="a830d-140">Modulo a</span><span class="sxs-lookup"><span data-stu-id="a830d-140">ModuleA</span></span>  | <span data-ttu-id="a830d-141">0</span><span class="sxs-lookup"><span data-stu-id="a830d-141">0</span></span>              | <span data-ttu-id="a830d-142">ModuleB</span><span class="sxs-lookup"><span data-stu-id="a830d-142">ModuleB</span></span>    | <span data-ttu-id="a830d-143">1033</span><span class="sxs-lookup"><span data-stu-id="a830d-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="a830d-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a830d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a830d-145">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="a830d-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




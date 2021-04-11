---
description: ICEM08 garantisce che un modulo non escluda un altro modulo da cui dipende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232447"
---
# <a name="icem08"></a><span data-ttu-id="a59b3-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="a59b3-103">ICEM08</span></span>

<span data-ttu-id="a59b3-104">ICEM08 garantisce che un modulo non escluda un altro modulo da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="a59b3-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="a59b3-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="a59b3-105">Result</span></span>

<span data-ttu-id="a59b3-106">ICEM08 Invia un errore quando un modulo esclude un altro modulo da cui dipende.</span><span class="sxs-lookup"><span data-stu-id="a59b3-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="a59b3-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="a59b3-107">Example</span></span>

<span data-ttu-id="a59b3-108">ICEM08 invia il messaggio di errore seguente per un modulo contenente le voci di database indicate nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="a59b3-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="a59b3-109">Tabella ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="a59b3-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="a59b3-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="a59b3-110">ModuleID</span></span>             | <span data-ttu-id="a59b3-111">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="a59b3-111">ModuleLanguage</span></span> | <span data-ttu-id="a59b3-112">RequiredID</span><span class="sxs-lookup"><span data-stu-id="a59b3-112">RequiredID</span></span>           | <span data-ttu-id="a59b3-113">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="a59b3-113">RequiredLanguage</span></span> | <span data-ttu-id="a59b3-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="a59b3-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="a59b3-115">Modulo a.<GUID></span><span class="sxs-lookup"><span data-stu-id="a59b3-115">ModuleA.<GUID></span></span> | <span data-ttu-id="a59b3-116">1033</span><span class="sxs-lookup"><span data-stu-id="a59b3-116">1033</span></span>           | <span data-ttu-id="a59b3-117">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="a59b3-117">ModuleB.<GUID></span></span> | <span data-ttu-id="a59b3-118">1033</span><span class="sxs-lookup"><span data-stu-id="a59b3-118">1033</span></span>             | <span data-ttu-id="a59b3-119">1.0</span><span class="sxs-lookup"><span data-stu-id="a59b3-119">1.0</span></span>             |



 

[<span data-ttu-id="a59b3-120">Tabella ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="a59b3-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="a59b3-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="a59b3-121">ModuleID</span></span>             | <span data-ttu-id="a59b3-122">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="a59b3-122">ModuleLanguage</span></span> | <span data-ttu-id="a59b3-123">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="a59b3-123">ExcludedID</span></span>           | <span data-ttu-id="a59b3-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="a59b3-124">ExcludedLanguage</span></span> | <span data-ttu-id="a59b3-125">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="a59b3-125">ExcludedMinVersion</span></span> | <span data-ttu-id="a59b3-126">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="a59b3-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="a59b3-127">Modulo a.<GUID></span><span class="sxs-lookup"><span data-stu-id="a59b3-127">ModuleA.<GUID></span></span> | <span data-ttu-id="a59b3-128">1033</span><span class="sxs-lookup"><span data-stu-id="a59b3-128">1033</span></span>           | <span data-ttu-id="a59b3-129">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="a59b3-129">ModuleB.<GUID></span></span> | <span data-ttu-id="a59b3-130">1033</span><span class="sxs-lookup"><span data-stu-id="a59b3-130">1033</span></span>             |                    | <span data-ttu-id="a59b3-131">1.0</span><span class="sxs-lookup"><span data-stu-id="a59b3-131">1.0</span></span>                |



 

<span data-ttu-id="a59b3-132">Per correggere l'errore, rimuovere la dipendenza o l'esclusione.</span><span class="sxs-lookup"><span data-stu-id="a59b3-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="a59b3-133">Se ModuleB è una dipendenza (RequiredID) di Modulea, non è possibile escluderla, come illustrato nella colonna ExludedID della tabella ModuleExclusion.</span><span class="sxs-lookup"><span data-stu-id="a59b3-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="a59b3-134">Se è necessario escludere ModuleB, è necessario rimuovere la dipendenza di Modulea su di essa.</span><span class="sxs-lookup"><span data-stu-id="a59b3-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a59b3-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a59b3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a59b3-136">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="a59b3-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 




---
description: ICE14 convalida la tabella delle funzionalità di un database Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346326"
---
# <a name="ice14"></a><span data-ttu-id="e804c-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="e804c-103">ICE14</span></span>

<span data-ttu-id="e804c-104">ICE14 convalida quanto segue per le funzionalità:</span><span class="sxs-lookup"><span data-stu-id="e804c-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="e804c-105">Per le funzionalità padre radice non è impostato il bit msidbFeatureAttributesFollowParent nella colonna Attributes della [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e804c-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="e804c-106">Una funzionalità radice non ha un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="e804c-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="e804c-107">Nessuna caratteristica ha la stessa voce nelle colonne padre feature e feature \_ della [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e804c-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="e804c-108">Nessuna funzionalità può essere il proprio padre.</span><span class="sxs-lookup"><span data-stu-id="e804c-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="e804c-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="e804c-109">Result</span></span>

<span data-ttu-id="e804c-110">ICE14 Invia un messaggio di errore se trova una funzionalità radice con il set di bit msidbFeatureAttributesFollowParent o una funzionalità con voci identiche nelle colonne padre feature e feature \_ della tabella Feature.</span><span class="sxs-lookup"><span data-stu-id="e804c-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="e804c-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="e804c-111">Example</span></span>

<span data-ttu-id="e804c-112">ICE14 restituirebbe gli errori seguenti per l'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="e804c-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="e804c-113">La funzionalità Sport presenta lo stesso valore nelle colonne padre feature e feature \_ della tabella file.</span><span class="sxs-lookup"><span data-stu-id="e804c-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="e804c-114">Per la funzionalità radice sport è impostato il bit msidbFeatureAttributesFollowParent.</span><span class="sxs-lookup"><span data-stu-id="e804c-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="e804c-115">Nell'albero delle funzionalità di questo esempio, sport è la funzionalità radice e un elemento padre delle funzionalità di nuoto e football.</span><span class="sxs-lookup"><span data-stu-id="e804c-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="e804c-116">Freestyle è una funzionalità figlio di swimming.</span><span class="sxs-lookup"><span data-stu-id="e804c-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="e804c-117">TouchFootball è una funzionalità figlio di football.</span><span class="sxs-lookup"><span data-stu-id="e804c-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="e804c-118">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e804c-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="e804c-119">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e804c-119">Feature</span></span>       | <span data-ttu-id="e804c-120">Attributi</span><span class="sxs-lookup"><span data-stu-id="e804c-120">Attributes</span></span> | <span data-ttu-id="e804c-121">\_Elemento padre della funzionalità</span><span class="sxs-lookup"><span data-stu-id="e804c-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="e804c-122">Sport</span><span class="sxs-lookup"><span data-stu-id="e804c-122">Sport</span></span>         | <span data-ttu-id="e804c-123">4</span><span class="sxs-lookup"><span data-stu-id="e804c-123">4</span></span>          | <span data-ttu-id="e804c-124">Sport</span><span class="sxs-lookup"><span data-stu-id="e804c-124">Sport</span></span>           |
| <span data-ttu-id="e804c-125">Swimming</span><span class="sxs-lookup"><span data-stu-id="e804c-125">Swimming</span></span>      | <span data-ttu-id="e804c-126">1</span><span class="sxs-lookup"><span data-stu-id="e804c-126">1</span></span>          | <span data-ttu-id="e804c-127">Sport</span><span class="sxs-lookup"><span data-stu-id="e804c-127">Sport</span></span>           |
| <span data-ttu-id="e804c-128">Calcio</span><span class="sxs-lookup"><span data-stu-id="e804c-128">Football</span></span>      | <span data-ttu-id="e804c-129">4</span><span class="sxs-lookup"><span data-stu-id="e804c-129">4</span></span>          | <span data-ttu-id="e804c-130">Sport</span><span class="sxs-lookup"><span data-stu-id="e804c-130">Sport</span></span>           |
| <span data-ttu-id="e804c-131">Freestyle</span><span class="sxs-lookup"><span data-stu-id="e804c-131">Freestyle</span></span>     | <span data-ttu-id="e804c-132">1</span><span class="sxs-lookup"><span data-stu-id="e804c-132">1</span></span>          | <span data-ttu-id="e804c-133">Swimming</span><span class="sxs-lookup"><span data-stu-id="e804c-133">Swimming</span></span>        |
| <span data-ttu-id="e804c-134">TouchFootball</span><span class="sxs-lookup"><span data-stu-id="e804c-134">TouchFootball</span></span> | <span data-ttu-id="e804c-135">4</span><span class="sxs-lookup"><span data-stu-id="e804c-135">4</span></span>          | <span data-ttu-id="e804c-136">Calcio</span><span class="sxs-lookup"><span data-stu-id="e804c-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e804c-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e804c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e804c-138">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e804c-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




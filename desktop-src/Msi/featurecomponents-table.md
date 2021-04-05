---
description: La tabella FeatureComponents definisce la relazione tra le funzionalità e i componenti. Per ogni funzionalità, in questa tabella sono elencati tutti i componenti che costituiscono tale funzionalità.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabella FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754226"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="062af-104">Tabella FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="062af-104">FeatureComponents Table</span></span>

<span data-ttu-id="062af-105">La tabella FeatureComponents definisce la relazione tra le funzionalità e i componenti.</span><span class="sxs-lookup"><span data-stu-id="062af-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="062af-106">Per ogni funzionalità, in questa tabella sono elencati tutti i componenti che costituiscono tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="062af-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="062af-107">La tabella FeatureComponents include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="062af-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="062af-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="062af-108">Column</span></span>      | <span data-ttu-id="062af-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="062af-109">Type</span></span>                         | <span data-ttu-id="062af-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="062af-110">Key</span></span> | <span data-ttu-id="062af-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="062af-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="062af-112">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="062af-112">Feature\_</span></span>   | [<span data-ttu-id="062af-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="062af-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="062af-114">S</span><span class="sxs-lookup"><span data-stu-id="062af-114">Y</span></span>   | <span data-ttu-id="062af-115">N</span><span class="sxs-lookup"><span data-stu-id="062af-115">N</span></span>        |
| <span data-ttu-id="062af-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="062af-116">Component\_</span></span> | [<span data-ttu-id="062af-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="062af-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="062af-118">S</span><span class="sxs-lookup"><span data-stu-id="062af-118">Y</span></span>   | <span data-ttu-id="062af-119">N</span><span class="sxs-lookup"><span data-stu-id="062af-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="062af-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="062af-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="062af-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="062af-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="062af-122">Chiave esterna nella prima colonna della [tabella](feature-table.md)delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="062af-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="062af-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="062af-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="062af-124">Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="062af-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="062af-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="062af-125">Remarks</span></span>

<span data-ttu-id="062af-126">È previsto un limite massimo di 1600 componenti per funzionalità.</span><span class="sxs-lookup"><span data-stu-id="062af-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="062af-127">I componenti possono essere condivisi da due o più funzionalità, ovvero lo stesso componente può essere definito da più di una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="062af-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="062af-128">Questa tabella viene definita quando viene eseguita l'azione [PublishFeatures](publishfeatures-action.md) o [UnpublishFeatures](unpublishfeatures-action.md) .</span><span class="sxs-lookup"><span data-stu-id="062af-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="062af-129">Convalida</span><span class="sxs-lookup"><span data-stu-id="062af-129">Validation</span></span>

<dl>

[<span data-ttu-id="062af-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="062af-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="062af-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="062af-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="062af-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="062af-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="062af-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="062af-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="062af-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="062af-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="062af-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="062af-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="062af-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="062af-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="062af-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="062af-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="062af-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="062af-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="062af-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="062af-139">ICE69</span></span>](ice69.md)  
</dl>

 

 




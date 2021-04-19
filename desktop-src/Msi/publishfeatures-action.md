---
description: L'azione PublishFeatures scrive lo stato di ogni funzionalità nel registro di sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Azione PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311729"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="ee24e-103">Azione PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="ee24e-103">PublishFeatures Action</span></span>

<span data-ttu-id="ee24e-104">L'azione PublishFeatures scrive lo stato di ogni funzionalità nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ee24e-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="ee24e-105">Lo stato della funzionalità può essere assente, pubblicizzato o installato.</span><span class="sxs-lookup"><span data-stu-id="ee24e-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="ee24e-106">L'azione PublishFeatures scrive anche il mapping del componente della funzionalità nel registro di sistema per ogni funzionalità installata.</span><span class="sxs-lookup"><span data-stu-id="ee24e-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="ee24e-107">L'azione PublishFeatures esegue una query sulla tabella [FeatureComponents](featurecomponents-table.md), la [tabella delle funzionalità](feature-table.md)e la [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee24e-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ee24e-108">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="ee24e-108">Sequence Restrictions</span></span>

<span data-ttu-id="ee24e-109">L'azione PublishFeatures deve essere precedente a [PublishProduct](publishproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="ee24e-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ee24e-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="ee24e-110">ActionData Messages</span></span>



| <span data-ttu-id="ee24e-111">Campo</span><span class="sxs-lookup"><span data-stu-id="ee24e-111">Field</span></span> | <span data-ttu-id="ee24e-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="ee24e-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="ee24e-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ee24e-113">\[1\]</span></span> | <span data-ttu-id="ee24e-114">Identificatore della funzionalità annunciata.</span><span class="sxs-lookup"><span data-stu-id="ee24e-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ee24e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee24e-115">Remarks</span></span>

<span data-ttu-id="ee24e-116">L'azione PublishFeatures pubblica la composizione di tutte le funzionalità selezionate per l'annuncio o l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ee24e-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 




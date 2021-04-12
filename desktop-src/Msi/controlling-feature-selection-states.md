---
description: È possibile controllare quali opzioni di installazione delle funzionalità sono disponibili per gli utenti e le applicazioni da selezionare creando la tabella delle funzionalità e la tabella dei componenti.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controllo degli Stati di selezione delle funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233708"
---
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="cddb2-103">Controllo degli Stati di selezione delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="cddb2-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="cddb2-104">È possibile controllare quali opzioni di installazione delle funzionalità sono disponibili per gli utenti e le applicazioni da selezionare creando la [tabella delle funzionalità](feature-table.md) e la [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="cddb2-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="cddb2-105">Per evitare la selezione dello stato di annuncio per una funzionalità, includere **msidbFeatureAttributesDisallowAdvertise** nel campo attributi della funzionalità della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cddb2-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="cddb2-106">Per evitare la selezione degli Stati di esecuzione dall'origine o della rete per una funzionalità, includere **msidbComponentAttributesLocalOnly** nei campi degli attributi della [tabella dei componenti](component-table.md) per ogni componente appartenente alla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cddb2-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="cddb2-107">Se una funzionalità non dispone di componenti, per la funzionalità sono sempre disponibili le opzioni Esegui da origine e esecuzione da computer.</span><span class="sxs-lookup"><span data-stu-id="cddb2-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="cddb2-108">Per evitare la selezione dello stato di esecuzione dal computer per una funzionalità, includere **msidbComponentAttributesSourceOnly** nei campi degli attributi della [tabella dei componenti](component-table.md) per ogni componente appartenente alla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cddb2-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="cddb2-109">Se una funzionalità non dispone di componenti, per la funzionalità sono sempre disponibili le opzioni Esegui da origine e esecuzione da computer.</span><span class="sxs-lookup"><span data-stu-id="cddb2-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="cddb2-110">È possibile creare nuove funzionalità figlio includendo **msidbFeatureAttributesFollowParent** e **MsidbFeatureAttributesUIDisallowAbsent** nel campo Attributes della [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="cddb2-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 




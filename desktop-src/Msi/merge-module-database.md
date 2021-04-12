---
description: Il database di un modulo merge contiene tutte le proprietà di installazione e la logica di installazione per il modulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Database del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347156"
---
# <a name="merge-module-database"></a><span data-ttu-id="ad497-103">Database del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ad497-103">Merge Module Database</span></span>

<span data-ttu-id="ad497-104">Il database di un modulo merge contiene tutte le proprietà di installazione e la logica di installazione per il modulo.</span><span class="sxs-lookup"><span data-stu-id="ad497-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="ad497-105">Si tratta essenzialmente di un [database di installazione](installer-database.md) semplificato o di un file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="ad497-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="ad497-106">I file di database del modulo merge standard sono indicati da un'estensione MSM.</span><span class="sxs-lookup"><span data-stu-id="ad497-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="ad497-107">Per un elenco di tutte le tabelle di database che possono esistere nei moduli merge, vedere [Merge Module Database Tables](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ad497-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="ad497-108">Nel database di ogni file con estensione MSM sono necessarie le tabelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad497-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="ad497-109">Componente</span><span class="sxs-lookup"><span data-stu-id="ad497-109">Component</span></span>](component-table.md)

[<span data-ttu-id="ad497-110">Directory</span><span class="sxs-lookup"><span data-stu-id="ad497-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="ad497-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="ad497-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="ad497-112">File</span><span class="sxs-lookup"><span data-stu-id="ad497-112">File</span></span>](file-table.md)

[<span data-ttu-id="ad497-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="ad497-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="ad497-114">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="ad497-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="ad497-115">Si noti che le tabelle Component, directory, FeatureComponents e file sono presenti anche in tutti i file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="ad497-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="ad497-116">Un database del modulo merge non contiene una [tabella delle funzionalità](feature-table.md) e pertanto non è possibile installare il file con estensione MSM da solo.</span><span class="sxs-lookup"><span data-stu-id="ad497-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="ad497-117">Per installare un modulo merge, è necessario innanzitutto eseguirne il merge utilizzando uno strumento di merge in un file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="ad497-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="ad497-118">La [tabella ModuleSignature](modulesignature-table.md) è presente solo nei file con estensione msi di cui è stato eseguito il merge con almeno un file. msm.</span><span class="sxs-lookup"><span data-stu-id="ad497-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="ad497-119">Se questa tabella è presente in un file con estensione msi, contiene un record per ogni modulo merge precedentemente Unito al database di installazione.</span><span class="sxs-lookup"><span data-stu-id="ad497-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="ad497-120">I moduli merge possono contenere tabelle di sequenza MergeModule facoltative.</span><span class="sxs-lookup"><span data-stu-id="ad497-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="ad497-121">Queste tabelle si verificano solo nei file con estensione MSM.</span><span class="sxs-lookup"><span data-stu-id="ad497-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="ad497-122">Quando i file con estensione MSM vengono uniti in un file con estensione msi, queste tabelle modificano le [*tabelle di sequenza*](s-gly.md) delle azioni del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="ad497-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="ad497-123">I moduli merge possono contenere tabelle personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ad497-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="ad497-124">Queste tabelle vengono utilizzate da [azioni personalizzate](custom-actions.md) definite nel modulo unione.</span><span class="sxs-lookup"><span data-stu-id="ad497-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="ad497-125">I moduli merge richiedono raramente tabelle dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ad497-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="ad497-126">Queste tabelle devono essere presenti solo in rari casi in cui il modulo merge richiede l'input dell'utente durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ad497-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="ad497-127">Per ulteriori informazioni, vedere [creazione di interfacce utente nei moduli unione](authoring-user-interfaces-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ad497-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 




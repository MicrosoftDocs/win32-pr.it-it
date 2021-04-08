---
description: Ogni elemento in una raccolta espone le proprietà.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Modifica di proprietà nel catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748274"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="1b099-103">Modifica di proprietà nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="1b099-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="1b099-104">Ogni elemento in una raccolta espone le proprietà.</span><span class="sxs-lookup"><span data-stu-id="1b099-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="1b099-105">Queste proprietà consentono di conservare i dati di configurazione per qualsiasi elemento rappresentato dall'elemento.</span><span class="sxs-lookup"><span data-stu-id="1b099-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="1b099-106">Nello strumento di amministrazione Servizi componenti, queste proprietà vengono visualizzate in una pagina delle proprietà a cui si accede facendo clic con il pulsante destro del mouse su un elemento in una cartella.</span><span class="sxs-lookup"><span data-stu-id="1b099-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="1b099-107">Poiché gli elementi di una raccolta specifica rappresentano tutti lo stesso tipo di elemento, tali elementi espongono un set di proprietà coerenti nell'intera raccolta.</span><span class="sxs-lookup"><span data-stu-id="1b099-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="1b099-108">La raccolta [**Applications**](applications.md) , ad esempio, espone una proprietà Name, una proprietà AppID e così via.</span><span class="sxs-lookup"><span data-stu-id="1b099-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="1b099-109">Questo è analogo al modo in cui per ogni applicazione nello strumento di amministrazione Servizi componenti è disponibile una pagina delle proprietà strutturata in modo coerente.</span><span class="sxs-lookup"><span data-stu-id="1b099-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="1b099-110">Per un elenco delle proprietà disponibili per la raccolta di **applicazioni** , vedere **Applications (applicazioni**).</span><span class="sxs-lookup"><span data-stu-id="1b099-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="1b099-111">Per un elenco delle proprietà disponibili per la raccolta [**Components**](components.md) , vedere **Components**.</span><span class="sxs-lookup"><span data-stu-id="1b099-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="1b099-112">Per un elenco completo delle proprietà esposte da elementi in ogni raccolta, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="1b099-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="1b099-113">Rappresenta un elemento in una raccolta usando un oggetto creato dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="1b099-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="1b099-114">Questo oggetto consente di impostare e ottenere le proprietà esposte dall'elemento.</span><span class="sxs-lookup"><span data-stu-id="1b099-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="1b099-115">Quando si impostano le proprietà, è anche possibile che si stia tendendo con un altro writer al catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="1b099-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="1b099-116">Per ulteriori informazioni, vedere [recupero e impostazione delle proprietà](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1b099-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="1b099-117">Dopo aver impostato le proprietà, non viene eseguito il commit delle modifiche fino a quando non si salvano in modo esplicito le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1b099-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="1b099-118">Per ulteriori informazioni, vedere [salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="1b099-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="1b099-119">Quando si salvano le modifiche, il catalogo COM+ applica una logica di configurazione per assicurarsi di non impostare elementi su configurazioni incompatibili.</span><span class="sxs-lookup"><span data-stu-id="1b099-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="1b099-120">Modifica anche alcune proprietà quando si modificano in modo esplicito determinate altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="1b099-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="1b099-121">Per ulteriori informazioni, vedere [interdipendenze tra proprietà](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1b099-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="1b099-122">COM+ dispone inoltre di una funzionalità che consente di eseguire query in modo dinamico per vedere quali proprietà sono disponibili per gli elementi di una raccolta specifica.</span><span class="sxs-lookup"><span data-stu-id="1b099-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="1b099-123">Per informazioni dettagliate, vedere [esecuzione di query per le proprietà disponibili](querying-for-available-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1b099-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b099-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b099-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b099-125">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="1b099-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="1b099-126">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="1b099-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="1b099-127">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="1b099-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="1b099-128">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="1b099-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="1b099-129">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="1b099-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 




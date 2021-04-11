---
description: COM+ fornisce un modello a oggetti di amministrazione che espone tutte le funzionalità dello strumento di amministrazione Servizi componenti, ovvero un front-end grafico scritto sopra gli oggetti amministrativi.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automazione dell'amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127163"
---
# <a name="automating-com-administration"></a><span data-ttu-id="e9044-103">Automazione dell'amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e9044-103">Automating COM+ Administration</span></span>

<span data-ttu-id="e9044-104">COM+ fornisce un modello a oggetti di amministrazione che espone tutte le funzionalità dello strumento di amministrazione Servizi componenti, ovvero un front-end grafico scritto sopra gli oggetti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="e9044-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="e9044-105">È possibile utilizzare questi oggetti, forniti dalla libreria di amministrazione di Servizi componenti (COMAdmin), per automatizzare tutte le attività nell'amministrazione di applicazioni e servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="e9044-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="e9044-106">Gli oggetti COMAdmin consentono di leggere e scrivere le informazioni archiviate nel catalogo COM+, l'archivio dati sottostante che include tutti i dati di configurazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e9044-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="e9044-107">È possibile utilizzare questi oggetti per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9044-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="e9044-108">Creazione e configurazione di applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="e9044-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="e9044-109">Installare ed esportare applicazioni COM+ esistenti.</span><span class="sxs-lookup"><span data-stu-id="e9044-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="e9044-110">Gestire le applicazioni COM+ installate.</span><span class="sxs-lookup"><span data-stu-id="e9044-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="e9044-111">Gestire e configurare i servizi.</span><span class="sxs-lookup"><span data-stu-id="e9044-111">Manage and configure services.</span></span>
-   <span data-ttu-id="e9044-112">Amministrare in remoto i servizi componenti in un computer diverso.</span><span class="sxs-lookup"><span data-stu-id="e9044-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="e9044-113">È possibile utilizzare gli oggetti COMAdmin consentiti tramite script con qualsiasi linguaggio compatibile con l'automazione, ad esempio Microsoft Visual Basic e Visual Basic script.</span><span class="sxs-lookup"><span data-stu-id="e9044-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="e9044-114">È possibile sviluppare script leggeri o strumenti di amministrazione per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="e9044-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="e9044-115">Ad esempio, è possibile eseguire quanto le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9044-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="e9044-116">Scrivere script per eseguire attività amministrative di routine.</span><span class="sxs-lookup"><span data-stu-id="e9044-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="e9044-117">Scrivere script per automatizzare i processi nello sviluppo di applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="e9044-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="e9044-118">Sviluppare strumenti generici per l'amministrazione e il monitoraggio di Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="e9044-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="e9044-119">Sviluppare eseguibili di installazione per installare e distribuire l'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="e9044-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="e9044-120">La libreria COMAdmin fornisce la compatibilità con le versioni precedenti della libreria di amministrazione MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="e9044-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="e9044-121">La maggior parte del codice di amministrazione MTS 2,0 esistente continuerà a funzionare, anche se con alcune eccezioni.</span><span class="sxs-lookup"><span data-stu-id="e9044-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="e9044-122">Vedere la pagina relativa alla [libreria di amministrazione MTS](mts-administration-library.md).</span><span class="sxs-lookup"><span data-stu-id="e9044-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="e9044-123">Per automatizzare l'amministrazione, è necessario avere familiarità con le attività amministrative eseguite con lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="e9044-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="e9044-124">Per una descrizione completa degli oggetti COMAdmin e delle interfacce corrispondenti, vedere la documentazione di riferimento COM+ per le classi e le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9044-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="e9044-125">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="e9044-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="e9044-126">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="e9044-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="e9044-127">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="e9044-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="e9044-128">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="e9044-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="e9044-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="e9044-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="e9044-130">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="e9044-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="e9044-131">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="e9044-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="e9044-132">Negli argomenti seguenti di questa sezione viene fornita una panoramica per l'automazione dell'amministrazione utilizzando gli oggetti COMAdmin:</span><span class="sxs-lookup"><span data-stu-id="e9044-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="e9044-133">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="e9044-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="e9044-134">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="e9044-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="e9044-135">Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="e9044-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="e9044-136">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e9044-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="e9044-137">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="e9044-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="e9044-138">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e9044-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 




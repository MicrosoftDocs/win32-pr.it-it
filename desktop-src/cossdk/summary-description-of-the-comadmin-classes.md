---
description: La libreria COMAdmin (comadmin.dll) fornisce tre classi, ciascuna delle quali implementa un'interfaccia COM duale.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descrizione riepilogativa delle classi COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304727"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="800bd-103">Descrizione riepilogativa delle classi COMAdmin</span><span class="sxs-lookup"><span data-stu-id="800bd-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="800bd-104">La libreria COMAdmin (comadmin.dll) fornisce tre classi, ciascuna delle quali implementa un'interfaccia COM duale.</span><span class="sxs-lookup"><span data-stu-id="800bd-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="800bd-105">Gli oggetti creati da queste classi vengono utilizzati per ottenere l'accesso al catalogo, per rappresentare le raccolte nel catalogo e per rappresentare gli elementi contenuti nelle raccolte.</span><span class="sxs-lookup"><span data-stu-id="800bd-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="800bd-106">COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="800bd-106">COMAdminCatalog</span></span>

<span data-ttu-id="800bd-107">La classe [**COMAdminCatalog**](comadmincatalog.md) rappresenta il catalogo stesso.</span><span class="sxs-lookup"><span data-stu-id="800bd-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="800bd-108">Un oggetto creato da **COMAdminCatalog** è l'oggetto fondamentale usato nell'amministrazione a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="800bd-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="800bd-109">Oltre a stabilire la connessione di base al server di catalogo quando ne viene creata un'istanza, **COMAdminCatalog** fornisce metodi che consentono di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="800bd-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="800bd-110">Ottiene le raccolte nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="800bd-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="800bd-111">Connettersi al server di catalogo in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="800bd-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="800bd-112">Installare, esportare, avviare, arrestare e ottenere informazioni sulle applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="800bd-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="800bd-113">Installare i componenti in applicazioni COM+ e ottenere informazioni relative ai componenti.</span><span class="sxs-lookup"><span data-stu-id="800bd-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="800bd-114">Avviare, arrestare o aggiornare i servizi in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="800bd-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="800bd-115">Aggiornare, ripristinare o eseguire il backup delle informazioni del catalogo.</span><span class="sxs-lookup"><span data-stu-id="800bd-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="800bd-116">In COM+ 1,0, la classe [**COMAdminCatalog**](comadmincatalog.md) implementa l'interfaccia [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="800bd-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="800bd-117">In COM+ 1,5, la classe **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) come interfaccia predefinita.</span><span class="sxs-lookup"><span data-stu-id="800bd-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="800bd-118">COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="800bd-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="800bd-119">La classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) rappresenta qualsiasi raccolta nel catalogo, fornendo una stringa che assegna un nome alla raccolta specifica in fase di creazione dell'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="800bd-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="800bd-120">Le raccolte di cataloghi disponibili sono denominate nella tabella in [raccolte di amministrazione com+](com--administration-collections.md). Gli oggetti vengono creati da questa classe durante il recupero di una raccolta di livello superiore chiamando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) dell'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="800bd-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="800bd-121">Questi oggetti vengono creati anche quando si recupera una raccolta figlio chiamando il metodo **GetCollection** dell'oggetto raccolta padre.</span><span class="sxs-lookup"><span data-stu-id="800bd-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="800bd-122">Gli oggetti **COMAdminCatalogCollection** consentono di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="800bd-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="800bd-123">Enumerare gli elementi contenuti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="800bd-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="800bd-124">Recuperare un elemento dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="800bd-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="800bd-125">Aggiungere o rimuovere elementi da o verso la raccolta.</span><span class="sxs-lookup"><span data-stu-id="800bd-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="800bd-126">Salvare o rimuovere tutte le modifiche in sospeso apportate alla raccolta o agli elementi in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="800bd-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="800bd-127">Ottenere una raccolta diversa nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="800bd-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="800bd-128">La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa l'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .</span><span class="sxs-lookup"><span data-stu-id="800bd-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="800bd-129">COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="800bd-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="800bd-130">La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) rappresenta qualsiasi elemento contenuto in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="800bd-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="800bd-131">Gli oggetti vengono creati da questa classe quando si recupera un elemento tramite la proprietà [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) di un oggetto della raccolta di cataloghi.</span><span class="sxs-lookup"><span data-stu-id="800bd-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="800bd-132">Gli oggetti creati dalla classe **COMAdminCatalogObject** consentono di eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="800bd-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="800bd-133">Ottiene o imposta le proprietà supportate dall'elemento che l'oggetto viene utilizzato per rappresentare.</span><span class="sxs-lookup"><span data-stu-id="800bd-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="800bd-134">Ottenere informazioni sull'elemento e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="800bd-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="800bd-135">La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa l'interfaccia [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="800bd-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="800bd-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="800bd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="800bd-137">Accesso al catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="800bd-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="800bd-138">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="800bd-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 




---
title: Architettura di Download Manager
description: Architettura di Download Manager
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- architettura per Download Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708560"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="7881f-110">Architettura di Download Manager</span><span class="sxs-lookup"><span data-stu-id="7881f-110">Download Manager Architecture</span></span>

<span data-ttu-id="7881f-111">Gestione download di Windows Media Player utilizza la tecnologia COM.</span><span class="sxs-lookup"><span data-stu-id="7881f-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="7881f-112">La funzionalità è distillata in un set di interfacce di programmazione; è possibile scrivere codice di programmazione che utilizza queste interfacce utilizzando Microsoft JScript o C++.</span><span class="sxs-lookup"><span data-stu-id="7881f-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="7881f-113">I linguaggi di scripting utilizzano il concetto di oggetti per dividere la funzionalità di programmazione.</span><span class="sxs-lookup"><span data-stu-id="7881f-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="7881f-114">Il modello a oggetti **downloadmanager** utilizza diversi oggetti per dividere i metodi e le proprietà in un'organizzazione logica che raggruppa le funzioni semanticamente correlate.</span><span class="sxs-lookup"><span data-stu-id="7881f-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="7881f-115">Le sezioni seguenti contengono informazioni sugli oggetti di Download Manager.</span><span class="sxs-lookup"><span data-stu-id="7881f-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="7881f-116">Sezione</span><span class="sxs-lookup"><span data-stu-id="7881f-116">Section</span></span>                                                                     | <span data-ttu-id="7881f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7881f-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7881f-118">Informazioni sull'oggetto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="7881f-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="7881f-119">L'oggetto **downloadmanager** rappresenta l'oggetto radice per gestione download di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7881f-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="7881f-120">Informazioni sull'oggetto DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="7881f-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="7881f-121">L'oggetto **DownloadCollection** rappresenta una raccolta di elementi di download.</span><span class="sxs-lookup"><span data-stu-id="7881f-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="7881f-122">Informazioni sull'oggetto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="7881f-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="7881f-123">L'oggetto **DownloadItem** rappresenta una singola richiesta di download.</span><span class="sxs-lookup"><span data-stu-id="7881f-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="7881f-124">Informazioni sull'oggetto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="7881f-124">About the DownloadManager Object</span></span>

<span data-ttu-id="7881f-125">**Downloadmanager** è l'oggetto radice per gestione download di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7881f-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="7881f-126">Tutti gli altri oggetti sono accessibili tramite questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7881f-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="7881f-127">Per ottenere l'accesso all'oggetto **downloadmanager** , usare la sintassi JScript seguente:</span><span class="sxs-lookup"><span data-stu-id="7881f-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="7881f-128">In questo modo viene creata un'istanza dell'oggetto **downloadmanager** , che può quindi essere utilizzata per recuperare gli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="7881f-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="7881f-129">La sintassi seguente, ad esempio, recupera il primo elemento dalla raccolta di download con ID numero 253675:</span><span class="sxs-lookup"><span data-stu-id="7881f-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="7881f-130">Informazioni sull'oggetto DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="7881f-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="7881f-131">L'oggetto **DownloadCollection** rappresenta una raccolta di file da scaricare.</span><span class="sxs-lookup"><span data-stu-id="7881f-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="7881f-132">È possibile utilizzare questo oggetto per determinare il numero di download nella raccolta, rimuovere gli elementi dalla raccolta, recuperare un elemento di download specifico e avviare un nuovo download.</span><span class="sxs-lookup"><span data-stu-id="7881f-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="7881f-133">Quando si avvia un nuovo download, il download viene aggiunto automaticamente alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="7881f-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="7881f-134">Informazioni sull'oggetto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="7881f-134">About the DownloadItem Object</span></span>

<span data-ttu-id="7881f-135">L'oggetto **DownloadItem** rappresenta un singolo download.</span><span class="sxs-lookup"><span data-stu-id="7881f-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="7881f-136">Gli elementi di download sono sempre presenti come parte di una raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="7881f-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="7881f-137">Utilizzare questo oggetto per recuperare informazioni sull'elemento di download e per sospendere, riprendere o annullare il download in corso.</span><span class="sxs-lookup"><span data-stu-id="7881f-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="7881f-138">Quando si annulla un download, l'elemento di download rimane sul posto nella relativa raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="7881f-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="7881f-139">In questo caso, **scaricarecollection**. **downloadState** recupera un valore pari a 4, ovvero annullato.</span><span class="sxs-lookup"><span data-stu-id="7881f-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="7881f-140">È possibile usare **downloadItem**. stato di **avanzamento** per informare l'utente sulla quantità di file trasferiti o su quanto resta da scaricare.</span><span class="sxs-lookup"><span data-stu-id="7881f-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="7881f-141">È possibile utilizzare questo valore per stimare anche il tempo rimanente.</span><span class="sxs-lookup"><span data-stu-id="7881f-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7881f-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7881f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7881f-143">**Gestione download**</span><span class="sxs-lookup"><span data-stu-id="7881f-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 





---
description: In questa sezione vengono fornite le informazioni concettuali necessarie per l'implementazione, l'estensione e il test dei gestori del protocollo.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Sviluppo di gestori di protocollo per Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750426"
---
# <a name="developing-protocol-handlers-for-windows-search"></a><span data-ttu-id="c0d56-103">Sviluppo di gestori di protocollo per Windows Search</span><span class="sxs-lookup"><span data-stu-id="c0d56-103">Developing Protocol Handlers for Windows Search</span></span>

<span data-ttu-id="c0d56-104">In questa sezione vengono fornite le informazioni concettuali necessarie per l'implementazione, l'estensione e il test dei gestori del protocollo.</span><span class="sxs-lookup"><span data-stu-id="c0d56-104">This section provides conceptual information necessary for the implementation, extension and testing of protocol handlers.</span></span>

-   [<span data-ttu-id="c0d56-105">Informazioni sui gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="c0d56-105">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
-   [<span data-ttu-id="c0d56-106">Notifica dell'indice delle modifiche</span><span class="sxs-lookup"><span data-stu-id="c0d56-106">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
-   [<span data-ttu-id="c0d56-107">Aggiunta di icone e menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="c0d56-107">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
-   [<span data-ttu-id="c0d56-108">Esempio di codice: estensioni della Shell per i gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="c0d56-108">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
-   [<span data-ttu-id="c0d56-109">Installazione e registrazione di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="c0d56-109">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
-   [<span data-ttu-id="c0d56-110">Creazione di un connettore di ricerca per un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="c0d56-110">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
-   [<span data-ttu-id="c0d56-111">Debug di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="c0d56-111">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a><span data-ttu-id="c0d56-112">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="c0d56-112">Additional Resources</span></span>

<span data-ttu-id="c0d56-113">Per informazioni concettuali sull'indicizzazione, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0d56-113">For conceptual background on indexing, see the following topics:</span></span>

-   <span data-ttu-id="c0d56-114">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0d56-114">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="c0d56-115">Per estendere la ricerca di Windows in modo da indicizzare il contenuto e le proprietà dei nuovi formati di file e degli archivi dati, vedere [estensione dell'indice](-search-3x-wds-extidx-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0d56-115">To extend Windows Search to index the contents and properties of new file formats and data stores, see [Extending the Index](-search-3x-wds-extidx-overview.md).</span></span>
-   <span data-ttu-id="c0d56-116">Per panoramiche su Catalog Manager e Catalog Search Manager (CSM), vedere [using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [using the Crawl scope Manager](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="c0d56-116">For overviews of the Catalog Manager and Catalog Search Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

<span data-ttu-id="c0d56-117">Per informazioni concettuali sui tipi di file e sui gestori, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0d56-117">For conceptual background on file types and handlers, see the following topics:</span></span>

-   <span data-ttu-id="c0d56-118">Per estendere la shell con i gestori di tipi di file, vedere [creazione di gestori di estensioni della shell](../shell/handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c0d56-118">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](../shell/handlers.md).</span></span>
-   <span data-ttu-id="c0d56-119">Per informazioni concettuali sui gestori di filtri, vedere [sviluppo di gestori di filtri](-search-ifilter-conceptual.md).</span><span class="sxs-lookup"><span data-stu-id="c0d56-119">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>
-   <span data-ttu-id="c0d56-120">Per informazioni sulla creazione di gestori, vedere [Introduzione alle associazioni di file](../shell/fa-intro.md), [registrazione delle estensioni della shell](../shell/reg-shell-exts.md), creazione di gestori di estensioni della [Shell](../shell/handlers.md), [menu di scelta rapida](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [gestori di anteprime](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c0d56-120">For information about creating handlers, see [Introduction to File Associations](../shell/fa-intro.md), [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [Preview Handlers](../shell/preview-handlers.md).</span></span>

<span data-ttu-id="c0d56-121">Per informazioni di base sulle tecnologie correlate e sull'implementazione di un archivio dati, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0d56-121">For background on related technologies and on implementing a data store, see the following topics:</span></span>

-   <span data-ttu-id="c0d56-122">I gestori del protocollo di ricerca di Windows utilizzano specifiche di progettazione simili a quelle di SharePoint Server e spesso possono essere utilizzati in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="c0d56-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="c0d56-123">Per ulteriori informazioni, vedere il [centro per sviluppatori di SharePoint Server](https://developer.microsoft.com/office/docs).</span><span class="sxs-lookup"><span data-stu-id="c0d56-123">For more information, see [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span></span>
-   <span data-ttu-id="c0d56-124">In Windows 7 e versioni successive, il server di ricerca di SharePoint 2008 e MOSS 2007 SP2 supportano anche la ricerca federata.</span><span class="sxs-lookup"><span data-stu-id="c0d56-124">In Windows 7 and later, SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search.</span></span> <span data-ttu-id="c0d56-125">Per ulteriori informazioni sulla distribuzione di ricerca federata e server di ricerca 2008 con Office SharePoint Server 2007, vedere la pagina relativa al [ \[ server di ricerca federativo 2008 \] ](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="c0d56-125">For more information about federated search and Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>
-   <span data-ttu-id="c0d56-126">Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0d56-126">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="c0d56-127">Per esempi di codice, vedere le pagine seguenti del portale:</span><span class="sxs-lookup"><span data-stu-id="c0d56-127">For code samples, see the following portal pages:</span></span>

-   <span data-ttu-id="c0d56-128">Per gli esempi di codice di ricerca, vedere [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="c0d56-128">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="c0d56-129">Per esempi di codice della shell, vedere [esempi di Shell SDK](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0d56-129">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

 

 

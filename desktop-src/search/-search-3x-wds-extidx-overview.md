---
description: È possibile estendere Windows Search per indicizzare il contenuto e le proprietà dei nuovi formati di file e gli archivi dati usando le interfacce dei componenti aggiuntivi.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Estensione dell'indice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306188"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="3a3be-103">Estensione dell'indice (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="3a3be-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="3a3be-104">È possibile estendere Windows Search per indicizzare il contenuto e le proprietà dei nuovi formati di file e gli archivi dati usando le [interfacce dei componenti](./-search-data-addins-interfaces-entry-page.md)aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3a3be-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="3a3be-105">Per creare componenti aggiuntivi di Windows Search, gli sviluppatori di terze parti devono implementare prima di tutto un archivio dati della shell, quindi sviluppare un gestore di protocollo in modo che Windows Search possa accedere ai dati per l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a3be-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="3a3be-106">Se si dispone di un formato di file personalizzato, è necessario sviluppare un gestore di filtro per indicizzare il contenuto del file e un gestore di proprietà per ogni tipo di file per indicizzare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a3be-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="3a3be-107">Windows Search supporta attualmente l'indicizzazione di più di 200 tipi di elementi (ad esempio, i formati di file con estensione txt, HTML e XML) e può funzionare con più tipi di archivi dati (ad esempio NTFS file system e Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="3a3be-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="3a3be-108">Windows Search usa la tecnologia di filtro e gestore di protocollo simile a SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="3a3be-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="3a3be-109">Di conseguenza, se si dispone già di implementazioni per il formato di file, è possibile aggiornare le implementazioni da inizializzare con un flusso usando [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) in modo che il filtro funzioni con la ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="3a3be-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="3a3be-110">I gestori di filtri, i gestori di proprietà e i gestori di protocollo devono essere scritti in codice nativo.</span><span class="sxs-lookup"><span data-stu-id="3a3be-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="3a3be-111">Ciò è dovuto a potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo di esecuzione di più componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3a3be-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="3a3be-112">Questa sezione sull'estensione dell'indice con componenti aggiuntivi contiene gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a3be-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="3a3be-113">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="3a3be-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="3a3be-114">Sviluppo di gestori di proprietà per Windows Search</span><span class="sxs-lookup"><span data-stu-id="3a3be-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="3a3be-115">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="3a3be-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="3a3be-116">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3a3be-116">Additional Resources</span></span>

<span data-ttu-id="3a3be-117">Per esempi di codice correlati, vedere [esempi di codice di Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="3a3be-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a3be-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a3be-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3be-119">Guida allo sviluppo di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3a3be-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="3a3be-120">Gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="3a3be-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3a3be-121">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="3a3be-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3a3be-122">Estensione delle risorse della lingua</span><span class="sxs-lookup"><span data-stu-id="3a3be-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 

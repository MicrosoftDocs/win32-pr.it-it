---
description: Nell'esempio di codice CrawlScopeCommandLine viene illustrato come definire le opzioni della riga di comando per le operazioni di indicizzazione di gestione dell'ambito di ricerca (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306148"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="ce554-103">CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="ce554-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="ce554-104">Nell'esempio di codice CrawlScopeCommandLine viene illustrato come definire le opzioni della riga di comando per le operazioni di indicizzazione di gestione dell'ambito di ricerca (CSM).</span><span class="sxs-lookup"><span data-stu-id="ce554-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="ce554-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce554-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="ce554-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce554-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="ce554-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ce554-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="ce554-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ce554-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="ce554-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ce554-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="ce554-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce554-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="ce554-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce554-111">Requirements</span></span>

| <span data-ttu-id="ce554-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ce554-112">Product</span></span>     | <span data-ttu-id="ce554-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="ce554-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="ce554-114">Windows</span><span class="sxs-lookup"><span data-stu-id="ce554-114">Windows</span></span>     | <span data-ttu-id="ce554-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="ce554-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="ce554-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ce554-116">Windows SDK</span></span> | <span data-ttu-id="ce554-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ce554-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="ce554-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ce554-118">Downloading the Sample</span></span>

<span data-ttu-id="ce554-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="ce554-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="ce554-120">Location</span><span class="sxs-lookup"><span data-stu-id="ce554-120">Location</span></span> | <span data-ttu-id="ce554-121">Percorso o URL</span><span class="sxs-lookup"><span data-stu-id="ce554-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="ce554-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="ce554-122">GitHub</span></span>   |    [<span data-ttu-id="ce554-123">Esempio CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="ce554-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="ce554-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ce554-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="ce554-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ce554-125">Building the Sample</span></span>

1. <span data-ttu-id="ce554-126">Aprire Esplora risorse e passare alla directory del progetto **CrawlScopeCommandLine** .</span><span class="sxs-lookup"><span data-stu-id="ce554-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="ce554-127">Fare doppio clic sull'icona per il file csmcmd. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ce554-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="ce554-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="ce554-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="ce554-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ce554-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="ce554-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="ce554-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ce554-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ce554-131">Running the Sample</span></span>

1. <span data-ttu-id="ce554-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="ce554-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="ce554-133">Al prompt dei comandi, immettere `csmcmd.exe` o da Esplora risorse, fare doppio clic sull'icona per csmcmd.exe.</span><span class="sxs-lookup"><span data-stu-id="ce554-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce554-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce554-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="ce554-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ce554-135">Reference</span></span>

[<span data-ttu-id="ce554-136">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="ce554-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="ce554-137">**IEnumSearchScopeRules**</span><span class="sxs-lookup"><span data-stu-id="ce554-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="ce554-138">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="ce554-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="ce554-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="ce554-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="ce554-140">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="ce554-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="ce554-141">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="ce554-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="ce554-142">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="ce554-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="ce554-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="ce554-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="ce554-144">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="ce554-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="ce554-145">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="ce554-145">Other Samples</span></span>

[<span data-ttu-id="ce554-146">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="ce554-146">Search Code Samples</span></span>](-search-samples-ovw.md)

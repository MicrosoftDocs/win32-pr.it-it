---
description: "Nell'esempio di codice ReindexMatchingUrls viene illustrato come fornire tre modi per specificare i file da reindicizzare: URL che corrispondono a un tipo di file, a un tipo MIME o a una clausola WHERE specificata."
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484420"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="bf962-103">ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="bf962-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="bf962-104">Nell'esempio di codice ReindexMatchingUrls viene illustrato come fornire tre modi per specificare i file da reindicizzare: URL che corrispondono a un tipo di file, a un tipo MIME o a una clausola WHERE specificata.</span><span class="sxs-lookup"><span data-stu-id="bf962-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="bf962-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf962-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="bf962-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf962-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="bf962-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bf962-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="bf962-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bf962-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="bf962-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bf962-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="bf962-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf962-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="bf962-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf962-111">Requirements</span></span>

| <span data-ttu-id="bf962-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bf962-112">Product</span></span>     | <span data-ttu-id="bf962-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="bf962-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="bf962-114">Windows</span><span class="sxs-lookup"><span data-stu-id="bf962-114">Windows</span></span>     | <span data-ttu-id="bf962-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="bf962-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="bf962-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bf962-116">Windows SDK</span></span> | <span data-ttu-id="bf962-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bf962-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="bf962-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bf962-118">Downloading the Sample</span></span>

<span data-ttu-id="bf962-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="bf962-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="bf962-120">Location</span><span class="sxs-lookup"><span data-stu-id="bf962-120">Location</span></span>      | <span data-ttu-id="bf962-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="bf962-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="bf962-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="bf962-122">GitHub</span></span>  | [<span data-ttu-id="bf962-123">Esempio ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="bf962-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="bf962-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="bf962-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="bf962-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bf962-125">Building the Sample</span></span>

1. <span data-ttu-id="bf962-126">Aprire Esplora risorse e passare alla directory del progetto **ReindexMatchingUrls** .</span><span class="sxs-lookup"><span data-stu-id="bf962-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="bf962-127">Ad esempio, il percorso di installazione predefinito completo è `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .</span><span class="sxs-lookup"><span data-stu-id="bf962-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="bf962-128">Fare doppio clic sull'icona del file REINDEX. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bf962-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="bf962-129">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="bf962-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="bf962-130">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="bf962-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="bf962-131">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="bf962-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="bf962-132">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bf962-132">Running the Sample</span></span>

1. <span data-ttu-id="bf962-133">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="bf962-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="bf962-134">Al prompt dei comandi, immettere `Reindex.exe` o da Esplora risorse, fare doppio clic sull'icona per Reindex.exe.</span><span class="sxs-lookup"><span data-stu-id="bf962-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf962-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf962-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="bf962-136">Riferimento</span><span class="sxs-lookup"><span data-stu-id="bf962-136">Reference</span></span>

[<span data-ttu-id="bf962-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="bf962-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="bf962-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="bf962-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="bf962-139">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="bf962-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="bf962-140">**ISearchPersistentItemsChangedSink**</span><span class="sxs-lookup"><span data-stu-id="bf962-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="bf962-141">**ISearchViewChangedSink**</span><span class="sxs-lookup"><span data-stu-id="bf962-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="bf962-142">**ASSEGNARE priorità ai \_ flag**</span><span class="sxs-lookup"><span data-stu-id="bf962-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="bf962-143">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="bf962-143">Other Samples</span></span>

[<span data-ttu-id="bf962-144">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="bf962-144">Search Code Samples</span></span>](-search-samples-ovw.md)

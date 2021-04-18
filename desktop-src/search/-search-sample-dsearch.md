---
description: Nell'esempio di codice DSearch viene illustrato come creare una classe per un'applicazione console statica per eseguire una query su Windows Search utilizzando l'assembly Microsoft. search. Interop per ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306147"
---
# <a name="dsearch"></a><span data-ttu-id="2b153-103">DSearch</span><span class="sxs-lookup"><span data-stu-id="2b153-103">DSearch</span></span>

<span data-ttu-id="2b153-104">Nell'esempio di codice DSearch viene illustrato come creare una classe per un'applicazione console statica per eseguire una query su Windows Search utilizzando l'assembly Microsoft. search. Interop per [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="2b153-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="2b153-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b153-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="2b153-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b153-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="2b153-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2b153-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="2b153-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2b153-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="2b153-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2b153-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="2b153-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b153-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="2b153-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b153-111">Requirements</span></span>

| <span data-ttu-id="2b153-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2b153-112">Product</span></span>     | <span data-ttu-id="2b153-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="2b153-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="2b153-114">Windows</span><span class="sxs-lookup"><span data-stu-id="2b153-114">Windows</span></span>     | <span data-ttu-id="2b153-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="2b153-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="2b153-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2b153-116">Windows SDK</span></span> | <span data-ttu-id="2b153-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2b153-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="2b153-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2b153-118">Downloading the Sample</span></span>

<span data-ttu-id="2b153-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="2b153-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="2b153-120">Location</span><span class="sxs-lookup"><span data-stu-id="2b153-120">Location</span></span>      | <span data-ttu-id="2b153-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="2b153-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="2b153-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="2b153-122">GitHub</span></span>        | [<span data-ttu-id="2b153-123">Esempio DSearch</span><span class="sxs-lookup"><span data-stu-id="2b153-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="2b153-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="2b153-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="2b153-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2b153-125">Building the Sample</span></span>

1. <span data-ttu-id="2b153-126">Aprire Esplora risorse e passare alla directory del progetto **DSearch** .</span><span class="sxs-lookup"><span data-stu-id="2b153-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="2b153-127">Fare doppio clic sull'icona per il file DSearch. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2b153-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="2b153-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2b153-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="2b153-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="2b153-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="2b153-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="2b153-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2b153-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2b153-131">Running the Sample</span></span>

1. <span data-ttu-id="2b153-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="2b153-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="2b153-133">Al prompt dei comandi, immettere `DSearch.exe` o da Esplora risorse, fare doppio clic sull'icona per DSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="2b153-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b153-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b153-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="2b153-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2b153-135">Reference</span></span>

[<span data-ttu-id="2b153-136">**ISearchQueryHelper**</span><span class="sxs-lookup"><span data-stu-id="2b153-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="2b153-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="2b153-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="2b153-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="2b153-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="2b153-139">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="2b153-139">Other Samples</span></span>

[<span data-ttu-id="2b153-140">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="2b153-140">Search Code Samples</span></span>](-search-samples-ovw.md)

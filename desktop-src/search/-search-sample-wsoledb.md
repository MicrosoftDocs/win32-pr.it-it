---
description: Nell'esempio di codice WSOleDB viene illustrato Active Template Library (ATL) OLE DB l'accesso alle applicazioni di Windows Search e vengono illustrati due metodi aggiuntivi per recuperare i risultati da ricerca di Windows.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878806"
---
# <a name="wsoledb"></a><span data-ttu-id="b76db-103">WSOleDB</span><span class="sxs-lookup"><span data-stu-id="b76db-103">WSOleDB</span></span>

<span data-ttu-id="b76db-104">Nell'esempio di codice WSOleDB viene illustrato Active Template Library (ATL) OLE DB l'accesso alle applicazioni di Windows Search e vengono illustrati due metodi aggiuntivi per recuperare i risultati da ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="b76db-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="b76db-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b76db-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="b76db-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b76db-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="b76db-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76db-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="b76db-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76db-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="b76db-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76db-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="b76db-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b76db-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="b76db-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b76db-111">Requirements</span></span>

| <span data-ttu-id="b76db-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b76db-112">Product</span></span>     | <span data-ttu-id="b76db-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="b76db-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="b76db-114">Windows</span><span class="sxs-lookup"><span data-stu-id="b76db-114">Windows</span></span>     | <span data-ttu-id="b76db-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="b76db-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="b76db-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b76db-116">Windows SDK</span></span> | <span data-ttu-id="b76db-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b76db-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="b76db-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76db-118">Downloading the Sample</span></span>

<span data-ttu-id="b76db-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="b76db-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="b76db-120">Location</span><span class="sxs-lookup"><span data-stu-id="b76db-120">Location</span></span>      | <span data-ttu-id="b76db-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="b76db-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b76db-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="b76db-122">GitHub</span></span>        | [<span data-ttu-id="b76db-123">Esempio WSOleDB</span><span class="sxs-lookup"><span data-stu-id="b76db-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="b76db-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="b76db-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="b76db-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76db-125">Building the Sample</span></span>

1. <span data-ttu-id="b76db-126">Aprire Esplora risorse e passare alla directory del progetto **WSOleDB** .</span><span class="sxs-lookup"><span data-stu-id="b76db-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="b76db-127">Fare doppio clic sull'icona per il file WSOleDB. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b76db-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="b76db-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b76db-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="b76db-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="b76db-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="b76db-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="b76db-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b76db-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76db-131">Running the Sample</span></span>

1. <span data-ttu-id="b76db-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="b76db-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="b76db-133">Al prompt dei comandi, immettere `WSOleDB.exe` o da Esplora risorse, fare doppio clic sull'icona per WSOleDB.exe.</span><span class="sxs-lookup"><span data-stu-id="b76db-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b76db-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b76db-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="b76db-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b76db-135">Reference</span></span>

[<span data-ttu-id="b76db-136">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="b76db-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="b76db-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="b76db-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="b76db-138">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="b76db-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="b76db-139">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="b76db-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="b76db-140">Informazioni concettuali</span><span class="sxs-lookup"><span data-stu-id="b76db-140">Conceptual</span></span>

[<span data-ttu-id="b76db-141">Panoramica della programmazione OLE DB</span><span class="sxs-lookup"><span data-stu-id="b76db-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="b76db-142">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="b76db-142">Other Samples</span></span>

[<span data-ttu-id="b76db-143">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="b76db-143">Search Code Samples</span></span>](-search-samples-ovw.md)

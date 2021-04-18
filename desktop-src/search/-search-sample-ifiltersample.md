---
description: Nell'esempio di codice IFilterSample viene illustrato come creare una classe di base IFilter per implementare l'interfaccia IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306146"
---
# <a name="ifiltersample"></a><span data-ttu-id="6377e-103">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="6377e-103">IFilterSample</span></span>

<span data-ttu-id="6377e-104">Nell'esempio di codice IFilterSample viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="6377e-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="6377e-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6377e-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="6377e-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6377e-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="6377e-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6377e-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="6377e-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6377e-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="6377e-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6377e-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="6377e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6377e-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="6377e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6377e-111">Requirements</span></span>

| <span data-ttu-id="6377e-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6377e-112">Product</span></span>     | <span data-ttu-id="6377e-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="6377e-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="6377e-114">Windows</span><span class="sxs-lookup"><span data-stu-id="6377e-114">Windows</span></span>     | <span data-ttu-id="6377e-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="6377e-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="6377e-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6377e-116">Windows SDK</span></span> | <span data-ttu-id="6377e-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6377e-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="6377e-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6377e-118">Downloading the Sample</span></span>

<span data-ttu-id="6377e-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="6377e-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="6377e-120">Location</span><span class="sxs-lookup"><span data-stu-id="6377e-120">Location</span></span>      | <span data-ttu-id="6377e-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="6377e-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6377e-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="6377e-122">GitHub</span></span>        | [<span data-ttu-id="6377e-123">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="6377e-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="6377e-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6377e-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="6377e-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6377e-125">Building the Sample</span></span>

1. <span data-ttu-id="6377e-126">Aprire Esplora risorse e passare alla directory del progetto **FilterBase** .</span><span class="sxs-lookup"><span data-stu-id="6377e-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="6377e-127">Fare doppio clic sull'icona per il file FilterBase. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6377e-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="6377e-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6377e-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="6377e-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="6377e-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="6377e-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="6377e-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6377e-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6377e-131">Running the Sample</span></span>

1. <span data-ttu-id="6377e-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="6377e-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="6377e-133">Al prompt dei comandi, immettere `FilterBase.exe` o da Esplora risorse, fare doppio clic sull'icona per FilterBase.exe.</span><span class="sxs-lookup"><span data-stu-id="6377e-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6377e-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6377e-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="6377e-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6377e-135">Reference</span></span>

[<span data-ttu-id="6377e-136">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="6377e-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="6377e-137">Informazioni concettuali</span><span class="sxs-lookup"><span data-stu-id="6377e-137">Conceptual</span></span>

[<span data-ttu-id="6377e-138">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="6377e-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="6377e-139">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="6377e-139">Other Samples</span></span>

[<span data-ttu-id="6377e-140">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="6377e-140">Search Code Samples</span></span>](-search-samples-ovw.md)

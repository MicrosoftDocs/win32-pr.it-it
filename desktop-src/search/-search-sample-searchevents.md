---
description: Nell'esempio di codice SearchEvents viene illustrato come classificare in ordine di priorità gli eventi di indicizzazione.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306142"
---
# <a name="searchevents"></a><span data-ttu-id="935d6-103">SearchEvents</span><span class="sxs-lookup"><span data-stu-id="935d6-103">SearchEvents</span></span>

<span data-ttu-id="935d6-104">Nell'esempio di codice SearchEvents viene illustrato come classificare in ordine di priorità gli eventi di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="935d6-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="935d6-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="935d6-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="935d6-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="935d6-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="935d6-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="935d6-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="935d6-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="935d6-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="935d6-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="935d6-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="935d6-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="935d6-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="935d6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="935d6-111">Requirements</span></span>

| <span data-ttu-id="935d6-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="935d6-112">Product</span></span>     | <span data-ttu-id="935d6-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="935d6-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="935d6-114">Windows</span><span class="sxs-lookup"><span data-stu-id="935d6-114">Windows</span></span>     | <span data-ttu-id="935d6-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="935d6-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="935d6-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="935d6-116">Windows SDK</span></span> | <span data-ttu-id="935d6-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="935d6-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="935d6-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="935d6-118">Downloading the Sample</span></span>

<span data-ttu-id="935d6-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="935d6-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="935d6-120">Location</span><span class="sxs-lookup"><span data-stu-id="935d6-120">Location</span></span>      | <span data-ttu-id="935d6-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="935d6-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="935d6-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="935d6-122">GitHub</span></span>        | [<span data-ttu-id="935d6-123">Esempio SearchEvents</span><span class="sxs-lookup"><span data-stu-id="935d6-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="935d6-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="935d6-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="935d6-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="935d6-125">Building the Sample</span></span>

1. <span data-ttu-id="935d6-126">Aprire Esplora risorse e passare alla directory del progetto **SearchEvents** .</span><span class="sxs-lookup"><span data-stu-id="935d6-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="935d6-127">Fare doppio clic sull'icona del file Eventing. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="935d6-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="935d6-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="935d6-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="935d6-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="935d6-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="935d6-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="935d6-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="935d6-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="935d6-131">Running the Sample</span></span>

1. <span data-ttu-id="935d6-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="935d6-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="935d6-133">Al prompt dei comandi, immettere `Eventing.exe` o da Esplora risorse, fare doppio clic sull'icona per Eventing.exe.</span><span class="sxs-lookup"><span data-stu-id="935d6-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="935d6-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="935d6-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="935d6-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="935d6-135">Reference</span></span>

[<span data-ttu-id="935d6-136">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="935d6-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="935d6-137">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="935d6-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="935d6-138">**livello di priorità \_**</span><span class="sxs-lookup"><span data-stu-id="935d6-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="935d6-139">**\_ITEMSTATE ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="935d6-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="935d6-140">**\_tipo ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="935d6-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="935d6-141">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="935d6-141">Other Samples</span></span>

[<span data-ttu-id="935d6-142">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="935d6-142">Search Code Samples</span></span>](-search-samples-ovw.md)

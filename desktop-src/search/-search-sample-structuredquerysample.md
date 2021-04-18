---
description: L'esempio di codice StructuredQuerySample illustra come leggere le righe dalla console, analizzarle usando lo schema del sistema e visualizzare gli alberi delle condizioni risultanti.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306143"
---
# <a name="structuredquerysample"></a><span data-ttu-id="21039-103">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="21039-103">StructuredQuerySample</span></span>

<span data-ttu-id="21039-104">L'esempio di codice StructuredQuerySample illustra come leggere le righe dalla console, analizzarle usando lo schema del sistema e visualizzare gli alberi delle condizioni risultanti.</span><span class="sxs-lookup"><span data-stu-id="21039-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="21039-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="21039-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="21039-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21039-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="21039-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="21039-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="21039-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="21039-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="21039-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="21039-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="21039-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21039-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="21039-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21039-111">Requirements</span></span>

| <span data-ttu-id="21039-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="21039-112">Product</span></span>     | <span data-ttu-id="21039-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="21039-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="21039-114">Windows</span><span class="sxs-lookup"><span data-stu-id="21039-114">Windows</span></span>     | <span data-ttu-id="21039-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="21039-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="21039-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="21039-116">Windows SDK</span></span> | <span data-ttu-id="21039-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="21039-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="21039-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="21039-118">Downloading the Sample</span></span>

<span data-ttu-id="21039-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="21039-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="21039-120">Location</span><span class="sxs-lookup"><span data-stu-id="21039-120">Location</span></span>      | <span data-ttu-id="21039-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="21039-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="21039-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="21039-122">GitHub</span></span>        | [<span data-ttu-id="21039-123">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="21039-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="21039-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="21039-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="21039-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="21039-125">Building the Sample</span></span>

1. <span data-ttu-id="21039-126">Aprire Esplora risorse e passare alla directory del progetto **StructuredQuerySample** .</span><span class="sxs-lookup"><span data-stu-id="21039-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="21039-127">Fare doppio clic sull'icona per il file StructuredQuerySample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="21039-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="21039-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="21039-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="21039-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="21039-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="21039-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="21039-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="21039-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="21039-131">Running the Sample</span></span>

1. <span data-ttu-id="21039-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="21039-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="21039-133">Al prompt dei comandi, immettere `StructuredQuerySample.exe` o da Esplora risorse, fare doppio clic sull'icona per StructuredQuerySample.exe.</span><span class="sxs-lookup"><span data-stu-id="21039-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21039-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21039-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="21039-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="21039-135">Reference</span></span>

[<span data-ttu-id="21039-136">**ICondition**</span><span class="sxs-lookup"><span data-stu-id="21039-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="21039-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="21039-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="21039-138">**IConditionFactory**</span><span class="sxs-lookup"><span data-stu-id="21039-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="21039-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="21039-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="21039-140">**IConditionGenerator**</span><span class="sxs-lookup"><span data-stu-id="21039-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="21039-141">**IQueryParser**</span><span class="sxs-lookup"><span data-stu-id="21039-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="21039-142">**IQueryParserManager**</span><span class="sxs-lookup"><span data-stu-id="21039-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="21039-143">**IQuerySolution**</span><span class="sxs-lookup"><span data-stu-id="21039-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="21039-144">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="21039-144">Other Samples</span></span>

[<span data-ttu-id="21039-145">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="21039-145">Search Code Samples</span></span>](-search-samples-ovw.md)

---
description: Nell'esempio di codice OpenSearch viene illustrato come creare un servizio di ricerca federato utilizzando il protocollo OpenSearch e un file descrittore OpenSearch (con estensione osdx) (un connettore di ricerca).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401628"
---
# <a name="opensearch"></a><span data-ttu-id="92e4a-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="92e4a-103">OpenSearch</span></span>

<span data-ttu-id="92e4a-104">Nell'esempio di codice OpenSearch viene illustrato come creare un servizio di ricerca federato utilizzando il protocollo [OpenSearch](https://github.com/dewitt/opensearch) e un file descrittore OpenSearch (con estensione osdx) (un connettore di ricerca).</span><span class="sxs-lookup"><span data-stu-id="92e4a-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="92e4a-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="92e4a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="92e4a-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92e4a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="92e4a-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="92e4a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="92e4a-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="92e4a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="92e4a-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="92e4a-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="92e4a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92e4a-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="92e4a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92e4a-111">Requirements</span></span>



| <span data-ttu-id="92e4a-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="92e4a-112">Product</span></span>     | <span data-ttu-id="92e4a-113">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="92e4a-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="92e4a-114">Windows</span><span class="sxs-lookup"><span data-stu-id="92e4a-114">Windows</span></span>     | <span data-ttu-id="92e4a-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="92e4a-115">Windows 7</span></span>               |
| <span data-ttu-id="92e4a-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="92e4a-116">Windows SDK</span></span> | <span data-ttu-id="92e4a-117">7.0</span><span class="sxs-lookup"><span data-stu-id="92e4a-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="92e4a-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="92e4a-118">Downloading the Sample</span></span>

<span data-ttu-id="92e4a-119">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="92e4a-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="92e4a-120">Location</span><span class="sxs-lookup"><span data-stu-id="92e4a-120">Location</span></span>      | <span data-ttu-id="92e4a-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="92e4a-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="92e4a-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="92e4a-122">GitHub</span></span>  | [<span data-ttu-id="92e4a-123">Esempio OpenSearch</span><span class="sxs-lookup"><span data-stu-id="92e4a-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="92e4a-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="92e4a-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="92e4a-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="92e4a-125">Building the Sample</span></span>

<span data-ttu-id="92e4a-126">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="92e4a-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="92e4a-127">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="92e4a-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="92e4a-128">Immettere `msbuild AdventureSearch.sln`.</span><span class="sxs-lookup"><span data-stu-id="92e4a-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="92e4a-129">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="92e4a-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="92e4a-130">Aprire Esplora risorse e passare alla directory del progetto **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="92e4a-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="92e4a-131">Fare doppio clic sull'icona per il file AdventureSearch. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="92e4a-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="92e4a-132">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="92e4a-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="92e4a-133">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="92e4a-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="92e4a-134">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="92e4a-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="92e4a-135">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="92e4a-135">Running the Sample</span></span>

1.  <span data-ttu-id="92e4a-136">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="92e4a-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="92e4a-137">Al prompt dei comandi, immettere `AdventureSearch.exe` o da Esplora risorse, fare doppio clic sull'icona per AdventureSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="92e4a-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="92e4a-138">Al prompt dei comandi, immettere `GetOSDX.exe` o da Esplora risorse, fare doppio clic sull'icona per GetOSDX.exe.</span><span class="sxs-lookup"><span data-stu-id="92e4a-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92e4a-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92e4a-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="92e4a-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="92e4a-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92e4a-141">Panoramica dello schema di descrizione del connettore di ricerca</span><span class="sxs-lookup"><span data-stu-id="92e4a-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="92e4a-142">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="92e4a-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="92e4a-143">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="92e4a-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="92e4a-144">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="92e4a-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="92e4a-145">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="92e4a-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="92e4a-146">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="92e4a-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 

---
description: Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e la ricerca di Windows tramite Structured Query Language (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878805"
---
# <a name="wssql"></a><span data-ttu-id="03806-103">WSSQL</span><span class="sxs-lookup"><span data-stu-id="03806-103">WSSQL</span></span>

<span data-ttu-id="03806-104">Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e la ricerca di Windows tramite Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="03806-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="03806-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="03806-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="03806-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03806-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="03806-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="03806-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="03806-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="03806-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="03806-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="03806-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="03806-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03806-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="03806-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03806-111">Requirements</span></span>

| <span data-ttu-id="03806-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="03806-112">Product</span></span>     | <span data-ttu-id="03806-113">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="03806-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="03806-114">Windows</span><span class="sxs-lookup"><span data-stu-id="03806-114">Windows</span></span>     | <span data-ttu-id="03806-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="03806-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="03806-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="03806-116">Windows SDK</span></span> | <span data-ttu-id="03806-117">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="03806-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="03806-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="03806-118">Downloading the Sample</span></span>

<span data-ttu-id="03806-119">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="03806-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="03806-120">Location</span><span class="sxs-lookup"><span data-stu-id="03806-120">Location</span></span>      | <span data-ttu-id="03806-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="03806-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="03806-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="03806-122">GitHub</span></span>        | [<span data-ttu-id="03806-123">Esempio WSSQL</span><span class="sxs-lookup"><span data-stu-id="03806-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="03806-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="03806-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="03806-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="03806-125">Building the Sample</span></span>

1. <span data-ttu-id="03806-126">Aprire Esplora risorse e passare alla directory del progetto **WSSQL** .</span><span class="sxs-lookup"><span data-stu-id="03806-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="03806-127">Fare doppio clic sull'icona per il file WSSQL. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="03806-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="03806-128">Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="03806-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="03806-129">Questo non avrà alcun effetto sul comportamento dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="03806-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="03806-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="03806-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="03806-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="03806-131">Running the Sample</span></span>

1. <span data-ttu-id="03806-132">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="03806-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="03806-133">Al prompt dei comandi, immettere `WSSQL.exe` o da Esplora risorse, fare doppio clic sull'icona per WSSQL.exe.</span><span class="sxs-lookup"><span data-stu-id="03806-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03806-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03806-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="03806-135">Informazioni concettuali</span><span class="sxs-lookup"><span data-stu-id="03806-135">Conceptual</span></span>

[<span data-ttu-id="03806-136">Uso della sintassi SQL di Windows Search</span><span class="sxs-lookup"><span data-stu-id="03806-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="03806-137">Informazioni generali sul linguaggio di query</span><span class="sxs-lookup"><span data-stu-id="03806-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="03806-138">Panoramica della programmazione OLE DB</span><span class="sxs-lookup"><span data-stu-id="03806-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="03806-139">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="03806-139">Other Samples</span></span>

[<span data-ttu-id="03806-140">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="03806-140">Search Code Samples</span></span>](-search-samples-ovw.md)

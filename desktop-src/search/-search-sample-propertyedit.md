---
description: Nell'esempio di codice PropertyEdit viene illustrato come convertire il nome di proprietà canonico in un PROPERTYKEY, impostare il valore dell'archivio delle proprietà su quello dell'elemento e riscrivere i dati nel flusso di file.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878810"
---
# <a name="propertyedit"></a><span data-ttu-id="edacb-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="edacb-103">PropertyEdit</span></span>

<span data-ttu-id="edacb-104">Nell'esempio di codice PropertyEdit viene illustrato come convertire il nome di proprietà canonico in un PROPERTYKEY, impostare il valore dell'archivio delle proprietà su quello dell'elemento e riscrivere i dati nel flusso di file.</span><span class="sxs-lookup"><span data-stu-id="edacb-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="edacb-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="edacb-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="edacb-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edacb-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="edacb-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="edacb-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="edacb-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="edacb-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="edacb-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="edacb-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="edacb-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="edacb-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="edacb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edacb-111">Requirements</span></span>



| <span data-ttu-id="edacb-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="edacb-112">Product</span></span>     | <span data-ttu-id="edacb-113">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="edacb-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="edacb-114">Windows</span><span class="sxs-lookup"><span data-stu-id="edacb-114">Windows</span></span>     | <span data-ttu-id="edacb-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="edacb-115">Windows 7</span></span>               |
| <span data-ttu-id="edacb-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="edacb-116">Windows SDK</span></span> | <span data-ttu-id="edacb-117">7.0</span><span class="sxs-lookup"><span data-stu-id="edacb-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="edacb-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="edacb-118">Downloading the Sample</span></span>

<span data-ttu-id="edacb-119">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="edacb-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="edacb-120">Location</span><span class="sxs-lookup"><span data-stu-id="edacb-120">Location</span></span>      | <span data-ttu-id="edacb-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="edacb-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="edacb-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="edacb-122">GitHub</span></span>  | [<span data-ttu-id="edacb-123">Esempio PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="edacb-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="edacb-124">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="edacb-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="edacb-125">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="edacb-125">Building the Sample</span></span>

<span data-ttu-id="edacb-126">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="edacb-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="edacb-127">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="edacb-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="edacb-128">Immettere `msbuild PropertyEdit.sln`.</span><span class="sxs-lookup"><span data-stu-id="edacb-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="edacb-129">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="edacb-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="edacb-130">Aprire Esplora risorse e passare alla directory del progetto **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="edacb-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="edacb-131">Fare doppio clic sull'icona per il file PropertyEdit. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="edacb-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="edacb-132">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="edacb-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="edacb-133">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="edacb-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="edacb-134">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="edacb-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="edacb-135">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="edacb-135">Running the Sample</span></span>

1.  <span data-ttu-id="edacb-136">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="edacb-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="edacb-137">Al prompt dei comandi, immettere `PropertyEdit.exe` o da Esplora risorse, fare doppio clic sull'icona per PropertyEdit.exe.</span><span class="sxs-lookup"><span data-stu-id="edacb-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edacb-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="edacb-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="edacb-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="edacb-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="edacb-140">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="edacb-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="edacb-141">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="edacb-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="edacb-142">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="edacb-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="edacb-143">Informazioni sulle proprietà e sui gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="edacb-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="edacb-144">[Schema Descrizione proprietà](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="edacb-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 

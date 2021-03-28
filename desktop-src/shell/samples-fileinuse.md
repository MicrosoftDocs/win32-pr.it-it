---
description: Viene illustrato come personalizzare la finestra di dialogo file in uso per visualizzare informazioni e opzioni aggiuntive per i file attualmente aperti nell'applicazione.
title: Esempio di File in uso
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345926"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="83a3e-103">Esempio di File in uso</span><span class="sxs-lookup"><span data-stu-id="83a3e-103">File Is In Use Sample</span></span>

<span data-ttu-id="83a3e-104">Viene illustrato come personalizzare la finestra di dialogo **file in uso** per visualizzare informazioni e opzioni aggiuntive per i file attualmente aperti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="83a3e-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="83a3e-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="83a3e-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="83a3e-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83a3e-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="83a3e-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="83a3e-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="83a3e-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="83a3e-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="83a3e-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="83a3e-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="83a3e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83a3e-110">Requirements</span></span>



| <span data-ttu-id="83a3e-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="83a3e-111">Product</span></span>                                | <span data-ttu-id="83a3e-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="83a3e-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="83a3e-113">Windows</span><span class="sxs-lookup"><span data-stu-id="83a3e-113">Windows</span></span>                                | <span data-ttu-id="83a3e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83a3e-114">Windows Vista</span></span>           |
| <span data-ttu-id="83a3e-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="83a3e-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="83a3e-116">6.1</span><span class="sxs-lookup"><span data-stu-id="83a3e-116">6.1</span></span>                     |



 

<span data-ttu-id="83a3e-117">Per ulteriori requisiti, vedere il \_ file IFileIsInUsesample.docx incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="83a3e-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="83a3e-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="83a3e-118">Downloading the Sample</span></span>

| <span data-ttu-id="83a3e-119">Location</span><span class="sxs-lookup"><span data-stu-id="83a3e-119">Location</span></span>      | <span data-ttu-id="83a3e-120">URL percorso</span><span class="sxs-lookup"><span data-stu-id="83a3e-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a3e-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="83a3e-121">GitHub</span></span>  | [<span data-ttu-id="83a3e-122">Esempio FileIsInUse</span><span class="sxs-lookup"><span data-stu-id="83a3e-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="83a3e-123">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="83a3e-123">Building the Sample</span></span>

<span data-ttu-id="83a3e-124">Per compilare l'esempio dalla finestra del prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="83a3e-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="83a3e-125">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **FileIsInUse** .</span><span class="sxs-lookup"><span data-stu-id="83a3e-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="83a3e-126">Immettere `msbuild FileIsInUse.sln`.</span><span class="sxs-lookup"><span data-stu-id="83a3e-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="83a3e-127">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="83a3e-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="83a3e-128">Aprire Esplora risorse e passare alla directory del progetto **filesinus** .</span><span class="sxs-lookup"><span data-stu-id="83a3e-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="83a3e-129">Ad esempio, il percorso di installazione predefinito completo è `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .</span><span class="sxs-lookup"><span data-stu-id="83a3e-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="83a3e-130">Fare doppio clic sull'icona per il file FileIsInUseSample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="83a3e-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="83a3e-131">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="83a3e-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="83a3e-132">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="83a3e-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="83a3e-133">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="83a3e-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="83a3e-134">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="83a3e-134">Running the Sample</span></span>

1.  <span data-ttu-id="83a3e-135">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="83a3e-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="83a3e-136">Al prompt dei comandi, immettere `FileIsInUseSample.exe` o da Esplora risorse, fare doppio clic sull'icona per FileIsInUseSample.exe.</span><span class="sxs-lookup"><span data-stu-id="83a3e-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="83a3e-137">Per informazioni dettagliate su questo esempio di codice, vedere il \_ file IFileIsInUsesample.docx incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="83a3e-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 




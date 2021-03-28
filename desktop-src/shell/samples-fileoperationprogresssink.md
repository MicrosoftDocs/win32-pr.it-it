---
description: Viene illustrato come utilizzare i metodi dell'interfaccia IFileOperationProgressSink per il monitoraggio dei dettagli delle azioni dell'interfaccia IFileOperation.
title: FileOperationProgressSink
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050181"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="62210-103">FileOperationProgressSink</span><span class="sxs-lookup"><span data-stu-id="62210-103">File Operation Progress Sink</span></span>

<span data-ttu-id="62210-104">Viene illustrato come utilizzare i metodi dell'interfaccia [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) per il monitoraggio dei dettagli delle azioni dell'interfaccia [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .</span><span class="sxs-lookup"><span data-stu-id="62210-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="62210-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="62210-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="62210-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62210-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="62210-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62210-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="62210-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62210-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="62210-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62210-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="62210-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62210-110">Requirements</span></span>



| <span data-ttu-id="62210-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="62210-111">Product</span></span>                                | <span data-ttu-id="62210-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="62210-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="62210-113">Windows</span><span class="sxs-lookup"><span data-stu-id="62210-113">Windows</span></span>                                | <span data-ttu-id="62210-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62210-114">Windows Vista</span></span>           |
| <span data-ttu-id="62210-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="62210-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="62210-116">6.1</span><span class="sxs-lookup"><span data-stu-id="62210-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="62210-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62210-117">Downloading the Sample</span></span>

| <span data-ttu-id="62210-118">Location</span><span class="sxs-lookup"><span data-stu-id="62210-118">Location</span></span>      | <span data-ttu-id="62210-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="62210-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62210-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="62210-120">GitHub</span></span>  | [<span data-ttu-id="62210-121">Esempio FileOperationProgressSink</span><span class="sxs-lookup"><span data-stu-id="62210-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="62210-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62210-122">Building the Sample</span></span>

<span data-ttu-id="62210-123">Per compilare l'esempio dalla finestra del prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="62210-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="62210-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **FileOperationProgressSink** .</span><span class="sxs-lookup"><span data-stu-id="62210-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="62210-125">Immettere `msbuild FileOperationProgressSinkSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="62210-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="62210-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="62210-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="62210-127">Aprire Esplora risorse e passare alla directory del progetto **filesinus** .</span><span class="sxs-lookup"><span data-stu-id="62210-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="62210-128">Ad esempio, il percorso di installazione predefinito completo è `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .</span><span class="sxs-lookup"><span data-stu-id="62210-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="62210-129">Fare doppio clic sull'icona per il file FileOperationProgressSinkSample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="62210-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="62210-130">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="62210-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="62210-131">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="62210-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="62210-132">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="62210-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="62210-133">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62210-133">Running the Sample</span></span>

1.  <span data-ttu-id="62210-134">Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="62210-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="62210-135">Al prompt dei comandi, immettere `FileOperationProgressSinkSample.exe` o da Esplora risorse, fare doppio clic sull'icona per FileOperationProgressSinkSample.exe.</span><span class="sxs-lookup"><span data-stu-id="62210-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 




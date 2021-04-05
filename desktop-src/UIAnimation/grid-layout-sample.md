---
title: Esempio di layout di griglia
description: Viene illustrato come utilizzare l'animazione Windows utilizzando Direct2D per animare una griglia di immagini.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "103724359"
---
# <a name="grid-layout-sample"></a><span data-ttu-id="0ba70-103">Esempio di layout di griglia</span><span class="sxs-lookup"><span data-stu-id="0ba70-103">Grid Layout Sample</span></span>

<span data-ttu-id="0ba70-104">Viene illustrato come utilizzare l'animazione Windows utilizzando Direct2D per animare una griglia di immagini.</span><span class="sxs-lookup"><span data-stu-id="0ba70-104">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="0ba70-105">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0ba70-105">Downloading the Sample</span></span>

<span data-ttu-id="0ba70-106">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ba70-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="0ba70-107">Location</span><span class="sxs-lookup"><span data-stu-id="0ba70-107">Location</span></span>                               | <span data-ttu-id="0ba70-108">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="0ba70-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba70-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="0ba70-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="0ba70-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="0ba70-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="0ba70-111">Code Gallery</span><span class="sxs-lookup"><span data-stu-id="0ba70-111">Code Gallery</span></span>                           | [<span data-ttu-id="0ba70-112">Codice di esempio di Windows Animation Manager</span><span class="sxs-lookup"><span data-stu-id="0ba70-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="0ba70-113">Dopo aver scaricato e installato il Windows SDK, gli esempi sono disponibili nella directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="0ba70-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="0ba70-114">Se ad esempio si usa il percorso di installazione predefinito per il Windows SDK per Windows 7, gli esempi vengono installati in C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi.</span><span class="sxs-lookup"><span data-stu-id="0ba70-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="0ba70-115">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0ba70-115">Building the Sample</span></span>

<span data-ttu-id="0ba70-116">Per compilare l'esempio, utilizzare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ba70-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="0ba70-117">**Per compilare l'esempio al prompt dei comandi**</span><span class="sxs-lookup"><span data-stu-id="0ba70-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="0ba70-118">Aprire la finestra del prompt dei comandi e passare alla directory del progetto GridLayout.</span><span class="sxs-lookup"><span data-stu-id="0ba70-118">Open the Command Prompt window and navigate to the GridLayout project directory.</span></span> <span data-ttu-id="0ba70-119">Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ GridLayout</span><span class="sxs-lookup"><span data-stu-id="0ba70-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\GridLayout</span></span>

2.  <span data-ttu-id="0ba70-120">Eseguire il comando seguente: **MSBuild GridLayout. sln**</span><span class="sxs-lookup"><span data-stu-id="0ba70-120">Run the following command: **msbuild GridLayout.sln**</span></span>

<span data-ttu-id="0ba70-121">**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**</span><span class="sxs-lookup"><span data-stu-id="0ba70-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="0ba70-122">Aprire Esplora risorse e passare alla directory del progetto GridLayout.</span><span class="sxs-lookup"><span data-stu-id="0ba70-122">Open Windows Explorer and navigate to the GridLayout project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="0ba70-123">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="0ba70-123">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="0ba70-124">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="0ba70-124">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="0ba70-125">Fare doppio clic sull'icona per il file GridLayout. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0ba70-125">Double-click the icon for the GridLayout.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="0ba70-126">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="0ba70-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0ba70-127">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0ba70-127">Running the Sample</span></span>

<span data-ttu-id="0ba70-128">Per eseguire l'esempio:</span><span class="sxs-lookup"><span data-stu-id="0ba70-128">To run the sample:</span></span>

1.  <span data-ttu-id="0ba70-129">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="0ba70-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="0ba70-130">Eseguire **GridLayout.exe** al prompt dei comandi oppure fare doppio clic sull'icona GridLayout.exe in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="0ba70-130">Run **GridLayout.exe** at the command prompt, or double-click the icon for GridLayout.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="0ba70-131">Le immagini di esempio vengono caricate dalla raccolta immagini.</span><span class="sxs-lookup"><span data-stu-id="0ba70-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="0ba70-132">Ridimensionare la finestra e le immagini si disporrà in una griglia.</span><span class="sxs-lookup"><span data-stu-id="0ba70-132">Resize the window and the images will arrange themselves into a grid.</span></span>

 

 





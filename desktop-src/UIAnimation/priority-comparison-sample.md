---
title: Esempio di confronto prioritario
description: Viene illustrato come utilizzare l'animazione Windows con un confronto prioritario tramite Direct2D per il rendering.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "104117502"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="70ab7-103">Esempio di confronto prioritario</span><span class="sxs-lookup"><span data-stu-id="70ab7-103">Priority Comparison Sample</span></span>

<span data-ttu-id="70ab7-104">Viene illustrato come utilizzare l'animazione Windows con un confronto prioritario tramite Direct2D per il rendering.</span><span class="sxs-lookup"><span data-stu-id="70ab7-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="70ab7-105">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70ab7-105">Downloading the Sample</span></span>

<span data-ttu-id="70ab7-106">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="70ab7-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="70ab7-107">Location</span><span class="sxs-lookup"><span data-stu-id="70ab7-107">Location</span></span>                               | <span data-ttu-id="70ab7-108">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="70ab7-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ab7-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="70ab7-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="70ab7-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="70ab7-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="70ab7-111">Code Gallery</span><span class="sxs-lookup"><span data-stu-id="70ab7-111">Code Gallery</span></span>                           | [<span data-ttu-id="70ab7-112">Codice di esempio di Windows Animation Manager</span><span class="sxs-lookup"><span data-stu-id="70ab7-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="70ab7-113">Dopo aver scaricato e installato il Windows SDK, gli esempi sono disponibili nella directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="70ab7-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="70ab7-114">Se ad esempio si usa il percorso di installazione predefinito per il Windows SDK per Windows 7, gli esempi vengono installati in C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi.</span><span class="sxs-lookup"><span data-stu-id="70ab7-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="70ab7-115">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70ab7-115">Building the Sample</span></span>

<span data-ttu-id="70ab7-116">Per compilare l'esempio, utilizzare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="70ab7-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="70ab7-117">**Per compilare l'esempio al prompt dei comandi**</span><span class="sxs-lookup"><span data-stu-id="70ab7-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="70ab7-118">Aprire la finestra del prompt dei comandi e passare alla directory del progetto PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="70ab7-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="70ab7-119">Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="70ab7-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="70ab7-120">Eseguire il comando seguente: **MSBuild PriorityComparison. sln**</span><span class="sxs-lookup"><span data-stu-id="70ab7-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="70ab7-121">**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**</span><span class="sxs-lookup"><span data-stu-id="70ab7-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="70ab7-122">Aprire Esplora risorse e passare alla directory del progetto PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="70ab7-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="70ab7-123">Fare doppio clic sull'icona per il file PriorityComparison. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="70ab7-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="70ab7-124">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="70ab7-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="70ab7-125">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="70ab7-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="70ab7-126">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="70ab7-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="70ab7-127">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="70ab7-127">Running the Sample</span></span>

<span data-ttu-id="70ab7-128">Per eseguire l'esempio:</span><span class="sxs-lookup"><span data-stu-id="70ab7-128">To run the sample:</span></span>

1.  <span data-ttu-id="70ab7-129">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="70ab7-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="70ab7-130">Eseguire **PriorityComparison.exe** al prompt dei comandi oppure fare doppio clic sull'icona PriorityComparison.exe in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="70ab7-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="70ab7-131">Le immagini di esempio vengono caricate dalla raccolta immagini.</span><span class="sxs-lookup"><span data-stu-id="70ab7-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="70ab7-132">Ridimensionare la finestra o premere la barra spaziatrice e le immagini vengono spostate al centro.</span><span class="sxs-lookup"><span data-stu-id="70ab7-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="70ab7-133">Usare i tasti freccia sinistra e destra per selezionare immagini diverse (più velocemente verrà premuto il tasto, più velocemente verrà modificata la selezione).</span><span class="sxs-lookup"><span data-stu-id="70ab7-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="70ab7-134">Usare i tasti freccia su e giù per creare un'onda attraverso le immagini (maggiore è la pressione della chiave, più velocemente l'onda).</span><span class="sxs-lookup"><span data-stu-id="70ab7-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 





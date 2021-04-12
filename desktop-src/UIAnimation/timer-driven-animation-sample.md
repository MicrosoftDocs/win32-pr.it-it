---
title: Esempio di animazione Timer-Driven
description: Viene illustrato come utilizzare l'animazione Windows con il timer animazione, mentre si utilizza GDI+ per animare il colore di sfondo di una finestra.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "104336742"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="228ca-103">Esempio di animazione Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="228ca-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="228ca-104">Viene illustrato come utilizzare l'animazione Windows con il timer animazione, mentre si utilizza GDI+ per animare il colore di sfondo di una finestra.</span><span class="sxs-lookup"><span data-stu-id="228ca-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="228ca-105">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="228ca-105">Downloading the Sample</span></span>

<span data-ttu-id="228ca-106">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="228ca-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="228ca-107">Location</span><span class="sxs-lookup"><span data-stu-id="228ca-107">Location</span></span>                               | <span data-ttu-id="228ca-108">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="228ca-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="228ca-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="228ca-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="228ca-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="228ca-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="228ca-111">Code Gallery</span><span class="sxs-lookup"><span data-stu-id="228ca-111">Code Gallery</span></span>                           | [<span data-ttu-id="228ca-112">Codice di esempio di Windows Animation Manager</span><span class="sxs-lookup"><span data-stu-id="228ca-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="228ca-113">Dopo aver scaricato e installato il Windows SDK, gli esempi sono disponibili nella directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="228ca-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="228ca-114">Se ad esempio si usa il percorso di installazione predefinito per il Windows SDK per Windows 7, gli esempi vengono installati in C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi.</span><span class="sxs-lookup"><span data-stu-id="228ca-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="228ca-115">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="228ca-115">Building the Sample</span></span>

<span data-ttu-id="228ca-116">Per compilare l'esempio, utilizzare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="228ca-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="228ca-117">**Per compilare l'esempio al prompt dei comandi**</span><span class="sxs-lookup"><span data-stu-id="228ca-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="228ca-118">Aprire la finestra del prompt dei comandi e passare alla directory del progetto TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="228ca-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="228ca-119">Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="228ca-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="228ca-120">Eseguire il comando seguente: **MSBuild TimerDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="228ca-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="228ca-121">**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**</span><span class="sxs-lookup"><span data-stu-id="228ca-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="228ca-122">Aprire Esplora risorse e passare alla directory del progetto TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="228ca-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="228ca-123">Fare doppio clic sull'icona per il file TimerDriven. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="228ca-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="228ca-124">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="228ca-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="228ca-125">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="228ca-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="228ca-126">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="228ca-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="228ca-127">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="228ca-127">Running the Sample</span></span>

<span data-ttu-id="228ca-128">Per eseguire l'esempio:</span><span class="sxs-lookup"><span data-stu-id="228ca-128">To run the sample:</span></span>

1.  <span data-ttu-id="228ca-129">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="228ca-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="228ca-130">Eseguire **TimerDriven.exe** al prompt dei comandi oppure fare doppio clic sull'icona TimerDriven.exe in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="228ca-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="228ca-131">Fare clic in un punto qualsiasi dell'area client e il colore di sfondo della finestra cambierà in un colore casuale.</span><span class="sxs-lookup"><span data-stu-id="228ca-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 





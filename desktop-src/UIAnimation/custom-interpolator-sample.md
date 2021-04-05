---
title: Esempio di interpolazione personalizzata
description: Viene illustrato come utilizzare l'animazione Windows con un interpolatore personalizzato, con Direct2D utilizzato per il rendering.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "104117503"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="b655f-103">Esempio di interpolazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b655f-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="b655f-104">Viene illustrato come utilizzare l'animazione Windows con un interpolatore personalizzato, con Direct2D utilizzato per il rendering.</span><span class="sxs-lookup"><span data-stu-id="b655f-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="b655f-105">Le immagini di esempio vengono caricate dalla raccolta immagini.</span><span class="sxs-lookup"><span data-stu-id="b655f-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b655f-106">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b655f-106">Downloading the Sample</span></span>

<span data-ttu-id="b655f-107">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b655f-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="b655f-108">Location</span><span class="sxs-lookup"><span data-stu-id="b655f-108">Location</span></span>                               | <span data-ttu-id="b655f-109">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="b655f-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b655f-110">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b655f-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="b655f-111">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="b655f-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="b655f-112">Code Gallery</span><span class="sxs-lookup"><span data-stu-id="b655f-112">Code Gallery</span></span>                           | [<span data-ttu-id="b655f-113">Codice di esempio di Windows Animation Manager</span><span class="sxs-lookup"><span data-stu-id="b655f-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="b655f-114">Dopo aver scaricato e installato il Windows SDK, gli esempi sono disponibili nella directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="b655f-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="b655f-115">Se ad esempio si usa il percorso di installazione predefinito per il Windows SDK per Windows 7, gli esempi vengono installati in C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi.</span><span class="sxs-lookup"><span data-stu-id="b655f-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="b655f-116">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b655f-116">Building the Sample</span></span>

<span data-ttu-id="b655f-117">Per compilare l'esempio, utilizzare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b655f-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="b655f-118">**Per compilare l'esempio al prompt dei comandi**</span><span class="sxs-lookup"><span data-stu-id="b655f-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="b655f-119">Aprire la finestra del prompt dei comandi e passare alla directory del progetto CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="b655f-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="b655f-120">Ad esempio, il percorso di installazione predefinito per questo esempio è C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ CustomInterpolator</span><span class="sxs-lookup"><span data-stu-id="b655f-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="b655f-121">Eseguire il comando seguente: **MSBuild CustomInterpolator. sln**</span><span class="sxs-lookup"><span data-stu-id="b655f-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="b655f-122">**Per compilare l'esempio utilizzando Microsoft Visual Studio (scelta consigliata)**</span><span class="sxs-lookup"><span data-stu-id="b655f-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="b655f-123">Aprire Esplora risorse e passare alla directory del progetto CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="b655f-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="b655f-124">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="b655f-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="b655f-125">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="b655f-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="b655f-126">Fare doppio clic sull'icona per il file CustomInterpolator. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b655f-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="b655f-127">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="b655f-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b655f-128">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b655f-128">Running the Sample</span></span>

<span data-ttu-id="b655f-129">Per eseguire l'esempio:</span><span class="sxs-lookup"><span data-stu-id="b655f-129">To run the sample:</span></span>

1.  <span data-ttu-id="b655f-130">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="b655f-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="b655f-131">Eseguire **CustomInterpolator.exe** al prompt dei comandi oppure fare doppio clic sull'icona CustomInterpolator.exe in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="b655f-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="b655f-132">Ridimensionare la finestra o premere la barra spaziatrice e le immagini si sistemeranno in modo casuale al centro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="b655f-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="b655f-133">Premere la freccia verso l'alto o verso il basso e le immagini si accelereranno verso la parte superiore o inferiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="b655f-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 





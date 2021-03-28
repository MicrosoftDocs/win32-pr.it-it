---
description: Viene illustrato come implementare un verbo della shell utilizzando il metodo DropTarget.
title: Esempio di verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979935"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="04174-103">Esempio di verbo DropTarget</span><span class="sxs-lookup"><span data-stu-id="04174-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="04174-104">Viene illustrato come implementare un verbo della shell utilizzando il metodo DropTarget.</span><span class="sxs-lookup"><span data-stu-id="04174-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="04174-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="04174-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="04174-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04174-106">Description</span></span>](#description)
-   [<span data-ttu-id="04174-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04174-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="04174-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="04174-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="04174-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="04174-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="04174-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="04174-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="04174-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04174-111">Description</span></span>

<span data-ttu-id="04174-112">In questo esempio viene illustrato come implementare un verbo della shell utilizzando il metodo DropTarget.</span><span class="sxs-lookup"><span data-stu-id="04174-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="04174-113">Questo metodo è preferibile per le implementazioni di verbi che devono funzionare in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04174-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="04174-114">Questo esempio implementa un oggetto server locale Component Object Model (COM) autonomo, ma si prevede che l'implementazione del verbo verrà integrata nelle applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="04174-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="04174-115">A tale scopo, l'oggetto applicazione principale registra un class factory per se stesso.</span><span class="sxs-lookup"><span data-stu-id="04174-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="04174-116">Tale oggetto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per i verbi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="04174-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="04174-117">Si noti che COM avvia l'applicazione se non è già in esecuzione, ma si connette a un'istanza in esecuzione dell'applicazione, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="04174-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="04174-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04174-118">Requirements</span></span>



| <span data-ttu-id="04174-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="04174-119">Product</span></span>                                | <span data-ttu-id="04174-120">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="04174-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="04174-121">Windows</span><span class="sxs-lookup"><span data-stu-id="04174-121">Windows</span></span>                                | <span data-ttu-id="04174-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04174-122">Windows Vista</span></span>           |
| <span data-ttu-id="04174-123">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="04174-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="04174-124">7.0</span><span class="sxs-lookup"><span data-stu-id="04174-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="04174-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="04174-125">Downloading the Sample</span></span>

| <span data-ttu-id="04174-126">Location</span><span class="sxs-lookup"><span data-stu-id="04174-126">Location</span></span>      | <span data-ttu-id="04174-127">URL percorso</span><span class="sxs-lookup"><span data-stu-id="04174-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04174-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="04174-128">GitHub</span></span>  | [<span data-ttu-id="04174-129">Esempio DropTargetVerb</span><span class="sxs-lookup"><span data-stu-id="04174-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="04174-130">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="04174-130">Building the Sample</span></span>

<span data-ttu-id="04174-131">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="04174-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="04174-132">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="04174-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="04174-133">Immettere `msbuild DropTargetVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="04174-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="04174-134">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="04174-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="04174-135">Aprire Esplora risorse e passare alla directory del progetto **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="04174-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="04174-136">Fare doppio clic sull'icona per il file DropTargetVerb. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="04174-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="04174-137">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="04174-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="04174-138">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="04174-138">Running the Sample</span></span>

1.  <span data-ttu-id="04174-139">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="04174-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="04174-140">Nella riga di comando, immettere `DropTargetVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="04174-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="04174-141">In alternativa, in Esplora risorse fare doppio clic sull'icona per DropTargetVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="04174-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="04174-142">Seguire le istruzioni riportate nella finestra di dialogo visualizzata</span><span class="sxs-lookup"><span data-stu-id="04174-142">Follow the instructions in the displayed dialog</span></span>

 

 

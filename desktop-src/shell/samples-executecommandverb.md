---
description: Viene illustrato come implementare un verbo della shell utilizzando il metodo ExecuteCommand.
title: Esempio di verbo del comando Execute
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234213"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="a37d8-103">Esempio di verbo del comando Execute</span><span class="sxs-lookup"><span data-stu-id="a37d8-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="a37d8-104">Viene illustrato come implementare un verbo della shell utilizzando il metodo ExecuteCommand.</span><span class="sxs-lookup"><span data-stu-id="a37d8-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="a37d8-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a37d8-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a37d8-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a37d8-106">Description</span></span>](#description)
-   [<span data-ttu-id="a37d8-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a37d8-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a37d8-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a37d8-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a37d8-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a37d8-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a37d8-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a37d8-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="a37d8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a37d8-111">Description</span></span>

<span data-ttu-id="a37d8-112">Questo metodo è preferibile per le implementazioni di verbi perché offre la massima flessibilità, è semplice e supporta l'attivazione out-of-process.</span><span class="sxs-lookup"><span data-stu-id="a37d8-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="a37d8-113">In questo esempio viene implementato un oggetto server locale Component Object Model (COM) autonomo, ma si prevede che l'implementazione del verbo verrà integrata nelle applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="a37d8-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="a37d8-114">A tale scopo, l'oggetto applicazione principale deve registrare un class factory per se stesso.</span><span class="sxs-lookup"><span data-stu-id="a37d8-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="a37d8-115">Tale oggetto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per i verbi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a37d8-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="a37d8-116">Si noti che COM avvia l'applicazione se non è già in esecuzione, ma si connette a un'istanza in esecuzione dell'applicazione, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="a37d8-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="a37d8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a37d8-117">Requirements</span></span>



| <span data-ttu-id="a37d8-118">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a37d8-118">Product</span></span>                                | <span data-ttu-id="a37d8-119">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="a37d8-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a37d8-120">Windows</span><span class="sxs-lookup"><span data-stu-id="a37d8-120">Windows</span></span>                                | <span data-ttu-id="a37d8-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a37d8-121">Windows 7</span></span>               |
| <span data-ttu-id="a37d8-122">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="a37d8-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a37d8-123">7.0</span><span class="sxs-lookup"><span data-stu-id="a37d8-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a37d8-124">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a37d8-124">Downloading the Sample</span></span>

| <span data-ttu-id="a37d8-125">Location</span><span class="sxs-lookup"><span data-stu-id="a37d8-125">Location</span></span>      | <span data-ttu-id="a37d8-126">URL percorso</span><span class="sxs-lookup"><span data-stu-id="a37d8-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a37d8-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="a37d8-127">GitHub</span></span>  | [<span data-ttu-id="a37d8-128">Esempio ExecuteCommandVerb</span><span class="sxs-lookup"><span data-stu-id="a37d8-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="a37d8-129">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a37d8-129">Building the Sample</span></span>

<span data-ttu-id="a37d8-130">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="a37d8-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="a37d8-131">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="a37d8-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="a37d8-132">Immettere `msbuild ExecuteCommand.sln`.</span><span class="sxs-lookup"><span data-stu-id="a37d8-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="a37d8-133">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="a37d8-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="a37d8-134">Aprire Esplora risorse e passare alla directory del progetto **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="a37d8-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="a37d8-135">Fare doppio clic sull'icona per il file ExecuteCommand. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a37d8-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="a37d8-136">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="a37d8-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a37d8-137">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a37d8-137">Running the Sample</span></span>

1.  <span data-ttu-id="a37d8-138">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="a37d8-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="a37d8-139">Nella riga di comando, immettere `ExecuteCommand.exe` .</span><span class="sxs-lookup"><span data-stu-id="a37d8-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="a37d8-140">In alternativa, in Esplora risorse fare doppio clic sull'icona per ExecuteCommand.exe.</span><span class="sxs-lookup"><span data-stu-id="a37d8-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="a37d8-141">Seguire le istruzioni riportate nella finestra di dialogo visualizzata</span><span class="sxs-lookup"><span data-stu-id="a37d8-141">Follow the instructions in the displayed dialog</span></span>

 

 

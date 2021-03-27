---
description: Viene illustrato come creare un verbo che opera su elementi e contenitori della shell che riproduce elementi o aggiunge elementi a una coda.
title: Esempio di verbo del lettore
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231924"
---
# <a name="player-verb-sample"></a><span data-ttu-id="ca0c9-103">Esempio di verbo del lettore</span><span class="sxs-lookup"><span data-stu-id="ca0c9-103">Player Verb Sample</span></span>

<span data-ttu-id="ca0c9-104">Viene illustrato come creare un verbo che opera su elementi e contenitori della shell che riproduce elementi o aggiunge elementi a una coda.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="ca0c9-105">Questo esempio è particolarmente utile per le applicazioni multimediali.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="ca0c9-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ca0c9-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca0c9-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ca0c9-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca0c9-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ca0c9-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca0c9-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ca0c9-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca0c9-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="ca0c9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca0c9-111">Requirements</span></span>



| <span data-ttu-id="ca0c9-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ca0c9-112">Product</span></span>                                | <span data-ttu-id="ca0c9-113">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="ca0c9-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="ca0c9-114">Windows</span><span class="sxs-lookup"><span data-stu-id="ca0c9-114">Windows</span></span>                                | <span data-ttu-id="ca0c9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca0c9-115">Windows Vista</span></span>           |
| <span data-ttu-id="ca0c9-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="ca0c9-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="ca0c9-117">7.0</span><span class="sxs-lookup"><span data-stu-id="ca0c9-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ca0c9-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca0c9-118">Downloading the Sample</span></span>

| <span data-ttu-id="ca0c9-119">Location</span><span class="sxs-lookup"><span data-stu-id="ca0c9-119">Location</span></span>      | <span data-ttu-id="ca0c9-120">URL percorso</span><span class="sxs-lookup"><span data-stu-id="ca0c9-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0c9-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="ca0c9-121">GitHub</span></span>  | [<span data-ttu-id="ca0c9-122">Esempio PlayerVerb</span><span class="sxs-lookup"><span data-stu-id="ca0c9-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="ca0c9-123">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca0c9-123">Building the Sample</span></span>

<span data-ttu-id="ca0c9-124">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="ca0c9-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="ca0c9-125">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="ca0c9-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="ca0c9-126">Immettere `msbuild PlayerVerbSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="ca0c9-127">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="ca0c9-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="ca0c9-128">Aprire Esplora risorse e passare alla directory del progetto **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="ca0c9-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="ca0c9-129">Fare doppio clic sull'icona per il file PlayerVerbSample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="ca0c9-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="ca0c9-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ca0c9-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ca0c9-131">Running the Sample</span></span>

1.  <span data-ttu-id="ca0c9-132">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="ca0c9-133">Nella riga di comando, immettere `PlayerVerbSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="ca0c9-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="ca0c9-134">In alternativa, in Esplora risorse fare doppio clic sull'icona per PlayerVerbSample.exe.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="ca0c9-135">Selezionare `Register Verbs` nella finestra di dialogo **Sample verbi Player** .</span><span class="sxs-lookup"><span data-stu-id="ca0c9-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="ca0c9-136">Fare clic con il pulsante destro del mouse su elementi immagine (file, cartella o stack) in Esplora risorse per aggiungerli a una coda o riprodurli nell'applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="ca0c9-137">Usare gli elementi musicali quando si modifica l'esempio per lavorare con musica.</span><span class="sxs-lookup"><span data-stu-id="ca0c9-137">Use music items when you change the sample to work with music.</span></span>

 

 




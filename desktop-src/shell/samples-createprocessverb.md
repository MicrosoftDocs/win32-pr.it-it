---
description: Viene illustrato come implementare un verbo della shell utilizzando il metodo CreateProcess.
title: Esempio di verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980330"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="946a0-103">Esempio di verbo CreateProcess</span><span class="sxs-lookup"><span data-stu-id="946a0-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="946a0-104">Viene illustrato come implementare un verbo della shell utilizzando il metodo CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="946a0-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="946a0-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="946a0-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="946a0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="946a0-106">Description</span></span>](#description)
-   [<span data-ttu-id="946a0-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="946a0-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="946a0-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="946a0-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="946a0-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="946a0-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="946a0-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="946a0-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="946a0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="946a0-111">Description</span></span>

<span data-ttu-id="946a0-112">I verbi basati su CreateProcess dipendono dall'esecuzione di un eseguibile e dal passaggio di un argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="946a0-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="946a0-113">Questo metodo non è altrettanto efficace dei metodi DropTarget e ExecuteCommand, ma consente di ottenere il comportamento out-of-process auspicabile.</span><span class="sxs-lookup"><span data-stu-id="946a0-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="946a0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="946a0-114">Requirements</span></span>



| <span data-ttu-id="946a0-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="946a0-115">Product</span></span>                                | <span data-ttu-id="946a0-116">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="946a0-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="946a0-117">Windows</span><span class="sxs-lookup"><span data-stu-id="946a0-117">Windows</span></span>                                | <span data-ttu-id="946a0-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="946a0-118">Windows Vista</span></span>           |
| <span data-ttu-id="946a0-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="946a0-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="946a0-120">7.0</span><span class="sxs-lookup"><span data-stu-id="946a0-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="946a0-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="946a0-121">Downloading the Sample</span></span>

| <span data-ttu-id="946a0-122">Location</span><span class="sxs-lookup"><span data-stu-id="946a0-122">Location</span></span>      | <span data-ttu-id="946a0-123">URL percorso</span><span class="sxs-lookup"><span data-stu-id="946a0-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946a0-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="946a0-124">GitHub</span></span>  | [<span data-ttu-id="946a0-125">Esempio CreateProcessVerb</span><span class="sxs-lookup"><span data-stu-id="946a0-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="946a0-126">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="946a0-126">Building the Sample</span></span>

<span data-ttu-id="946a0-127">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="946a0-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="946a0-128">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="946a0-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="946a0-129">Immettere `msbuild CreateProcessVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="946a0-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="946a0-130">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="946a0-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="946a0-131">Aprire Esplora risorse e passare alla directory del progetto **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="946a0-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="946a0-132">Fare doppio clic sull'icona per il file CreateProcessVerb. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="946a0-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="946a0-133">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="946a0-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="946a0-134">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="946a0-134">Running the Sample</span></span>

1.  <span data-ttu-id="946a0-135">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="946a0-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="946a0-136">Nella riga di comando, immettere `CreateProcessVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="946a0-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="946a0-137">In alternativa, in Esplora risorse fare doppio clic sull'icona per CreateProcessVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="946a0-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="946a0-138">Seguire le istruzioni riportate nella finestra di dialogo visualizzata</span><span class="sxs-lookup"><span data-stu-id="946a0-138">Follow the instructions in the displayed dialog</span></span>

 

 




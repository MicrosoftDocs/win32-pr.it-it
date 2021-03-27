---
description: Viene illustrato come implementare un verbo della shell utilizzando i metodi ExplorerCommand e ExplorerCommandState.
title: Esempio di verbo del comando Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884949"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="6c31d-103">Esempio di verbo del comando Explorer</span><span class="sxs-lookup"><span data-stu-id="6c31d-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="6c31d-104">Viene illustrato come implementare un verbo della shell utilizzando i metodi ExplorerCommand e ExplorerCommandState.</span><span class="sxs-lookup"><span data-stu-id="6c31d-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="6c31d-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c31d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6c31d-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c31d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6c31d-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c31d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6c31d-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c31d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6c31d-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c31d-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6c31d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c31d-110">Requirements</span></span>



| <span data-ttu-id="6c31d-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6c31d-111">Product</span></span>                                | <span data-ttu-id="6c31d-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="6c31d-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6c31d-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6c31d-113">Windows</span></span>                                | <span data-ttu-id="6c31d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c31d-114">Windows Vista</span></span>           |
| <span data-ttu-id="6c31d-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="6c31d-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6c31d-116">7.0</span><span class="sxs-lookup"><span data-stu-id="6c31d-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6c31d-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c31d-117">Downloading the Sample</span></span>

| <span data-ttu-id="6c31d-118">Location</span><span class="sxs-lookup"><span data-stu-id="6c31d-118">Location</span></span>      | <span data-ttu-id="6c31d-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="6c31d-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c31d-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="6c31d-120">GitHub</span></span>  | [<span data-ttu-id="6c31d-121">Esempio ExplorerCommandVerb</span><span class="sxs-lookup"><span data-stu-id="6c31d-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="6c31d-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c31d-122">Building the Sample</span></span>

<span data-ttu-id="6c31d-123">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="6c31d-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="6c31d-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="6c31d-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="6c31d-125">Immettere `msbuild ExplorerCommandVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="6c31d-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="6c31d-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="6c31d-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="6c31d-127">Aprire Esplora risorse e passare alla directory del progetto **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="6c31d-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="6c31d-128">Fare doppio clic sull'icona per il file ExplorerCommandVerb. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6c31d-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="6c31d-129">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="6c31d-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6c31d-130">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c31d-130">Running the Sample</span></span>

1.  <span data-ttu-id="6c31d-131">Passare alla directory che contiene il ExplorerCommandVerb.dll, usando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="6c31d-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="6c31d-132">Assicurarsi di usare il file DLL a 64 bit in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6c31d-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="6c31d-133">Nella riga di comando, immettere `regsvr32.exe ExplorerCommandVerb.dll` .</span><span class="sxs-lookup"><span data-stu-id="6c31d-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="6c31d-134">Due nuovi verbi verranno visualizzati nel menu di scelta rapida quando si fa clic con il pulsante destro del mouse su un file con estensione txt.</span><span class="sxs-lookup"><span data-stu-id="6c31d-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 




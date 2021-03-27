---
description: Viene illustrato come estendere il menu di scelta rapida del trascinamento della selezione (talvolta definito menu di scelta rapida).
title: Esempio NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347931"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="95118-103">Esempio NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="95118-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="95118-104">Viene illustrato come estendere il menu di scelta rapida del trascinamento della selezione (talvolta definito menu di scelta rapida).</span><span class="sxs-lookup"><span data-stu-id="95118-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="95118-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="95118-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="95118-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95118-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="95118-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="95118-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="95118-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="95118-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="95118-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="95118-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="95118-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95118-110">Requirements</span></span>



| <span data-ttu-id="95118-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="95118-111">Product</span></span>                                | <span data-ttu-id="95118-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="95118-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="95118-113">Windows</span><span class="sxs-lookup"><span data-stu-id="95118-113">Windows</span></span>                                | <span data-ttu-id="95118-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95118-114">Windows Vista</span></span>           |
| <span data-ttu-id="95118-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="95118-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="95118-116">7.0</span><span class="sxs-lookup"><span data-stu-id="95118-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="95118-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="95118-117">Downloading the Sample</span></span>

| <span data-ttu-id="95118-118">Location</span><span class="sxs-lookup"><span data-stu-id="95118-118">Location</span></span>      | <span data-ttu-id="95118-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="95118-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95118-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="95118-120">GitHub</span></span>  | [<span data-ttu-id="95118-121">Esempio NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="95118-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="95118-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="95118-122">Building the Sample</span></span>

<span data-ttu-id="95118-123">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="95118-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="95118-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="95118-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="95118-125">Immettere `msbuild NonDefaultDropMenuVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="95118-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="95118-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="95118-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="95118-127">Aprire Esplora risorse e passare alla directory del progetto **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="95118-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="95118-128">Fare doppio clic sull'icona per il file NonDefaultDropMenuVerb. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="95118-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="95118-129">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="95118-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="95118-130">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="95118-130">Running the Sample</span></span>

1.  <span data-ttu-id="95118-131">Passare alla directory che contiene il nuovo file DLL, usando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="95118-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="95118-132">Copiare NonDefaultDropMenuVerb.dll nella directory di sistema, ad esempio C: \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="95118-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="95118-133">Al prompt dei comandi immettere `regedit NonDefaultDropMenuVerb.reg` .</span><span class="sxs-lookup"><span data-stu-id="95118-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="95118-134">Usare il pulsante destro del mouse per trascinare un file da una cartella a un'altra.</span><span class="sxs-lookup"><span data-stu-id="95118-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="95118-135">Vengono visualizzate altre voci di menu per l'operazione DROP.</span><span class="sxs-lookup"><span data-stu-id="95118-135">You will see additional menu items for the drop operation.</span></span>

 

 




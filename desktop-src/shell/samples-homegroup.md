---
description: Viene illustrato come determinare lo stato di appartenenza del gruppo Home, enumerare gli elementi di primo livello nella cartella della shell del gruppo Home e avviare la condivisione guidata Gruppo Home.
title: Esempio di HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050180"
---
# <a name="homegroup-sample"></a><span data-ttu-id="cfa5d-103">Esempio di HomeGroup</span><span class="sxs-lookup"><span data-stu-id="cfa5d-103">HomeGroup Sample</span></span>

<span data-ttu-id="cfa5d-104">Viene illustrato come determinare lo stato di appartenenza del gruppo Home, enumerare gli elementi di primo livello nella cartella della shell del **Gruppo Home** e avviare la **condivisione guidata Gruppo Home**.</span><span class="sxs-lookup"><span data-stu-id="cfa5d-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="cfa5d-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cfa5d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cfa5d-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfa5d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cfa5d-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cfa5d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="cfa5d-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cfa5d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="cfa5d-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cfa5d-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="cfa5d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfa5d-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="cfa5d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfa5d-111">Requirements</span></span>



| <span data-ttu-id="cfa5d-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="cfa5d-112">Product</span></span>                                | <span data-ttu-id="cfa5d-113">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="cfa5d-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="cfa5d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="cfa5d-114">Windows</span></span>                                | <span data-ttu-id="cfa5d-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cfa5d-115">Windows 7</span></span>               |
| <span data-ttu-id="cfa5d-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="cfa5d-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="cfa5d-117">7.0</span><span class="sxs-lookup"><span data-stu-id="cfa5d-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="cfa5d-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cfa5d-118">Downloading the Sample</span></span>

| <span data-ttu-id="cfa5d-119">Location</span><span class="sxs-lookup"><span data-stu-id="cfa5d-119">Location</span></span>      | <span data-ttu-id="cfa5d-120">URL percorso</span><span class="sxs-lookup"><span data-stu-id="cfa5d-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa5d-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="cfa5d-121">GitHub</span></span>  | [<span data-ttu-id="cfa5d-122">Esempio gruppo Home</span><span class="sxs-lookup"><span data-stu-id="cfa5d-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="cfa5d-123">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cfa5d-123">Building the Sample</span></span>

<span data-ttu-id="cfa5d-124">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="cfa5d-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="cfa5d-125">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **Gruppo Home** .</span><span class="sxs-lookup"><span data-stu-id="cfa5d-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="cfa5d-126">Immettere `msbuild HomeGroup.sln`.</span><span class="sxs-lookup"><span data-stu-id="cfa5d-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="cfa5d-127">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="cfa5d-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="cfa5d-128">Aprire Esplora risorse e passare alla directory del progetto **Gruppo Home** .</span><span class="sxs-lookup"><span data-stu-id="cfa5d-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="cfa5d-129">Fare doppio clic sull'icona del file HomeGroup. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cfa5d-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="cfa5d-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="cfa5d-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cfa5d-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cfa5d-131">Running the Sample</span></span>

1.  <span data-ttu-id="cfa5d-132">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="cfa5d-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="cfa5d-133">Nella riga di comando, immettere `HomeGroup.exe` .</span><span class="sxs-lookup"><span data-stu-id="cfa5d-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="cfa5d-134">In alternativa, in Esplora risorse fare doppio clic sull'icona per HomeGroup.exe.</span><span class="sxs-lookup"><span data-stu-id="cfa5d-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfa5d-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfa5d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfa5d-136">**IHomeGroup**</span><span class="sxs-lookup"><span data-stu-id="cfa5d-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="cfa5d-137">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="cfa5d-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 




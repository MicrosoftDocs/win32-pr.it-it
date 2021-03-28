---
description: Viene illustrato come un'applicazione può esporre più destinazioni switch (come per le tabulazioni) in un TaskBand e come fornire le relative anteprime.
title: Esempio TabThumbnails
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980746"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="33179-103">Esempio TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="33179-103">TabThumbnails Sample</span></span>

<span data-ttu-id="33179-104">Viene illustrato come un'applicazione può esporre più destinazioni switch (come per le tabulazioni) in un TaskBand e come fornire le relative anteprime.</span><span class="sxs-lookup"><span data-stu-id="33179-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="33179-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="33179-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="33179-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33179-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="33179-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="33179-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="33179-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="33179-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="33179-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="33179-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="33179-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33179-110">Requirements</span></span>



| <span data-ttu-id="33179-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="33179-111">Product</span></span>                                | <span data-ttu-id="33179-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="33179-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="33179-113">Windows</span><span class="sxs-lookup"><span data-stu-id="33179-113">Windows</span></span>                                | <span data-ttu-id="33179-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33179-114">Windows 7</span></span>               |
| <span data-ttu-id="33179-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="33179-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="33179-116">7.0</span><span class="sxs-lookup"><span data-stu-id="33179-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="33179-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="33179-117">Downloading the Sample</span></span>

| <span data-ttu-id="33179-118">Location</span><span class="sxs-lookup"><span data-stu-id="33179-118">Location</span></span>      | <span data-ttu-id="33179-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="33179-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33179-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="33179-120">GitHub</span></span>  | [<span data-ttu-id="33179-121">Esempio TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="33179-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="33179-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="33179-122">Building the Sample</span></span>

<span data-ttu-id="33179-123">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="33179-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="33179-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="33179-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="33179-125">Immettere `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="33179-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="33179-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="33179-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="33179-127">Aprire Esplora risorse e passare alla directory del progetto **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="33179-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="33179-128">Fare doppio clic sull'icona per il file TabThumbnails. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="33179-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="33179-129">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="33179-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="33179-130">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="33179-130">Running the Sample</span></span>

1.  <span data-ttu-id="33179-131">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="33179-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="33179-132">Nella riga di comando, immettere `TabThumbnails.exe` .</span><span class="sxs-lookup"><span data-stu-id="33179-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="33179-133">In alternativa, in Esplora risorse fare doppio clic sull'icona per TabThumbnails.exe.</span><span class="sxs-lookup"><span data-stu-id="33179-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 




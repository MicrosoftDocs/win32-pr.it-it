---
description: Viene illustrato come aggiungere elementi alla Jump List automatica per un'applicazione, incluso il passaggio tra la visualizzazione delle categorie frequenti e recenti.
title: Esempio di jump list automatica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485564"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="27c6a-103">Esempio di jump list automatica</span><span class="sxs-lookup"><span data-stu-id="27c6a-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="27c6a-104">Viene illustrato come aggiungere elementi alla Jump List automatica per un'applicazione, incluso il passaggio tra la visualizzazione delle categorie frequenti e recenti.</span><span class="sxs-lookup"><span data-stu-id="27c6a-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="27c6a-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="27c6a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="27c6a-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c6a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="27c6a-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="27c6a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="27c6a-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="27c6a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="27c6a-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="27c6a-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="27c6a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27c6a-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="27c6a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c6a-111">Requirements</span></span>



| <span data-ttu-id="27c6a-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="27c6a-112">Product</span></span>                                | <span data-ttu-id="27c6a-113">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="27c6a-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="27c6a-114">Windows</span><span class="sxs-lookup"><span data-stu-id="27c6a-114">Windows</span></span>                                | <span data-ttu-id="27c6a-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27c6a-115">Windows 7</span></span>               |
| <span data-ttu-id="27c6a-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="27c6a-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="27c6a-117">7.0</span><span class="sxs-lookup"><span data-stu-id="27c6a-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="27c6a-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="27c6a-118">Downloading the Sample</span></span>

| <span data-ttu-id="27c6a-119">Location</span><span class="sxs-lookup"><span data-stu-id="27c6a-119">Location</span></span>      | <span data-ttu-id="27c6a-120">URL percorso</span><span class="sxs-lookup"><span data-stu-id="27c6a-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c6a-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="27c6a-121">GitHub</span></span>  | [<span data-ttu-id="27c6a-122">Esempio AutomaticJumpList</span><span class="sxs-lookup"><span data-stu-id="27c6a-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="27c6a-123">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="27c6a-123">Building the Sample</span></span>

<span data-ttu-id="27c6a-124">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="27c6a-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="27c6a-125">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="27c6a-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="27c6a-126">Immettere `msbuild AutomaticJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="27c6a-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="27c6a-127">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="27c6a-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="27c6a-128">Aprire Esplora risorse e passare alla directory del progetto **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="27c6a-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="27c6a-129">Fare doppio clic sull'icona per il file AutomaticJumpListSample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="27c6a-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="27c6a-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="27c6a-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="27c6a-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="27c6a-131">Running the Sample</span></span>

1.  <span data-ttu-id="27c6a-132">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="27c6a-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="27c6a-133">Nella riga di comando, immettere `AutomaticJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="27c6a-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="27c6a-134">In alternativa, in Esplora risorse fare doppio clic sull'icona per AutomaticJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="27c6a-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="27c6a-135">Questo esempio deve essere eseguito come amministratore alla prima esecuzione, in modo da poter installare le registrazioni dei tipi di file necessarie.</span><span class="sxs-lookup"><span data-stu-id="27c6a-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="27c6a-136">Dopo la registrazione dei tipi di file, l'esempio può essere eseguito come utente standard.</span><span class="sxs-lookup"><span data-stu-id="27c6a-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="27c6a-137">Scegliere Opzioni dal menu nell'applicazione di esempio, inclusa la selezione dei documenti con estensione txt o doc tramite la finestra di dialogo **Apri** per vedere come influiscono sulla Jump List dell'applicazione nella barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="27c6a-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27c6a-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27c6a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c6a-139">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="27c6a-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 




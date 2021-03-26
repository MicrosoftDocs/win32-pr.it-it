---
description: Viene illustrato come creare una Jump List personalizzata per un'applicazione, tra cui l'aggiunta di una categoria e attività personalizzate.
title: Esempio di jump list personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232710"
---
# <a name="custom-jump-list-sample"></a><span data-ttu-id="c8811-103">Esempio di jump list personalizzata</span><span class="sxs-lookup"><span data-stu-id="c8811-103">Custom Jump List Sample</span></span>

<span data-ttu-id="c8811-104">Viene illustrato come creare una Jump List personalizzata per un'applicazione, tra cui l'aggiunta di una categoria e attività personalizzate.</span><span class="sxs-lookup"><span data-stu-id="c8811-104">Demonstrates how to create a custom Jump List for an application, including adding a custom category and tasks.</span></span>

<span data-ttu-id="c8811-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8811-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c8811-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8811-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c8811-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c8811-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c8811-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c8811-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c8811-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c8811-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c8811-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8811-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c8811-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8811-111">Requirements</span></span>



| <span data-ttu-id="c8811-112">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c8811-112">Product</span></span>                                | <span data-ttu-id="c8811-113">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="c8811-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c8811-114">Windows</span><span class="sxs-lookup"><span data-stu-id="c8811-114">Windows</span></span>                                | <span data-ttu-id="c8811-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8811-115">Windows 7</span></span>               |
| <span data-ttu-id="c8811-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c8811-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c8811-117">7.0</span><span class="sxs-lookup"><span data-stu-id="c8811-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c8811-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c8811-118">Downloading the Sample</span></span>

| <span data-ttu-id="c8811-119">Location</span><span class="sxs-lookup"><span data-stu-id="c8811-119">Location</span></span>      | <span data-ttu-id="c8811-120">URL percorso</span><span class="sxs-lookup"><span data-stu-id="c8811-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8811-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="c8811-121">GitHub</span></span>  | [<span data-ttu-id="c8811-122">Esempio CustomJumpList</span><span class="sxs-lookup"><span data-stu-id="c8811-122">CustomJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="c8811-123">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c8811-123">Building the Sample</span></span>

<span data-ttu-id="c8811-124">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c8811-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="c8811-125">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="c8811-125">Open the command prompt window and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="c8811-126">Immettere `msbuild CustomJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="c8811-126">Enter `msbuild CustomJumpListSample.sln`.</span></span>

<span data-ttu-id="c8811-127">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="c8811-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c8811-128">Aprire Esplora risorse e passare alla directory del progetto **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="c8811-128">Open Windows Explorer and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="c8811-129">Fare doppio clic sull'icona per il file CustomJumpListSample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c8811-129">Double-click the icon for the CustomJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="c8811-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="c8811-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c8811-131">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c8811-131">Running the Sample</span></span>

1.  <span data-ttu-id="c8811-132">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c8811-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="c8811-133">Nella riga di comando, immettere `CustomJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="c8811-133">At the command line, enter `CustomJumpListSample.exe`.</span></span> <span data-ttu-id="c8811-134">In alternativa, in Esplora risorse fare doppio clic sull'icona per CustomJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="c8811-134">Alternatively, from Windows Explorer double-click the icon for CustomJumpListSample.exe.</span></span>
3.  <span data-ttu-id="c8811-135">Questo esempio deve essere eseguito come amministratore alla prima esecuzione, in modo da poter installare le registrazioni dei tipi di file necessarie.</span><span class="sxs-lookup"><span data-stu-id="c8811-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="c8811-136">Dopo la registrazione dei tipi di file, l'esempio può essere eseguito come utente standard.</span><span class="sxs-lookup"><span data-stu-id="c8811-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="c8811-137">Scegliere Opzioni dal menu nell'applicazione di esempio per vedere come influiscono sulla Jump List dell'applicazione nella barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c8811-137">Select options from the menu in the sample application to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8811-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8811-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8811-139">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="c8811-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 




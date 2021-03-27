---
description: Viene illustrato come enumerare le librerie come contenitori.
title: Esempio di backup della libreria shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980759"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="731a8-103">Esempio di backup della libreria shell</span><span class="sxs-lookup"><span data-stu-id="731a8-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="731a8-104">Viene illustrato come enumerare le librerie come contenitori.</span><span class="sxs-lookup"><span data-stu-id="731a8-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="731a8-105">Le librerie sono il nuovo paradigma di archiviazione per i file utente e sono introdotti in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="731a8-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="731a8-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="731a8-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="731a8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="731a8-107">Description</span></span>](#description)
-   [<span data-ttu-id="731a8-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="731a8-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="731a8-109">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="731a8-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="731a8-110">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="731a8-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="731a8-111">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="731a8-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="731a8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="731a8-112">Description</span></span>

<span data-ttu-id="731a8-113">Questo esempio è un'applicazione di backup fittizio che Mostra come selezionare le librerie tramite la finestra di dialogo file comune.</span><span class="sxs-lookup"><span data-stu-id="731a8-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="731a8-114">Viene inoltre illustrato come eseguire il backup delle librerie utilizzando lo spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="731a8-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="731a8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="731a8-115">Requirements</span></span>



| <span data-ttu-id="731a8-116">Prodotto</span><span class="sxs-lookup"><span data-stu-id="731a8-116">Product</span></span>                                | <span data-ttu-id="731a8-117">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="731a8-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="731a8-118">Windows</span><span class="sxs-lookup"><span data-stu-id="731a8-118">Windows</span></span>                                | <span data-ttu-id="731a8-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="731a8-119">Windows 7</span></span>               |
| <span data-ttu-id="731a8-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="731a8-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="731a8-121">7.0</span><span class="sxs-lookup"><span data-stu-id="731a8-121">7.0</span></span>                     |



 

<span data-ttu-id="731a8-122">Per ulteriori requisiti, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="731a8-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="731a8-123">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="731a8-123">Downloading the Sample</span></span>

| <span data-ttu-id="731a8-124">Location</span><span class="sxs-lookup"><span data-stu-id="731a8-124">Location</span></span>      | <span data-ttu-id="731a8-125">URL percorso</span><span class="sxs-lookup"><span data-stu-id="731a8-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731a8-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="731a8-126">GitHub</span></span>  | [<span data-ttu-id="731a8-127">Esempio ShellLibraryBackup</span><span class="sxs-lookup"><span data-stu-id="731a8-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="731a8-128">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="731a8-128">Building the Sample</span></span>

<span data-ttu-id="731a8-129">Per istruzioni su come compilare l'esempio, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="731a8-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="731a8-130">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="731a8-130">Running the Sample</span></span>

<span data-ttu-id="731a8-131">Per istruzioni su come compilare l'esempio, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="731a8-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 




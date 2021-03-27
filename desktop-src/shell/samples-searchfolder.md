---
description: Viene illustrato come creare una ricerca con vincoli di query utilizzando il modello di programmazione della shell.
title: Esempio di cartella di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232490"
---
# <a name="search-folder-sample"></a><span data-ttu-id="12963-103">Esempio di cartella di ricerca</span><span class="sxs-lookup"><span data-stu-id="12963-103">Search Folder Sample</span></span>

<span data-ttu-id="12963-104">Viene illustrato come creare una ricerca con vincoli di query utilizzando il modello di programmazione della shell.</span><span class="sxs-lookup"><span data-stu-id="12963-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="12963-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="12963-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12963-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12963-106">Description</span></span>](#description)
-   [<span data-ttu-id="12963-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12963-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="12963-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="12963-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="12963-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="12963-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="12963-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="12963-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="12963-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12963-111">Description</span></span>

<span data-ttu-id="12963-112">In questo esempio viene illustrato come creare una ricerca vincolata utilizzando l'interfaccia [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) per costruire un elemento della shell di cartelle (un contenitore) che rappresenta la query.</span><span class="sxs-lookup"><span data-stu-id="12963-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="12963-113">I risultati vengono visualizzati utilizzando la finestra di dialogo Apri file.</span><span class="sxs-lookup"><span data-stu-id="12963-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="12963-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12963-114">Requirements</span></span>



| <span data-ttu-id="12963-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="12963-115">Product</span></span>                                | <span data-ttu-id="12963-116">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="12963-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="12963-117">Windows</span><span class="sxs-lookup"><span data-stu-id="12963-117">Windows</span></span>                                | <span data-ttu-id="12963-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12963-118">Windows Vista</span></span>           |
| <span data-ttu-id="12963-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="12963-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="12963-120">7.0</span><span class="sxs-lookup"><span data-stu-id="12963-120">7.0</span></span>                     |



 

<span data-ttu-id="12963-121">Per ulteriori requisiti, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="12963-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="12963-122">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="12963-122">Downloading the Sample</span></span>

| <span data-ttu-id="12963-123">Location</span><span class="sxs-lookup"><span data-stu-id="12963-123">Location</span></span>      | <span data-ttu-id="12963-124">URL percorso</span><span class="sxs-lookup"><span data-stu-id="12963-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12963-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="12963-125">GitHub</span></span>  | [<span data-ttu-id="12963-126">Esempio SearchFolder</span><span class="sxs-lookup"><span data-stu-id="12963-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="12963-127">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="12963-127">Building the Sample</span></span>

<span data-ttu-id="12963-128">Per istruzioni su come compilare l'esempio, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="12963-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="12963-129">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="12963-129">Running the Sample</span></span>

<span data-ttu-id="12963-130">Per istruzioni su come compilare l'esempio, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="12963-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 




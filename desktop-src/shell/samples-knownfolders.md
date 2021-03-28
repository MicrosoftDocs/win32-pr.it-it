---
description: Viene illustrato come definire, registrare, enumerare e trovare il percorso per tutte le cartelle note nel sistema corrente.
title: Esempio di cartelle note
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 49799A9E-BA86-4977-B5F3-590BE1E5FBF6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d3784e64986a338f6554534199852191bd06ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967748"
---
# <a name="known-folders-sample"></a><span data-ttu-id="f1be0-103">Esempio di cartelle note</span><span class="sxs-lookup"><span data-stu-id="f1be0-103">Known Folders Sample</span></span>

<span data-ttu-id="f1be0-104">Viene illustrato come definire, registrare, enumerare e trovare il percorso per tutte le cartelle note nel sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="f1be0-104">Demonstrates how to define, register, enumerate and find the path for all known folders on the current system.</span></span>

<span data-ttu-id="f1be0-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1be0-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f1be0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1be0-106">Description</span></span>](#description)
-   [<span data-ttu-id="f1be0-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1be0-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f1be0-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f1be0-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f1be0-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f1be0-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f1be0-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f1be0-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f1be0-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1be0-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f1be0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1be0-112">Description</span></span>

<span data-ttu-id="f1be0-113">Questo esempio include un file del registro di sistema che illustra come registrare una cartella nota scrivendo alcune chiavi del registro di sistema e i valori comuni per gli sviluppatori che preferiscono l'accesso al registro.</span><span class="sxs-lookup"><span data-stu-id="f1be0-113">This sample includes a registry file that demonstrates how to register a known folder by writing some common registry keys and values for developers who prefer registry access.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1be0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1be0-114">Requirements</span></span>



| <span data-ttu-id="f1be0-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f1be0-115">Product</span></span>                                | <span data-ttu-id="f1be0-116">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="f1be0-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f1be0-117">Windows</span><span class="sxs-lookup"><span data-stu-id="f1be0-117">Windows</span></span>                                | <span data-ttu-id="f1be0-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1be0-118">Windows Vista</span></span>           |
| <span data-ttu-id="f1be0-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f1be0-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f1be0-120">6.1</span><span class="sxs-lookup"><span data-stu-id="f1be0-120">6.1</span></span>                     |



 

<span data-ttu-id="f1be0-121">Per ulteriori requisiti, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f1be0-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="f1be0-122">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f1be0-122">Downloading the Sample</span></span>

| <span data-ttu-id="f1be0-123">Location</span><span class="sxs-lookup"><span data-stu-id="f1be0-123">Location</span></span>      | <span data-ttu-id="f1be0-124">URL percorso</span><span class="sxs-lookup"><span data-stu-id="f1be0-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1be0-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="f1be0-125">GitHub</span></span>  | [<span data-ttu-id="f1be0-126">Esempio KnownFolders</span><span class="sxs-lookup"><span data-stu-id="f1be0-126">KnownFolders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/knownfolders) |

## <a name="building-the-sample"></a><span data-ttu-id="f1be0-127">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f1be0-127">Building the Sample</span></span>

<span data-ttu-id="f1be0-128">Per istruzioni su come compilare l'esempio, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f1be0-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f1be0-129">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f1be0-129">Running the Sample</span></span>

<span data-ttu-id="f1be0-130">Per istruzioni su come compilare l'esempio, vedere il file Leggimi incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f1be0-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1be0-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1be0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1be0-132">Cartelle note</span><span class="sxs-lookup"><span data-stu-id="f1be0-132">Known Folders</span></span>](known-folders.md)
</dt> </dl>

 

 




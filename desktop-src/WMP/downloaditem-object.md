---
title: Oggetto DownloadItem
description: Oggetto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player Online Stores, oggetto DownloadItem
- archivi online, oggetto DownloadItem
- digitare 2 archivi online, oggetto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298927"
---
# <a name="downloaditem-object"></a><span data-ttu-id="173e3-107">Oggetto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="173e3-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="173e3-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="173e3-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="173e3-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="173e3-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="173e3-110">L'oggetto **DownloadItem** rappresenta una richiesta di download del file.</span><span class="sxs-lookup"><span data-stu-id="173e3-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="173e3-111">Può essere usato da pagine Web ospitate in modalità Full Windows Media Player e che hanno accesso all'oggetto **esterno** , ad esempio servizi Premium.</span><span class="sxs-lookup"><span data-stu-id="173e3-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="173e3-112">L'oggetto **DownloadItem** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="173e3-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="173e3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="173e3-113">Property</span></span>                                        | <span data-ttu-id="173e3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="173e3-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="173e3-115">downloadState</span><span class="sxs-lookup"><span data-stu-id="173e3-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="173e3-116">Recupera lo stato del download.</span><span class="sxs-lookup"><span data-stu-id="173e3-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="173e3-117">corso</span><span class="sxs-lookup"><span data-stu-id="173e3-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="173e3-118">Recupera lo stato di avanzamento del download in byte.</span><span class="sxs-lookup"><span data-stu-id="173e3-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="173e3-119">size</span><span class="sxs-lookup"><span data-stu-id="173e3-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="173e3-120">Recupera le dimensioni del download.</span><span class="sxs-lookup"><span data-stu-id="173e3-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="173e3-121">sourceURL</span><span class="sxs-lookup"><span data-stu-id="173e3-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="173e3-122">Recupera l'URL di origine del download.</span><span class="sxs-lookup"><span data-stu-id="173e3-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="173e3-123">type</span><span class="sxs-lookup"><span data-stu-id="173e3-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="173e3-124">Recupera il tipo di download.</span><span class="sxs-lookup"><span data-stu-id="173e3-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="173e3-125">L'oggetto **DownloadItem** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="173e3-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="173e3-126">Metodo</span><span class="sxs-lookup"><span data-stu-id="173e3-126">Method</span></span>                                      | <span data-ttu-id="173e3-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="173e3-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="173e3-128">cancel</span><span class="sxs-lookup"><span data-stu-id="173e3-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="173e3-129">Annulla il download.</span><span class="sxs-lookup"><span data-stu-id="173e3-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="173e3-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="173e3-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="173e3-131">Recupera il valore di un attributo per l'elemento di download.</span><span class="sxs-lookup"><span data-stu-id="173e3-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="173e3-132">pause</span><span class="sxs-lookup"><span data-stu-id="173e3-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="173e3-133">Sospende il download.</span><span class="sxs-lookup"><span data-stu-id="173e3-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="173e3-134">riprendere</span><span class="sxs-lookup"><span data-stu-id="173e3-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="173e3-135">Riprende il download.</span><span class="sxs-lookup"><span data-stu-id="173e3-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="173e3-136">È possibile accedere all'oggetto **DownloadItem** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="173e3-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="173e3-137">Oggetto</span><span class="sxs-lookup"><span data-stu-id="173e3-137">Object</span></span>                                              | <span data-ttu-id="173e3-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="173e3-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="173e3-139">DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="173e3-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="173e3-140">item</span><span class="sxs-lookup"><span data-stu-id="173e3-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="173e3-141">Ai fini dell'illustrazione, **downloadmanager**. **Getdownloadcollection**(*CollectionId*). **Item**(*ItemId*) viene usato nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="173e3-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="173e3-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="173e3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="173e3-143">**Riferimento per negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="173e3-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





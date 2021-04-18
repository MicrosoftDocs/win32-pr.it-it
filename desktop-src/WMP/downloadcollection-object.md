---
title: Download (oggetto)
description: Download (oggetto)
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player Online Stores, oggetto DownloadCollection
- archivi online, oggetto DownloadCollection
- digitare 2 archivi online, oggetto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298533"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="53fd4-107">Download (oggetto)</span><span class="sxs-lookup"><span data-stu-id="53fd4-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="53fd4-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="53fd4-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="53fd4-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="53fd4-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="53fd4-110">L'oggetto **DownloadCollection** contiene proprietà e metodi per gestire le raccolte di elementi di download.</span><span class="sxs-lookup"><span data-stu-id="53fd4-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="53fd4-111">Può essere usato da pagine Web ospitate in modalità Full Windows Media Player e che hanno accesso all'oggetto **esterno** , ad esempio gli archivi online.</span><span class="sxs-lookup"><span data-stu-id="53fd4-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="53fd4-112">L'oggetto **DownloadCollection** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="53fd4-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="53fd4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53fd4-113">Property</span></span>                              | <span data-ttu-id="53fd4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53fd4-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="53fd4-115">count</span><span class="sxs-lookup"><span data-stu-id="53fd4-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="53fd4-116">Recupera il numero di download in sospeso.</span><span class="sxs-lookup"><span data-stu-id="53fd4-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="53fd4-117">id</span><span class="sxs-lookup"><span data-stu-id="53fd4-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="53fd4-118">Recupera l'ID della raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="53fd4-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="53fd4-119">L'oggetto **DownloadCollection** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="53fd4-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="53fd4-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="53fd4-120">Method</span></span>                                                | <span data-ttu-id="53fd4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53fd4-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="53fd4-122">Cancella</span><span class="sxs-lookup"><span data-stu-id="53fd4-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="53fd4-123">Rimuove tutti gli elementi da una raccolta di download.</span><span class="sxs-lookup"><span data-stu-id="53fd4-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="53fd4-124">item</span><span class="sxs-lookup"><span data-stu-id="53fd4-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="53fd4-125">Recupera un oggetto di download in sospeso.</span><span class="sxs-lookup"><span data-stu-id="53fd4-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="53fd4-126">removeItem</span><span class="sxs-lookup"><span data-stu-id="53fd4-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="53fd4-127">Rimuove un elemento di download da una raccolta.</span><span class="sxs-lookup"><span data-stu-id="53fd4-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="53fd4-128">startDownload</span><span class="sxs-lookup"><span data-stu-id="53fd4-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="53fd4-129">Accoda un download.</span><span class="sxs-lookup"><span data-stu-id="53fd4-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="53fd4-130">È possibile accedere all'oggetto **DownloadCollection** tramite i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="53fd4-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="53fd4-131">Oggetto</span><span class="sxs-lookup"><span data-stu-id="53fd4-131">Object</span></span>                                        | <span data-ttu-id="53fd4-132">Metodo</span><span class="sxs-lookup"><span data-stu-id="53fd4-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="53fd4-133">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="53fd4-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="53fd4-134">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="53fd4-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="53fd4-135">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="53fd4-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="53fd4-136">getdownloadcollection</span><span class="sxs-lookup"><span data-stu-id="53fd4-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="53fd4-137">Ai fini dell'illustrazione, **downloadmanager**. **Getdownloadcollection**(*CollectionId*) viene usato nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="53fd4-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53fd4-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53fd4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53fd4-139">**Riferimento per negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="53fd4-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





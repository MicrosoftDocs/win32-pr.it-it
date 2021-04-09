---
title: Oggetto DownloadManager
description: Oggetto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Online Stores, oggetto DownloadManager
- archivi online, oggetto DownloadManager
- digitare 2 archivi online, oggetto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856346"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="408f7-107">Oggetto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="408f7-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="408f7-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="408f7-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="408f7-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="408f7-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="408f7-110">L'oggetto **downloadmanager** è l'oggetto radice per gestione download di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="408f7-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="408f7-111">Può essere usato da pagine Web ospitate nei riquadri attività del servizio di archiviazione online.</span><span class="sxs-lookup"><span data-stu-id="408f7-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="408f7-112">L'oggetto **downloadmanager** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="408f7-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="408f7-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="408f7-113">Method</span></span>                                                                   | <span data-ttu-id="408f7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="408f7-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="408f7-115">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="408f7-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="408f7-116">Crea una raccolta di download vuota.</span><span class="sxs-lookup"><span data-stu-id="408f7-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="408f7-117">getdownloadcollection</span><span class="sxs-lookup"><span data-stu-id="408f7-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="408f7-118">Recupera la raccolta di download specificata.</span><span class="sxs-lookup"><span data-stu-id="408f7-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="408f7-119">È possibile accedere all'oggetto **downloadmanager** tramite **External. DownloadManager**.</span><span class="sxs-lookup"><span data-stu-id="408f7-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="408f7-120">A scopo illustrativo, si presuppone che questo valore sia stato assegnato a una variabile denominata "DownloadManager", che verrà usata per identificare questo oggetto nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="408f7-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="408f7-121">In Windows Media Player 10 o versioni successive, la proprietà e l'oggetto **downloadmanager** sono accessibili solo dai riquadri attività del servizio di archiviazione online.</span><span class="sxs-lookup"><span data-stu-id="408f7-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="408f7-122">Non è possibile usare **downloadmanager** da altre funzionalità in cui l'oggetto **esterno** è disponibile, ad esempio HtmlView, visualizzazione centro informazioni e informazioni sugli album.</span><span class="sxs-lookup"><span data-stu-id="408f7-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="408f7-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="408f7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="408f7-124">**Riferimento per negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="408f7-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





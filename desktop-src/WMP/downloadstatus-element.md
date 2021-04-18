---
title: Elemento DownloadStatus (msfeeds. h)
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Finestra elementi DownloadStatus Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329323"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="f082f-105">Elemento DownloadStatus</span><span class="sxs-lookup"><span data-stu-id="f082f-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="f082f-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="f082f-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f082f-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f082f-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f082f-108">L'elemento **downloadStatus** specifica un URL visualizzato da Windows Media Player come collegamento per consentire agli utenti di visualizzare lo stato del download.</span><span class="sxs-lookup"><span data-stu-id="f082f-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="f082f-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="f082f-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="f082f-110"><span id="URL"></span><span id="url"></span>URL</span><span class="sxs-lookup"><span data-stu-id="f082f-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="f082f-111">URL della pagina Web visualizzata dal negozio online per mostrare lo stato di download all'utente.</span><span class="sxs-lookup"><span data-stu-id="f082f-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="f082f-112">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="f082f-112">Parent/Child Elements</span></span>



| <span data-ttu-id="f082f-113">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="f082f-113">Hierarchy</span></span>       | <span data-ttu-id="f082f-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="f082f-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="f082f-115">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f082f-115">Parent elements</span></span> | <span data-ttu-id="f082f-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f082f-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="f082f-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f082f-117">Child elements</span></span>  | <span data-ttu-id="f082f-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="f082f-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="f082f-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f082f-119">Remarks</span></span>

<span data-ttu-id="f082f-120">Windows Media Player visualizza un messaggio agli utenti quando è in corso un download.</span><span class="sxs-lookup"><span data-stu-id="f082f-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="f082f-121">Se i servizi attivi correnti definiscono un URL di stato di download, l'utente può fare clic sul testo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="f082f-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="f082f-122">Quando l'utente fa clic sul messaggio, il lettore passa all'URL specificato dall'elemento **downloadStatus** in modo che l'archivio attivo corrente possa fornire informazioni dettagliate sui download in corso.</span><span class="sxs-lookup"><span data-stu-id="f082f-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="f082f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f082f-123">Requirements</span></span>



| <span data-ttu-id="f082f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f082f-124">Requirement</span></span> | <span data-ttu-id="f082f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f082f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f082f-126">Versione</span><span class="sxs-lookup"><span data-stu-id="f082f-126">Version</span></span><br/> | <span data-ttu-id="f082f-127">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f082f-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="f082f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f082f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f082f-129"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="f082f-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f082f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f082f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f082f-131">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f082f-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="f082f-132">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="f082f-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="f082f-133">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f082f-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






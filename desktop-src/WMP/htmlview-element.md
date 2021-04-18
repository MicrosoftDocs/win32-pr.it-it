---
title: Elemento HTMLView
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento HTMLView specifica l'URL di base di una pagina Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Finestra elementi HTMLView Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327876"
---
# <a name="htmlview-element"></a><span data-ttu-id="5dba8-106">Elemento HTMLView</span><span class="sxs-lookup"><span data-stu-id="5dba8-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="5dba8-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="5dba8-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5dba8-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5dba8-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5dba8-109">L'elemento **HtmlView** specifica l'URL di base di una pagina Web htmlview.</span><span class="sxs-lookup"><span data-stu-id="5dba8-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="5dba8-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="5dba8-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="5dba8-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseUrl** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="5dba8-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="5dba8-112">URL di base per la pagina Web HTMLView visualizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5dba8-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="5dba8-113">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="5dba8-113">Parent/Child Elements</span></span>



| <span data-ttu-id="5dba8-114">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="5dba8-114">Hierarchy</span></span>       | <span data-ttu-id="5dba8-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5dba8-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="5dba8-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5dba8-116">Parent elements</span></span> | <span data-ttu-id="5dba8-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5dba8-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="5dba8-118">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5dba8-118">Child elements</span></span>  | <span data-ttu-id="5dba8-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="5dba8-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="5dba8-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5dba8-120">Remarks</span></span>

<span data-ttu-id="5dba8-121">È possibile usare questo elemento per integrare la funzionalità HTMLView con il negozio online.</span><span class="sxs-lookup"><span data-stu-id="5dba8-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="5dba8-122">Se il dominio dell'URL specificato dall'archivio online corrente corrisponde a quello per la pagina Web HTMLView, l'opzione per la **riproduzione** avviene senza l'intervento dell'utente e viene visualizzato il contenuto di htmlview.</span><span class="sxs-lookup"><span data-stu-id="5dba8-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="5dba8-123">In caso contrario, Windows Media Player chiede all'utente l'autorizzazione per visualizzare il contenuto di HTMLView.</span><span class="sxs-lookup"><span data-stu-id="5dba8-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="5dba8-124">Ad esempio, se l'URL per la pagina Web HTMLView è https://www.proseware.com/html/HTMLView.htm e l'URL per l'attributo **BaseUrl** è specificato come https://www.proseware.com , viene visualizzata la pagina Web HtmlView senza richiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="5dba8-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dba8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5dba8-125">Requirements</span></span>



| <span data-ttu-id="5dba8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dba8-126">Requirement</span></span> | <span data-ttu-id="5dba8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5dba8-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="5dba8-128">Versione</span><span class="sxs-lookup"><span data-stu-id="5dba8-128">Version</span></span><br/> | <span data-ttu-id="5dba8-129">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5dba8-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5dba8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5dba8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dba8-131">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="5dba8-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="5dba8-132">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5dba8-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5dba8-133">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="5dba8-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5dba8-134">**PARAM (elemento)**</span><span class="sxs-lookup"><span data-stu-id="5dba8-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="5dba8-135">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5dba8-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






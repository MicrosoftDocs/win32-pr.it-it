---
title: Navigate-elemento
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento Navigate specifica un URL usato dalle chiamate a External. NavigateTaskPaneURL.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Esplora finestre elementi Media Player
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328117"
---
# <a name="navigate-element"></a><span data-ttu-id="09965-106">Navigate-elemento</span><span class="sxs-lookup"><span data-stu-id="09965-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="09965-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="09965-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="09965-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09965-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="09965-109">L'elemento **Navigate** specifica un URL usato dalle chiamate a **External. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="09965-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="09965-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="09965-110">Attributes</span></span>



| <span data-ttu-id="09965-111">Termine</span><span class="sxs-lookup"><span data-stu-id="09965-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="09965-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09965-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09965-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseUrl** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="09965-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="09965-114">URL completo per la pagina Web in cui spostarsi.</span><span class="sxs-lookup"><span data-stu-id="09965-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="09965-115">**NavigateTaskPaneURL** può aggiungere una stringa di query a questo URL.</span><span class="sxs-lookup"><span data-stu-id="09965-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="09965-116">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="09965-116">Parent/Child Elements</span></span>



| <span data-ttu-id="09965-117">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="09965-117">Hierarchy</span></span>       | <span data-ttu-id="09965-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="09965-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="09965-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="09965-119">Parent elements</span></span> | <span data-ttu-id="09965-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="09965-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="09965-121">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="09965-121">Child elements</span></span>  | <span data-ttu-id="09965-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="09965-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="09965-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09965-123">Requirements</span></span>



| <span data-ttu-id="09965-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="09965-124">Requirement</span></span> | <span data-ttu-id="09965-125">Valore</span><span class="sxs-lookup"><span data-stu-id="09965-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="09965-126">Versione</span><span class="sxs-lookup"><span data-stu-id="09965-126">Version</span></span><br/> | <span data-ttu-id="09965-127">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="09965-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09965-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09965-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09965-129">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="09965-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="09965-130">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="09965-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="09965-131">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="09965-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="09965-132">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="09965-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






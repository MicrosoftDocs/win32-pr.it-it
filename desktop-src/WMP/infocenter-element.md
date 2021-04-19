---
title: Elemento centro informazioni
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento centro informazioni
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Finestra degli elementi del centro informazioni Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325447"
---
# <a name="infocenter-element"></a><span data-ttu-id="76751-105">Elemento centro informazioni</span><span class="sxs-lookup"><span data-stu-id="76751-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="76751-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="76751-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="76751-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="76751-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="76751-108">L' **elemento centro** informazioni consente di specificare l'URL della pagina Web visualizzata da Windows Media Player nella funzionalità di visualizzazione del centro informazioni per la **riproduzione** quando lo Store online è attivo.</span><span class="sxs-lookup"><span data-stu-id="76751-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="76751-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="76751-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="76751-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="76751-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="76751-111">URL per la pagina Web visualizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="76751-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="76751-112">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="76751-112">Parent/Child Elements</span></span>



| <span data-ttu-id="76751-113">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="76751-113">Hierarchy</span></span>       | <span data-ttu-id="76751-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="76751-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="76751-115">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="76751-115">Parent elements</span></span> | <span data-ttu-id="76751-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="76751-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="76751-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="76751-117">Child elements</span></span>  | <span data-ttu-id="76751-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="76751-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="76751-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="76751-119">Remarks</span></span>

<span data-ttu-id="76751-120">L'utente controlla quando la visualizzazione Info Center è attiva.</span><span class="sxs-lookup"><span data-stu-id="76751-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="76751-121">Per recuperare informazioni sull'elemento multimediale attualmente in riproduzione, è necessario incorporare un'istanza di Windows Media Player Control nella pagina Web e utilizzare il modello a oggetti del lettore.</span><span class="sxs-lookup"><span data-stu-id="76751-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="76751-122">La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.</span><span class="sxs-lookup"><span data-stu-id="76751-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="76751-123">Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="76751-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="76751-124">Nome</span><span class="sxs-lookup"><span data-stu-id="76751-124">Name</span></span>         | <span data-ttu-id="76751-125">Valore</span><span class="sxs-lookup"><span data-stu-id="76751-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76751-126">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="76751-126">*geoid*</span></span>      | <span data-ttu-id="76751-127">ID della posizione geografica di Windows.</span><span class="sxs-lookup"><span data-stu-id="76751-127">Windows geographical location ID.</span></span> <span data-ttu-id="76751-128">L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="76751-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="76751-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="76751-129">*locale*</span></span>     | <span data-ttu-id="76751-130">Windows Media Player ID impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="76751-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="76751-131">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="76751-131">*userlocale*</span></span> | <span data-ttu-id="76751-132">ID delle impostazioni locali di Windows.</span><span class="sxs-lookup"><span data-stu-id="76751-132">Windows locale ID.</span></span> <span data-ttu-id="76751-133">Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="76751-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="76751-134">*version*</span><span class="sxs-lookup"><span data-stu-id="76751-134">*version*</span></span>    | <span data-ttu-id="76751-135">Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="76751-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="76751-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76751-136">Requirements</span></span>



| <span data-ttu-id="76751-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="76751-137">Requirement</span></span> | <span data-ttu-id="76751-138">Valore</span><span class="sxs-lookup"><span data-stu-id="76751-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="76751-139">Versione</span><span class="sxs-lookup"><span data-stu-id="76751-139">Version</span></span><br/> | <span data-ttu-id="76751-140">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="76751-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76751-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76751-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76751-142">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="76751-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="76751-143">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="76751-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="76751-144">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="76751-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






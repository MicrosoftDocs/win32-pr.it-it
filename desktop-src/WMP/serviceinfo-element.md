---
title: Elemento ServiceInfo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento ServiceInfo è l'elemento principale per il documento ServiceInfo.xml.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Finestra elementi ServiceInfo Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328112"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="e103c-106">Elemento ServiceInfo</span><span class="sxs-lookup"><span data-stu-id="e103c-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="e103c-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="e103c-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e103c-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e103c-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e103c-109">L'elemento **ServiceInfo** è l'elemento principale per il documento ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="e103c-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="e103c-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="e103c-110">Attributes</span></span>



| <span data-ttu-id="e103c-111">Termine</span><span class="sxs-lookup"><span data-stu-id="e103c-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="e103c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e103c-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e103c-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versione** (facoltativa)</span><span class="sxs-lookup"><span data-stu-id="e103c-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="e103c-114">Versione del file di ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="e103c-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="e103c-115">La versione 1,00 è supportata per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e103c-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="e103c-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Chiave** (obbligatoria)</span><span class="sxs-lookup"><span data-stu-id="e103c-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="e103c-117">Stringa della chiave del servizio che identifica in modo univoco l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="e103c-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="e103c-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span><span class="sxs-lookup"><span data-stu-id="e103c-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="e103c-119">Indica se l'archivio online è un archivio di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="e103c-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="e103c-120">Il valore "true" indica che l'archivio è di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="e103c-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="e103c-121">Il valore "false" indica che l'archivio non è un archivio di tipo 1; ovvero, è un archivio di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="e103c-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="e103c-122">Il valore predefinito è "false".</span><span class="sxs-lookup"><span data-stu-id="e103c-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="e103c-123">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="e103c-123">Parent/Child Elements</span></span>



| <span data-ttu-id="e103c-124">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="e103c-124">Hierarchy</span></span>       | <span data-ttu-id="e103c-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="e103c-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e103c-126">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e103c-126">Parent elements</span></span> | <span data-ttu-id="e103c-127">nessuno</span><span class="sxs-lookup"><span data-stu-id="e103c-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="e103c-128">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e103c-128">Child elements</span></span>  | <span data-ttu-id="e103c-129">**AlbumInfo**, **BuyCD**, **color**, **Description**, **FriendlyName**, **HtmlView**, **Image**, **centro** informazioni, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="e103c-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e103c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e103c-130">Remarks</span></span>

<span data-ttu-id="e103c-131">La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.</span><span class="sxs-lookup"><span data-stu-id="e103c-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="e103c-132">Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e103c-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="e103c-133">La richiesta includerà anche tutti i parametri specificati usando il parametro della riga di comando ServiceExtra del programma di installazione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e103c-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="e103c-134">Nome</span><span class="sxs-lookup"><span data-stu-id="e103c-134">Name</span></span>         | <span data-ttu-id="e103c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e103c-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e103c-136">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="e103c-136">*geoid*</span></span>      | <span data-ttu-id="e103c-137">ID della posizione geografica di Windows.</span><span class="sxs-lookup"><span data-stu-id="e103c-137">Windows geographical location ID.</span></span> <span data-ttu-id="e103c-138">L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="e103c-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="e103c-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="e103c-139">*locale*</span></span>     | <span data-ttu-id="e103c-140">Windows Media Player ID impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="e103c-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="e103c-141">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="e103c-141">*userlocale*</span></span> | <span data-ttu-id="e103c-142">ID delle impostazioni locali di Windows.</span><span class="sxs-lookup"><span data-stu-id="e103c-142">Windows locale ID.</span></span> <span data-ttu-id="e103c-143">Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="e103c-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="e103c-144">*version*</span><span class="sxs-lookup"><span data-stu-id="e103c-144">*version*</span></span>    | <span data-ttu-id="e103c-145">Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="e103c-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="e103c-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e103c-146">Requirements</span></span>



| <span data-ttu-id="e103c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e103c-147">Requirement</span></span> | <span data-ttu-id="e103c-148">Valore</span><span class="sxs-lookup"><span data-stu-id="e103c-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="e103c-149">Versione</span><span class="sxs-lookup"><span data-stu-id="e103c-149">Version</span></span><br/> | <span data-ttu-id="e103c-150">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e103c-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e103c-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e103c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e103c-152">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e103c-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e103c-153">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="e103c-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e103c-154">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e103c-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






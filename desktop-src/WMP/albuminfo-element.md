---
title: Elemento AlbumInfo
description: L'elemento AlbumInfo specifica l'URL per la pagina Web visualizzata da Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Finestra elementi AlbumInfo Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328726"
---
# <a name="albuminfo-element"></a><span data-ttu-id="a809d-104">Elemento AlbumInfo</span><span class="sxs-lookup"><span data-stu-id="a809d-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="a809d-105">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="a809d-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a809d-106">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a809d-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a809d-107">L'elemento **AlbumInfo** specifica l'URL per la pagina Web visualizzata da Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a809d-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="a809d-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="a809d-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="a809d-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="a809d-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="a809d-110">URL per la pagina Web visualizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a809d-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="a809d-111">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="a809d-111">Parent/Child Elements</span></span>



| <span data-ttu-id="a809d-112">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="a809d-112">Hierarchy</span></span>       | <span data-ttu-id="a809d-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="a809d-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="a809d-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a809d-114">Parent elements</span></span> | <span data-ttu-id="a809d-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a809d-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="a809d-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a809d-116">Child elements</span></span>  | <span data-ttu-id="a809d-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="a809d-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="a809d-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a809d-118">Remarks</span></span>

<span data-ttu-id="a809d-119">Quando l'utente fa clic su un pulsante di Windows Media Player per visualizzare informazioni aggiuntive su un particolare elemento multimediale, il lettore Invia la richiesta URL con i parametri allegati usando un separatore di stringa di query punto interrogativo (?).</span><span class="sxs-lookup"><span data-stu-id="a809d-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="a809d-120">La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.</span><span class="sxs-lookup"><span data-stu-id="a809d-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="a809d-121">Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="a809d-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="a809d-122">Nome</span><span class="sxs-lookup"><span data-stu-id="a809d-122">Name</span></span>         | <span data-ttu-id="a809d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a809d-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a809d-124">*Album*</span><span class="sxs-lookup"><span data-stu-id="a809d-124">*Album*</span></span>      | <span data-ttu-id="a809d-125">Valore dell'attributo **WM/AlbumTitle** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a809d-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="a809d-126">*Artista*</span><span class="sxs-lookup"><span data-stu-id="a809d-126">*Artist*</span></span>     | <span data-ttu-id="a809d-127">Valore dell'attributo **WM/AlbumArtist** , se esistente, o in caso contrario, il valore dell'attributo **Author** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a809d-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="a809d-128">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="a809d-128">*geoid*</span></span>      | <span data-ttu-id="a809d-129">ID della posizione geografica di Windows.</span><span class="sxs-lookup"><span data-stu-id="a809d-129">Windows geographical location ID.</span></span> <span data-ttu-id="a809d-130">L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="a809d-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="a809d-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="a809d-131">*locale*</span></span>     | <span data-ttu-id="a809d-132">Windows Media Player ID impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="a809d-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="a809d-133">*Title*</span><span class="sxs-lookup"><span data-stu-id="a809d-133">*Title*</span></span>      | <span data-ttu-id="a809d-134">Valore dell'attributo **title** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a809d-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="a809d-135">*UFID*</span><span class="sxs-lookup"><span data-stu-id="a809d-135">*UFID*</span></span>       | <span data-ttu-id="a809d-136">Valore dell'attributo **WM/UniqueFileIdentifier** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a809d-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="a809d-137">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="a809d-137">*userlocale*</span></span> | <span data-ttu-id="a809d-138">ID delle impostazioni locali di Windows.</span><span class="sxs-lookup"><span data-stu-id="a809d-138">Windows locale ID.</span></span> <span data-ttu-id="a809d-139">Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="a809d-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="a809d-140">*version*</span><span class="sxs-lookup"><span data-stu-id="a809d-140">*version*</span></span>    | <span data-ttu-id="a809d-141">Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="a809d-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a809d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a809d-142">Requirements</span></span>



| <span data-ttu-id="a809d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a809d-143">Requirement</span></span> | <span data-ttu-id="a809d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="a809d-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="a809d-145">Versione</span><span class="sxs-lookup"><span data-stu-id="a809d-145">Version</span></span><br/> | <span data-ttu-id="a809d-146">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a809d-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a809d-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a809d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a809d-148">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="a809d-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="a809d-149">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="a809d-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="a809d-150">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a809d-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






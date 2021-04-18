---
title: Elemento BuyCD
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Finestra elementi BuyCD Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327625"
---
# <a name="buycd-element"></a><span data-ttu-id="29eb1-105">Elemento BuyCD</span><span class="sxs-lookup"><span data-stu-id="29eb1-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="29eb1-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="29eb1-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="29eb1-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="29eb1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="29eb1-108">L'elemento **BuyCD** specifica gli URL per le pagine Web visualizzate da Windows Media Player quando l'utente sceglie di effettuare un acquisto.</span><span class="sxs-lookup"><span data-stu-id="29eb1-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="29eb1-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="29eb1-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="29eb1-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="29eb1-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="29eb1-111">URL per la pagina Web visualizzata dal negozio online per offrire un CD o un DVD da acquistare in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="29eb1-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="29eb1-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span><span class="sxs-lookup"><span data-stu-id="29eb1-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="29eb1-113">URL per la pagina Web visualizzata nel negozio online per offrire un CD o DVD da acquistare in Windows XP Media Center Edition 2004 Update.</span><span class="sxs-lookup"><span data-stu-id="29eb1-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="29eb1-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span><span class="sxs-lookup"><span data-stu-id="29eb1-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="29eb1-115">URL per la pagina Web visualizzata dal negozio online per offrire un CD o un DVD da acquistare in una finestra del browser separata.</span><span class="sxs-lookup"><span data-stu-id="29eb1-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="29eb1-116">Questo URL viene usato anche da Windows XP Service Pack 2 o versione successiva per la funzionalità **Shop for Music online** .</span><span class="sxs-lookup"><span data-stu-id="29eb1-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="29eb1-117">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="29eb1-117">Parent/Child Elements</span></span>



| <span data-ttu-id="29eb1-118">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="29eb1-118">Hierarchy</span></span>       | <span data-ttu-id="29eb1-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="29eb1-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="29eb1-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="29eb1-120">Parent elements</span></span> | <span data-ttu-id="29eb1-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="29eb1-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="29eb1-122">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="29eb1-122">Child elements</span></span>  | <span data-ttu-id="29eb1-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="29eb1-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="29eb1-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="29eb1-124">Remarks</span></span>

<span data-ttu-id="29eb1-125">Quando l'utente fa clic su un pulsante o un collegamento in Windows Media Player per acquistare un CD o un DVD, il lettore Invia la richiesta URL a ServiceTask1 con i parametri allegati usando un separatore di stringa di query punto interrogativo (?).</span><span class="sxs-lookup"><span data-stu-id="29eb1-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="29eb1-126">La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.</span><span class="sxs-lookup"><span data-stu-id="29eb1-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="29eb1-127">Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="29eb1-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="29eb1-128">Nome</span><span class="sxs-lookup"><span data-stu-id="29eb1-128">Name</span></span>         | <span data-ttu-id="29eb1-129">Valore</span><span class="sxs-lookup"><span data-stu-id="29eb1-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29eb1-130">*Album*</span><span class="sxs-lookup"><span data-stu-id="29eb1-130">*Album*</span></span>      | <span data-ttu-id="29eb1-131">Valore dell'attributo **WM/AlbumTitle** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="29eb1-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="29eb1-132">*Artista*</span><span class="sxs-lookup"><span data-stu-id="29eb1-132">*Artist*</span></span>     | <span data-ttu-id="29eb1-133">Valore dell'attributo **WM/AlbumArtist** , se esistente, o in caso contrario, il valore dell'attributo **Author** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="29eb1-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="29eb1-134">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="29eb1-134">*geoid*</span></span>      | <span data-ttu-id="29eb1-135">ID della posizione geografica di Windows.</span><span class="sxs-lookup"><span data-stu-id="29eb1-135">Windows geographical location ID.</span></span> <span data-ttu-id="29eb1-136">L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="29eb1-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="29eb1-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="29eb1-137">*locale*</span></span>     | <span data-ttu-id="29eb1-138">Windows Media Player ID impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="29eb1-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="29eb1-139">*Title*</span><span class="sxs-lookup"><span data-stu-id="29eb1-139">*Title*</span></span>      | <span data-ttu-id="29eb1-140">Valore dell'attributo **title** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="29eb1-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="29eb1-141">*UFID*</span><span class="sxs-lookup"><span data-stu-id="29eb1-141">*UFID*</span></span>       | <span data-ttu-id="29eb1-142">Valore dell'attributo **WM/UniqueFileIdentifier** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="29eb1-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="29eb1-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="29eb1-143">*userlocale*</span></span> | <span data-ttu-id="29eb1-144">ID delle impostazioni locali di Windows.</span><span class="sxs-lookup"><span data-stu-id="29eb1-144">Windows locale ID.</span></span> <span data-ttu-id="29eb1-145">Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="29eb1-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="29eb1-146">*version*</span><span class="sxs-lookup"><span data-stu-id="29eb1-146">*version*</span></span>    | <span data-ttu-id="29eb1-147">Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="29eb1-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="29eb1-148">Windows XP Media Center Edition 2004 fornisce agli utenti un'interfaccia utente progettata per essere visualizzata a distanza.</span><span class="sxs-lookup"><span data-stu-id="29eb1-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="29eb1-149">È necessario creare pagine Web per il parametro *MediaCenterURL* da visualizzare su schermi di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="29eb1-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="29eb1-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29eb1-150">Requirements</span></span>



| <span data-ttu-id="29eb1-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="29eb1-151">Requirement</span></span> | <span data-ttu-id="29eb1-152">Valore</span><span class="sxs-lookup"><span data-stu-id="29eb1-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="29eb1-153">Versione</span><span class="sxs-lookup"><span data-stu-id="29eb1-153">Version</span></span><br/> | <span data-ttu-id="29eb1-154">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="29eb1-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29eb1-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29eb1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29eb1-156">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="29eb1-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="29eb1-157">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="29eb1-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="29eb1-158">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="29eb1-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






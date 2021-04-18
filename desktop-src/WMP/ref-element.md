---
title: REF-elemento
description: L'elemento REF specifica un URL per il contenuto multimediale digitale.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Media Player di Windows per elementi REF
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327288"
---
# <a name="ref-element"></a><span data-ttu-id="02168-104">REF-elemento</span><span class="sxs-lookup"><span data-stu-id="02168-104">REF Element</span></span>

<span data-ttu-id="02168-105">L'elemento **ref** specifica un URL per il contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="02168-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="02168-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="02168-106">Attributes</span></span>

<span data-ttu-id="02168-107">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="02168-107">**HREF** (required)</span></span>

<span data-ttu-id="02168-108">URL di qualsiasi contenuto multimediale supportato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02168-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="02168-109">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="02168-109">Parent/Child Elements</span></span>



| <span data-ttu-id="02168-110">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="02168-110">Hierarchy</span></span>       | <span data-ttu-id="02168-111">Elementi</span><span class="sxs-lookup"><span data-stu-id="02168-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="02168-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="02168-112">Parent elements</span></span> | <span data-ttu-id="02168-113">**VOCE**</span><span class="sxs-lookup"><span data-stu-id="02168-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="02168-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="02168-114">Child elements</span></span>  | <span data-ttu-id="02168-115">**Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime**</span><span class="sxs-lookup"><span data-stu-id="02168-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="02168-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="02168-116">Remarks</span></span>

<span data-ttu-id="02168-117">Questo elemento specifica un URL per una porzione di contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="02168-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="02168-118">L'URL può puntare a qualsiasi tipo di supporto supportato, usando qualsiasi protocollo supportato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02168-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="02168-119">I tipi di supporto supportati includono immagini ancora come le immagini. gif e. jpg e i file Flash con estensione di file SWF.</span><span class="sxs-lookup"><span data-stu-id="02168-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="02168-120">Questi tipi di supporti sono utili per includere contenuti pubblicitari all'interno di una playlist.</span><span class="sxs-lookup"><span data-stu-id="02168-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="02168-121">Con i file di immagine e i file Flash che rientrano in un ciclo, è inoltre necessario specificare la quantità di tempo per la visualizzazione dell'elemento multimediale includendo un elemento **Duration** all'interno dell'elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="02168-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="02168-122">Se si vuole che un'immagine continui a essere visualizzata mentre la voce successiva nella playlist è memorizzata nel buffer, includere un elemento **param** nell'elemento **entry** , impostare il relativo attributo **Name** su ShowWhileBuffering e impostare il relativo attributo **value** su true.</span><span class="sxs-lookup"><span data-stu-id="02168-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="02168-123">Per fare riferimento al contenuto di un CD o di un DVD che lo consente, vengono forniti i protocolli wmpcd e wmpdvd.</span><span class="sxs-lookup"><span data-stu-id="02168-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="02168-124">Se ad esempio si imposta l'attributo **href** su "wmpdvd://f/5/3", il capitolo 3 del titolo 5 verrà riprodotto in un DVD, ma solo se il DVD è stato creato per consentirlo.</span><span class="sxs-lookup"><span data-stu-id="02168-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="02168-125">Le applicazioni che aprono supporti digitali da dietro un firewall avranno prestazioni migliori quando si aprono gli elementi multimediali se l'indirizzo viene specificato usando il nome del Domain Name Server (DNS) invece dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="02168-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="02168-126">L'uso più comune di questo elemento è per il rollover degli URL.</span><span class="sxs-lookup"><span data-stu-id="02168-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="02168-127">Se Windows Media Player non è in grado di aprire un elemento multimediale definito in un elemento **ref** , tenta l'URL nell'elemento **ref** successivo.</span><span class="sxs-lookup"><span data-stu-id="02168-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="02168-128">Quando Windows Media Player apre contenuto multimediale da un URL definito nell'ambito di un elemento **entry** , ignora i tag **ref** successivi all'interno dell'elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="02168-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="02168-129">Una volta completata la riproduzione del contenuto, Windows Media Player si sposta sull'elemento **entry** successivo, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="02168-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="02168-130">**Importante** Una volta che Windows Media Player stabilisce una connessione a una parte di contenuto a cui si fa riferimento, ignora tutti gli altri elementi **ref** in tale **voce**, indipendentemente dal fatto che la connessione termini normalmente o in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="02168-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="02168-131">Se l'elemento multimediale a cui si fa riferimento è un file di immagine, è necessario usare l'elemento **Duration** per specificare l'ora di visualizzazione per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="02168-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="02168-132">**Nota**</span><span class="sxs-lookup"><span data-stu-id="02168-132">**Note**</span></span>

<span data-ttu-id="02168-133">Il tentativo di riprodurre supporti flash che includono suoni con il primo frame può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="02168-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="02168-134">È necessario creare il contenuto Flash per riprodurre un suono che inizia senza precedenti rispetto al secondo frame.</span><span class="sxs-lookup"><span data-stu-id="02168-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="02168-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="02168-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="02168-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02168-136">Requirements</span></span>



| <span data-ttu-id="02168-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="02168-137">Requirement</span></span> | <span data-ttu-id="02168-138">Valore</span><span class="sxs-lookup"><span data-stu-id="02168-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="02168-139">Versione</span><span class="sxs-lookup"><span data-stu-id="02168-139">Version</span></span><br/> | <span data-ttu-id="02168-140">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="02168-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02168-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02168-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02168-142">**Protocolli e tipi di file supportati**</span><span class="sxs-lookup"><span data-stu-id="02168-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="02168-143">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="02168-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="02168-144">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="02168-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






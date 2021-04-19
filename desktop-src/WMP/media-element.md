---
title: Elemento multimediale
description: L'elemento media specifica uno degli elementi multimediali in una playlist.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento multimediale Media Player Windows
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323911"
---
# <a name="media-element"></a><span data-ttu-id="56855-104">Elemento multimediale</span><span class="sxs-lookup"><span data-stu-id="56855-104">media Element</span></span>

<span data-ttu-id="56855-105">L'elemento **media** specifica uno degli elementi multimediali in una playlist.</span><span class="sxs-lookup"><span data-stu-id="56855-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="56855-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="56855-106">Attributes</span></span>



| <span data-ttu-id="56855-107">Termine</span><span class="sxs-lookup"><span data-stu-id="56855-107">Term</span></span>                                                                                                                       | <span data-ttu-id="56855-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56855-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56855-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="56855-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="56855-110">URL di un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="56855-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="56855-111"><span id="cid"></span><span id="CID"></span>**CID**</span><span class="sxs-lookup"><span data-stu-id="56855-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="56855-112">ID contenuto univoco per questo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="56855-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="56855-113"><span id="tid"></span><span id="TID"></span>**TID**</span><span class="sxs-lookup"><span data-stu-id="56855-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="56855-114">ID di traccia che può essere utilizzato per tenere traccia dell'oggetto file System per questo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="56855-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="56855-115">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="56855-115">Parent/Child Elements</span></span>



| <span data-ttu-id="56855-116">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="56855-116">Hierarchy</span></span> | <span data-ttu-id="56855-117">Elementi</span><span class="sxs-lookup"><span data-stu-id="56855-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="56855-118">Padre</span><span class="sxs-lookup"><span data-stu-id="56855-118">Parent</span></span>    | [<span data-ttu-id="56855-119">Seq</span><span class="sxs-lookup"><span data-stu-id="56855-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="56855-120">Figlio</span><span class="sxs-lookup"><span data-stu-id="56855-120">Child</span></span>     | <span data-ttu-id="56855-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="56855-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="56855-122">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="56855-122">Remarks</span></span>

<span data-ttu-id="56855-123">L'attributo **CID** (ID contenuto) viene popolato da Windows Media Player come un modo per identificare in modo univoco una porzione di contenuto multimediale anche se gli attributi dei metadati sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="56855-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="56855-124">Questo consente la condivisione delle playlist tra i computer, perché il contenuto può essere identificato in un altro computer e il percorso può essere "riparato automaticamente" dalla playlist di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="56855-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="56855-125">L'attributo **TID** (ID di traccia) usa il file System Windows per ripristinare automaticamente il percorso del supporto se il nome o il percorso del file viene modificato.</span><span class="sxs-lookup"><span data-stu-id="56855-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="56855-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="56855-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="56855-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56855-127">Requirements</span></span>



| <span data-ttu-id="56855-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="56855-128">Requirement</span></span> | <span data-ttu-id="56855-129">Valore</span><span class="sxs-lookup"><span data-stu-id="56855-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="56855-130">Versione</span><span class="sxs-lookup"><span data-stu-id="56855-130">Version</span></span><br/> | <span data-ttu-id="56855-131">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="56855-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56855-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56855-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56855-133">**Elemento seq**</span><span class="sxs-lookup"><span data-stu-id="56855-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="56855-134">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="56855-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






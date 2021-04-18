---
title: Elemento meta
description: L'elemento meta specifica i metadati che si applicano all'intera playlist.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- meta-elemento Media Player Windows
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327149"
---
# <a name="meta-element"></a><span data-ttu-id="6748d-104">Elemento meta</span><span class="sxs-lookup"><span data-stu-id="6748d-104">meta Element</span></span>

<span data-ttu-id="6748d-105">L'elemento **meta** specifica i metadati che si applicano all'intera playlist.</span><span class="sxs-lookup"><span data-stu-id="6748d-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="6748d-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="6748d-106">Attributes</span></span>



| <span data-ttu-id="6748d-107">Termine</span><span class="sxs-lookup"><span data-stu-id="6748d-107">Term</span></span>                                                                       | <span data-ttu-id="6748d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6748d-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6748d-109"><span id="name"></span><span id="NAME"></span>**nome**</span><span class="sxs-lookup"><span data-stu-id="6748d-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="6748d-110">Nome di un elemento di metadati.</span><span class="sxs-lookup"><span data-stu-id="6748d-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="6748d-111"><span id="content"></span><span id="CONTENT"></span>**contenuto**</span><span class="sxs-lookup"><span data-stu-id="6748d-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="6748d-112">Valore di un elemento di metadati.</span><span class="sxs-lookup"><span data-stu-id="6748d-112">The value of an item of metadata.</span></span> <span data-ttu-id="6748d-113">Ad esempio, se l'attributo del nome è "genre", l'attributo di contenuto potrebbe essere "Rock".</span><span class="sxs-lookup"><span data-stu-id="6748d-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6748d-114">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="6748d-114">Parent/Child Elements</span></span>



| <span data-ttu-id="6748d-115">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="6748d-115">Hierarchy</span></span> | <span data-ttu-id="6748d-116">Elementi</span><span class="sxs-lookup"><span data-stu-id="6748d-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="6748d-117">Padre</span><span class="sxs-lookup"><span data-stu-id="6748d-117">Parent</span></span>    | [<span data-ttu-id="6748d-118">Head</span><span class="sxs-lookup"><span data-stu-id="6748d-118">head</span></span>](head-element.md) |
| <span data-ttu-id="6748d-119">Figlio</span><span class="sxs-lookup"><span data-stu-id="6748d-119">Child</span></span>     | <span data-ttu-id="6748d-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="6748d-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="6748d-121">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6748d-121">Remarks</span></span>

<span data-ttu-id="6748d-122">L'autore di una playlist di Windows Media può impostare l'attributo Name di un metaelemento su qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="6748d-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="6748d-123">Nell'elenco seguente vengono illustrati alcuni attributi di nome tipici presenti nelle playlist di Windows Media create da Windows Media Player e altri componenti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6748d-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="6748d-124">Autore</span><span class="sxs-lookup"><span data-stu-id="6748d-124">Author</span></span>
-   <span data-ttu-id="6748d-125">Category</span><span class="sxs-lookup"><span data-stu-id="6748d-125">Category</span></span>
-   <span data-ttu-id="6748d-126">Genre</span><span class="sxs-lookup"><span data-stu-id="6748d-126">Genre</span></span>
-   <span data-ttu-id="6748d-127">UserName</span><span class="sxs-lookup"><span data-stu-id="6748d-127">UserName</span></span>
-   <span data-ttu-id="6748d-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="6748d-128">UserRating</span></span>
-   <span data-ttu-id="6748d-129">Generator</span><span class="sxs-lookup"><span data-stu-id="6748d-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="6748d-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="6748d-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="6748d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6748d-131">Requirements</span></span>



| <span data-ttu-id="6748d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6748d-132">Requirement</span></span> | <span data-ttu-id="6748d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6748d-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="6748d-134">Versione</span><span class="sxs-lookup"><span data-stu-id="6748d-134">Version</span></span><br/> | <span data-ttu-id="6748d-135">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6748d-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6748d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6748d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6748d-137">**Elemento Head**</span><span class="sxs-lookup"><span data-stu-id="6748d-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="6748d-138">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6748d-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






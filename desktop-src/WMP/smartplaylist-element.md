---
title: Elemento smartPlaylist
description: L'elemento smartPlaylist contiene la parte definita dinamicamente di una playlist.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Finestra elementi smartPlaylist Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331744"
---
# <a name="smartplaylist-element"></a><span data-ttu-id="6af70-104">Elemento smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="6af70-104">smartPlaylist Element</span></span>

<span data-ttu-id="6af70-105">L'elemento **smartPlaylist** contiene la parte definita dinamicamente di una playlist.</span><span class="sxs-lookup"><span data-stu-id="6af70-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="6af70-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="6af70-106">Attributes</span></span>



| <span data-ttu-id="6af70-107">Termine</span><span class="sxs-lookup"><span data-stu-id="6af70-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="6af70-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6af70-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af70-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**versione** (obbligatoria)</span><span class="sxs-lookup"><span data-stu-id="6af70-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="6af70-110">Numero decimale che rappresenta il numero di versione dello schema della playlist intelligente.</span><span class="sxs-lookup"><span data-stu-id="6af70-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="6af70-111">Impostare su 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="6af70-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6af70-112">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="6af70-112">Parent/Child Elements</span></span>



| <span data-ttu-id="6af70-113">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="6af70-113">Hierarchy</span></span> | <span data-ttu-id="6af70-114">Elementi</span><span class="sxs-lookup"><span data-stu-id="6af70-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="6af70-115">Padre</span><span class="sxs-lookup"><span data-stu-id="6af70-115">Parent</span></span>    | [<span data-ttu-id="6af70-116">Seq</span><span class="sxs-lookup"><span data-stu-id="6af70-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="6af70-117">Figlio</span><span class="sxs-lookup"><span data-stu-id="6af70-117">Child</span></span>     | <span data-ttu-id="6af70-118">[querySet](queryset-element.md), [filtro](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="6af70-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6af70-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6af70-119">Remarks</span></span>

<span data-ttu-id="6af70-120">Un elemento **smartPlaylist** contiene in genere un elemento **querySet** e può contenere anche un elemento **Filter** .</span><span class="sxs-lookup"><span data-stu-id="6af70-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="6af70-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="6af70-121">Examples</span></span>


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a><span data-ttu-id="6af70-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6af70-122">Requirements</span></span>



| <span data-ttu-id="6af70-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af70-123">Requirement</span></span> | <span data-ttu-id="6af70-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6af70-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="6af70-125">Versione</span><span class="sxs-lookup"><span data-stu-id="6af70-125">Version</span></span><br/> | <span data-ttu-id="6af70-126">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6af70-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6af70-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6af70-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af70-128">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="6af70-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="6af70-129">**Filter-elemento**</span><span class="sxs-lookup"><span data-stu-id="6af70-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="6af70-130">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="6af70-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="6af70-131">**Elemento querySet**</span><span class="sxs-lookup"><span data-stu-id="6af70-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="6af70-132">**Elemento seq**</span><span class="sxs-lookup"><span data-stu-id="6af70-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="6af70-133">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6af70-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






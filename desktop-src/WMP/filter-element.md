---
title: Filter-elemento
description: L'elemento Filter contiene elementi che limitano le dimensioni di una playlist, la durata di una playlist o il numero di elementi multimediali in una playlist.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- filtrare gli elementi di Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326726"
---
# <a name="filter-element"></a><span data-ttu-id="448f6-104">Filter-elemento</span><span class="sxs-lookup"><span data-stu-id="448f6-104">filter Element</span></span>

<span data-ttu-id="448f6-105">L'elemento **Filter** contiene elementi che limitano le dimensioni di una playlist, la durata di una playlist o il numero di elementi multimediali in una playlist.</span><span class="sxs-lookup"><span data-stu-id="448f6-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="448f6-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="448f6-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="448f6-107"><span id="type"></span><span id="TYPE"></span>**tipo**</span><span class="sxs-lookup"><span data-stu-id="448f6-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="448f6-108">Tipo di oggetto filtro.</span><span class="sxs-lookup"><span data-stu-id="448f6-108">The type of filter object.</span></span> <span data-ttu-id="448f6-109">Nessun valore predefinito per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="448f6-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="448f6-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="448f6-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="448f6-111">GUID che identifica in modo univoco un oggetto filtro.</span><span class="sxs-lookup"><span data-stu-id="448f6-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="448f6-112">I metodi dell'oggetto filtro vengono richiamati per interpretare gli elementi del **frammento** contenuti nell'elemento **filtro** .</span><span class="sxs-lookup"><span data-stu-id="448f6-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="448f6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="448f6-113">Value</span></span>                                  | <span data-ttu-id="448f6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="448f6-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="448f6-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="448f6-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="448f6-116">ID per il filtro "Microsoft auto playlist Filter-limita le playlist automatiche per conteggio, dimensioni o durata".</span><span class="sxs-lookup"><span data-stu-id="448f6-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="448f6-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="448f6-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="448f6-118">Nome dell'oggetto filtro.</span><span class="sxs-lookup"><span data-stu-id="448f6-118">The name of the filter object.</span></span>



| <span data-ttu-id="448f6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="448f6-119">Value</span></span>                                                                              | <span data-ttu-id="448f6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="448f6-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="448f6-121">Filtro playlist automatico Microsoft: limita le playlist automatiche in base al conteggio, alle dimensioni o alla durata</span><span class="sxs-lookup"><span data-stu-id="448f6-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="448f6-122">Limita le playlist automatiche in base al conteggio, alle dimensioni o alla durata.</span><span class="sxs-lookup"><span data-stu-id="448f6-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="448f6-123">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="448f6-123">Parent/Child Elements</span></span>



| <span data-ttu-id="448f6-124">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="448f6-124">Hierarchy</span></span> | <span data-ttu-id="448f6-125">Elementi</span><span class="sxs-lookup"><span data-stu-id="448f6-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="448f6-126">Padre</span><span class="sxs-lookup"><span data-stu-id="448f6-126">Parent</span></span>    | [<span data-ttu-id="448f6-127">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="448f6-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="448f6-128">Figlio</span><span class="sxs-lookup"><span data-stu-id="448f6-128">Child</span></span>     | [<span data-ttu-id="448f6-129">frammento</span><span class="sxs-lookup"><span data-stu-id="448f6-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="448f6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="448f6-130">Remarks</span></span>

<span data-ttu-id="448f6-131">L'elemento **Filter** non aggiunge elementi multimediali a una playlist; rimuove o filtra semplicemente il contenuto selezionato dall'elemento **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="448f6-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="448f6-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="448f6-132">Examples</span></span>


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a><span data-ttu-id="448f6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="448f6-133">Requirements</span></span>



| <span data-ttu-id="448f6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="448f6-134">Requirement</span></span> | <span data-ttu-id="448f6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="448f6-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="448f6-136">Versione</span><span class="sxs-lookup"><span data-stu-id="448f6-136">Version</span></span><br/> | <span data-ttu-id="448f6-137">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="448f6-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="448f6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="448f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448f6-139">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="448f6-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="448f6-140">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="448f6-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="448f6-141">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="448f6-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="448f6-142">**Elemento sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="448f6-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="448f6-143">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="448f6-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






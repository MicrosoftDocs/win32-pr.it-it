---
title: Elemento sourceFilter
description: L'elemento sourceFilter contiene elementi che selezionano gli elementi di una raccolta.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Finestra elementi sourceFilter Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331740"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="19edc-104">Elemento sourceFilter</span><span class="sxs-lookup"><span data-stu-id="19edc-104">sourceFilter Element</span></span>

<span data-ttu-id="19edc-105">L'elemento **sourceFilter** contiene elementi che selezionano gli elementi di una raccolta.</span><span class="sxs-lookup"><span data-stu-id="19edc-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="19edc-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="19edc-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="19edc-107"><span id="type"></span><span id="TYPE"></span>**tipo**</span><span class="sxs-lookup"><span data-stu-id="19edc-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="19edc-108">Tipo di oggetto filtro.</span><span class="sxs-lookup"><span data-stu-id="19edc-108">The type of filter object.</span></span> <span data-ttu-id="19edc-109">Nessun valore predefinito per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="19edc-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="19edc-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="19edc-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="19edc-111">GUID che identifica in modo univoco l'oggetto filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="19edc-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="19edc-112">I metodi dell'oggetto filtro di origine vengono richiamati per interpretare gli elementi del **frammento** contenuti nell'elemento **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="19edc-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="19edc-113">Valore</span><span class="sxs-lookup"><span data-stu-id="19edc-113">Value</span></span>                                  | <span data-ttu-id="19edc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19edc-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="19edc-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span><span class="sxs-lookup"><span data-stu-id="19edc-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="19edc-116">GUID per il filtro di origine "musica nel catalogo personale".</span><span class="sxs-lookup"><span data-stu-id="19edc-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="19edc-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="19edc-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="19edc-118">GUID per il filtro di origine "video in My Library".</span><span class="sxs-lookup"><span data-stu-id="19edc-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="19edc-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="19edc-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="19edc-120">GUID per il filtro di origine "Pictures in My Library".</span><span class="sxs-lookup"><span data-stu-id="19edc-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="19edc-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="19edc-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="19edc-122">Il GUID per il filtro di origine "TV shows in My Library".</span><span class="sxs-lookup"><span data-stu-id="19edc-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="19edc-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="19edc-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="19edc-124">Nome dell'oggetto filtro.</span><span class="sxs-lookup"><span data-stu-id="19edc-124">The name of the filter object.</span></span>



| <span data-ttu-id="19edc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="19edc-125">Value</span></span>                  | <span data-ttu-id="19edc-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19edc-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19edc-127">Musica nella libreria</span><span class="sxs-lookup"><span data-stu-id="19edc-127">Music in my library</span></span>    | <span data-ttu-id="19edc-128">Oggetto filtro che seleziona gli elementi specificati dal set di elementi musicali nella libreria dell'utente.</span><span class="sxs-lookup"><span data-stu-id="19edc-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="19edc-129">Video nella libreria</span><span class="sxs-lookup"><span data-stu-id="19edc-129">Video in my library</span></span>    | <span data-ttu-id="19edc-130">Oggetto filtro che seleziona gli elementi specificati dal set di elementi video nella libreria dell'utente.</span><span class="sxs-lookup"><span data-stu-id="19edc-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="19edc-131">Immagini nella libreria</span><span class="sxs-lookup"><span data-stu-id="19edc-131">Pictures in my library</span></span> | <span data-ttu-id="19edc-132">Oggetto filtro che seleziona gli elementi specificati dal set di elementi della foto nella libreria dell'utente.</span><span class="sxs-lookup"><span data-stu-id="19edc-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="19edc-133">Programmi TV nella libreria</span><span class="sxs-lookup"><span data-stu-id="19edc-133">TV shows in my library</span></span> | <span data-ttu-id="19edc-134">Oggetto filtro che seleziona gli elementi specificati dal set di elementi TV nella libreria dell'utente.</span><span class="sxs-lookup"><span data-stu-id="19edc-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="19edc-135">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="19edc-135">Parent/Child Elements</span></span>



| <span data-ttu-id="19edc-136">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="19edc-136">Hierarchy</span></span> | <span data-ttu-id="19edc-137">Elementi</span><span class="sxs-lookup"><span data-stu-id="19edc-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="19edc-138">Padre</span><span class="sxs-lookup"><span data-stu-id="19edc-138">Parent</span></span>    | [<span data-ttu-id="19edc-139">querySet</span><span class="sxs-lookup"><span data-stu-id="19edc-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="19edc-140">Figlio</span><span class="sxs-lookup"><span data-stu-id="19edc-140">Child</span></span>     | [<span data-ttu-id="19edc-141">frammento</span><span class="sxs-lookup"><span data-stu-id="19edc-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="19edc-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="19edc-142">Remarks</span></span>

<span data-ttu-id="19edc-143">L'elemento **sourceFilter** seleziona gli elementi dalla libreria senza considerare le dimensioni del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="19edc-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="19edc-144">L'elemento **Filter** , invece, limita le dimensioni del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="19edc-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="19edc-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="19edc-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
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
```



## <a name="requirements"></a><span data-ttu-id="19edc-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19edc-146">Requirements</span></span>



| <span data-ttu-id="19edc-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="19edc-147">Requirement</span></span> | <span data-ttu-id="19edc-148">Valore</span><span class="sxs-lookup"><span data-stu-id="19edc-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="19edc-149">Versione</span><span class="sxs-lookup"><span data-stu-id="19edc-149">Version</span></span><br/> | <span data-ttu-id="19edc-150">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="19edc-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19edc-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19edc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19edc-152">**Filter-elemento**</span><span class="sxs-lookup"><span data-stu-id="19edc-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="19edc-153">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="19edc-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="19edc-154">**Elemento querySet**</span><span class="sxs-lookup"><span data-stu-id="19edc-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="19edc-155">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="19edc-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






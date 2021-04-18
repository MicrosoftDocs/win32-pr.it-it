---
title: Elemento querySet
description: L'elemento querySet contiene elementi che definiscono quali elementi multimediali verranno selezionati dalla libreria.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Finestra elementi querySet Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331217"
---
# <a name="queryset-element"></a><span data-ttu-id="72f57-104">Elemento querySet</span><span class="sxs-lookup"><span data-stu-id="72f57-104">querySet Element</span></span>

<span data-ttu-id="72f57-105">L'elemento **querySet** contiene elementi che definiscono quali elementi multimediali verranno selezionati dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="72f57-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="72f57-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="72f57-106">Attributes</span></span>

<span data-ttu-id="72f57-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="72f57-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="72f57-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="72f57-108">Parent/Child Elements</span></span>



| <span data-ttu-id="72f57-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="72f57-109">Hierarchy</span></span> | <span data-ttu-id="72f57-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="72f57-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="72f57-111">Padre</span><span class="sxs-lookup"><span data-stu-id="72f57-111">Parent</span></span>    | [<span data-ttu-id="72f57-112">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="72f57-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="72f57-113">Figlio</span><span class="sxs-lookup"><span data-stu-id="72f57-113">Child</span></span>     | [<span data-ttu-id="72f57-114">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="72f57-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="72f57-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="72f57-115">Remarks</span></span>

<span data-ttu-id="72f57-116">L'elemento **querySet** specifica quali elementi multimediali devono essere selezionati dalla libreria, senza considerare le dimensioni del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="72f57-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="72f57-117">L'elemento **Filter** , invece, limita le dimensioni del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="72f57-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="72f57-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="72f57-118">Examples</span></span>


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a><span data-ttu-id="72f57-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72f57-119">Requirements</span></span>



| <span data-ttu-id="72f57-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f57-120">Requirement</span></span> | <span data-ttu-id="72f57-121">Valore</span><span class="sxs-lookup"><span data-stu-id="72f57-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="72f57-122">Versione</span><span class="sxs-lookup"><span data-stu-id="72f57-122">Version</span></span><br/> | <span data-ttu-id="72f57-123">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="72f57-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72f57-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72f57-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f57-125">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="72f57-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="72f57-126">**Filter-elemento**</span><span class="sxs-lookup"><span data-stu-id="72f57-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="72f57-127">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="72f57-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="72f57-128">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="72f57-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="72f57-129">**Elemento sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="72f57-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="72f57-130">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="72f57-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






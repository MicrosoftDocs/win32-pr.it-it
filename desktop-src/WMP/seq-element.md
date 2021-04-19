---
title: Elemento seq
description: L'elemento seq contiene elementi che definiscono una playlist statica o elementi che definiscono una playlist intelligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento seq Media Player Windows
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325828"
---
# <a name="seq-element"></a><span data-ttu-id="848a6-104">Elemento seq</span><span class="sxs-lookup"><span data-stu-id="848a6-104">seq Element</span></span>

<span data-ttu-id="848a6-105">L'elemento **Seq** contiene elementi che definiscono una playlist statica o elementi che definiscono una playlist intelligente.</span><span class="sxs-lookup"><span data-stu-id="848a6-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="848a6-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="848a6-106">Attributes</span></span>

<span data-ttu-id="848a6-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="848a6-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="848a6-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="848a6-108">Parent/Child Elements</span></span>



| <span data-ttu-id="848a6-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="848a6-109">Hierarchy</span></span> | <span data-ttu-id="848a6-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="848a6-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="848a6-111">Padre</span><span class="sxs-lookup"><span data-stu-id="848a6-111">Parent</span></span>    | [<span data-ttu-id="848a6-112">body</span><span class="sxs-lookup"><span data-stu-id="848a6-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="848a6-113">Figlio</span><span class="sxs-lookup"><span data-stu-id="848a6-113">Child</span></span>     | <span data-ttu-id="848a6-114">[supporti](media-element.md), [smartPlaylist](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="848a6-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="848a6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="848a6-115">Remarks</span></span>

<span data-ttu-id="848a6-116">Quando un elemento **Seq** contiene solo elementi **multimediali** che fanno riferimento a elementi multimediali specifici, la playlist viene considerata statica.</span><span class="sxs-lookup"><span data-stu-id="848a6-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="848a6-117">Quando un elemento **Seq** contiene un elemento **smartPlaylist** , viene considerato una playlist dinamica "intelligente".</span><span class="sxs-lookup"><span data-stu-id="848a6-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="848a6-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="848a6-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="848a6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="848a6-119">Requirements</span></span>



| <span data-ttu-id="848a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="848a6-120">Requirement</span></span> | <span data-ttu-id="848a6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="848a6-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="848a6-122">Versione</span><span class="sxs-lookup"><span data-stu-id="848a6-122">Version</span></span><br/> | <span data-ttu-id="848a6-123">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="848a6-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="848a6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="848a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848a6-125">**Body (elemento)**</span><span class="sxs-lookup"><span data-stu-id="848a6-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="848a6-126">**Elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="848a6-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="848a6-127">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="848a6-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="848a6-128">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="848a6-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






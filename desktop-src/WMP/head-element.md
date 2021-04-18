---
title: Elemento Head
description: L'elemento Head contiene i metadati che si applicano all'intera playlist.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Media Player di Windows elemento Head
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328883"
---
# <a name="head-element"></a><span data-ttu-id="48917-104">Elemento Head</span><span class="sxs-lookup"><span data-stu-id="48917-104">head Element</span></span>

<span data-ttu-id="48917-105">L'elemento **Head** contiene i metadati che si applicano all'intera playlist.</span><span class="sxs-lookup"><span data-stu-id="48917-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="48917-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="48917-106">Attributes</span></span>

<span data-ttu-id="48917-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="48917-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="48917-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="48917-108">Parent/Child Elements</span></span>



| <span data-ttu-id="48917-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="48917-109">Hierarchy</span></span> | <span data-ttu-id="48917-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="48917-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="48917-111">Padre</span><span class="sxs-lookup"><span data-stu-id="48917-111">Parent</span></span>    | [<span data-ttu-id="48917-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="48917-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="48917-113">Figlio</span><span class="sxs-lookup"><span data-stu-id="48917-113">Child</span></span>     | <span data-ttu-id="48917-114">[titolo](title-element--wpl.md), [meta](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="48917-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="48917-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="48917-115">Remarks</span></span>

<span data-ttu-id="48917-116">In genere l'elemento **Head** contiene un elemento **title** e uno o più elementi **meta** che definiscono le caratteristiche globali della playlist.</span><span class="sxs-lookup"><span data-stu-id="48917-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="48917-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="48917-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="48917-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48917-118">Requirements</span></span>



| <span data-ttu-id="48917-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="48917-119">Requirement</span></span> | <span data-ttu-id="48917-120">Valore</span><span class="sxs-lookup"><span data-stu-id="48917-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="48917-121">Versione</span><span class="sxs-lookup"><span data-stu-id="48917-121">Version</span></span><br/> | <span data-ttu-id="48917-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="48917-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48917-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48917-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48917-124">**Elemento meta**</span><span class="sxs-lookup"><span data-stu-id="48917-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="48917-125">**Elemento title (WPL)**</span><span class="sxs-lookup"><span data-stu-id="48917-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="48917-126">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="48917-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






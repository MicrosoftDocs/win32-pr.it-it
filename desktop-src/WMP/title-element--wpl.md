---
title: Elemento title (WPL)
description: L'elemento title specifica un titolo per la playlist.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento title (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328869"
---
# <a name="title-element-wpl"></a><span data-ttu-id="e681d-104">Elemento title (WPL)</span><span class="sxs-lookup"><span data-stu-id="e681d-104">title Element (WPL)</span></span>

<span data-ttu-id="e681d-105">L'elemento **title** specifica un titolo per la playlist.</span><span class="sxs-lookup"><span data-stu-id="e681d-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="e681d-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="e681d-106">Attributes</span></span>

<span data-ttu-id="e681d-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="e681d-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="e681d-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="e681d-108">Parent/Child Elements</span></span>



| <span data-ttu-id="e681d-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="e681d-109">Hierarchy</span></span> | <span data-ttu-id="e681d-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="e681d-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="e681d-111">Padre</span><span class="sxs-lookup"><span data-stu-id="e681d-111">Parent</span></span>    | [<span data-ttu-id="e681d-112">Head</span><span class="sxs-lookup"><span data-stu-id="e681d-112">head</span></span>](head-element.md) |
| <span data-ttu-id="e681d-113">Figlio</span><span class="sxs-lookup"><span data-stu-id="e681d-113">Child</span></span>     | <span data-ttu-id="e681d-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="e681d-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="e681d-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e681d-115">Remarks</span></span>

<span data-ttu-id="e681d-116">Quando si sceglie un titolo per una playlist Windows Media (WPL), tenere presente che il contenuto della playlist può essere dinamico.</span><span class="sxs-lookup"><span data-stu-id="e681d-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="e681d-117">Un approccio efficace consiste nel basare il titolo sulla logica negli elementi **argument** perché definisce il contenuto della playlist.</span><span class="sxs-lookup"><span data-stu-id="e681d-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="e681d-118">Esempi di questo argomento sono "canzoni rock preferite da 1966" o "canzoni dance che non ho eseguito di recente".</span><span class="sxs-lookup"><span data-stu-id="e681d-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="e681d-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="e681d-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="e681d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e681d-120">Requirements</span></span>



| <span data-ttu-id="e681d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e681d-121">Requirement</span></span> | <span data-ttu-id="e681d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e681d-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="e681d-123">Versione</span><span class="sxs-lookup"><span data-stu-id="e681d-123">Version</span></span><br/> | <span data-ttu-id="e681d-124">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e681d-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e681d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e681d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e681d-126">**Elemento argument**</span><span class="sxs-lookup"><span data-stu-id="e681d-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="e681d-127">**Elemento Head**</span><span class="sxs-lookup"><span data-stu-id="e681d-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="e681d-128">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e681d-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






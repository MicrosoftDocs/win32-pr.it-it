---
title: Body (elemento)
description: L'elemento Body contiene gli elementi che definiscono il contenuto di una playlist.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Finestra elementi corpo Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331015"
---
# <a name="body-element"></a><span data-ttu-id="3ccdb-104">Body (elemento)</span><span class="sxs-lookup"><span data-stu-id="3ccdb-104">body Element</span></span>

<span data-ttu-id="3ccdb-105">L'elemento **Body** contiene gli elementi che definiscono il contenuto di una playlist.</span><span class="sxs-lookup"><span data-stu-id="3ccdb-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="3ccdb-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="3ccdb-106">Attributes</span></span>

<span data-ttu-id="3ccdb-107">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="3ccdb-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="3ccdb-108">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="3ccdb-108">Parent/Child Elements</span></span>



| <span data-ttu-id="3ccdb-109">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="3ccdb-109">Hierarchy</span></span> | <span data-ttu-id="3ccdb-110">Elementi</span><span class="sxs-lookup"><span data-stu-id="3ccdb-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="3ccdb-111">Padre</span><span class="sxs-lookup"><span data-stu-id="3ccdb-111">Parent</span></span>    | [<span data-ttu-id="3ccdb-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="3ccdb-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="3ccdb-113">Figlio</span><span class="sxs-lookup"><span data-stu-id="3ccdb-113">Child</span></span>     | [<span data-ttu-id="3ccdb-114">Seq</span><span class="sxs-lookup"><span data-stu-id="3ccdb-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="3ccdb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ccdb-115">Remarks</span></span>

<span data-ttu-id="3ccdb-116">Il contenuto di una playlist è organizzato all'interno di un elemento **Seq** contenuto all'interno dell'elemento **Body** .</span><span class="sxs-lookup"><span data-stu-id="3ccdb-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="3ccdb-117">In genere è presente un elemento **Seq** che definisce un set statico di elementi multimediali e contiene elementi **multimediali** oppure ne esiste uno che definisce un set dinamico di elementi multimediali e contiene un elemento **smartPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="3ccdb-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="3ccdb-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ccdb-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="3ccdb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ccdb-119">Requirements</span></span>



| <span data-ttu-id="3ccdb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ccdb-120">Requirement</span></span> | <span data-ttu-id="3ccdb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3ccdb-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="3ccdb-122">Versione</span><span class="sxs-lookup"><span data-stu-id="3ccdb-122">Version</span></span><br/> | <span data-ttu-id="3ccdb-123">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3ccdb-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ccdb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ccdb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ccdb-125">**Elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="3ccdb-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="3ccdb-126">**Elemento seq**</span><span class="sxs-lookup"><span data-stu-id="3ccdb-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="3ccdb-127">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="3ccdb-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="3ccdb-128">**Elemento smil**</span><span class="sxs-lookup"><span data-stu-id="3ccdb-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="3ccdb-129">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3ccdb-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






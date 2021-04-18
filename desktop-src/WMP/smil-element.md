---
title: Elemento smil
description: L'elemento smil è sempre l'elemento di livello principale in un file di playlist Windows Media (WPL). Specifica che il file usa la sintassi e la grammatica di SMIL (Synchronized Multimedia Integration Language).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Finestre degli elementi SMIL Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331741"
---
# <a name="smil-element"></a><span data-ttu-id="96867-105">Elemento smil</span><span class="sxs-lookup"><span data-stu-id="96867-105">smil Element</span></span>

<span data-ttu-id="96867-106">L'elemento **SMIL** è sempre l'elemento di livello principale in un file di playlist Windows Media (WPL).</span><span class="sxs-lookup"><span data-stu-id="96867-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="96867-107">Specifica che il file usa la sintassi e la grammatica di SMIL (Synchronized Multimedia Integration Language).</span><span class="sxs-lookup"><span data-stu-id="96867-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="96867-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="96867-108">Attributes</span></span>

<span data-ttu-id="96867-109">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="96867-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="96867-110">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="96867-110">Parent/Child Elements</span></span>



| <span data-ttu-id="96867-111">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="96867-111">Hierarchy</span></span> | <span data-ttu-id="96867-112">Elementi</span><span class="sxs-lookup"><span data-stu-id="96867-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="96867-113">Padre</span><span class="sxs-lookup"><span data-stu-id="96867-113">Parent</span></span>    | <span data-ttu-id="96867-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="96867-114">None</span></span>                                               |
| <span data-ttu-id="96867-115">Figlio</span><span class="sxs-lookup"><span data-stu-id="96867-115">Child</span></span>     | <span data-ttu-id="96867-116">[Head](head-element.md), [corpo](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="96867-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="96867-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="96867-117">Remarks</span></span>

<span data-ttu-id="96867-118">Ogni playlist di Windows Media deve avere l'elemento **SMIL** alla radice.</span><span class="sxs-lookup"><span data-stu-id="96867-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="96867-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="96867-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="96867-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96867-120">Requirements</span></span>



| <span data-ttu-id="96867-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="96867-121">Requirement</span></span> | <span data-ttu-id="96867-122">Valore</span><span class="sxs-lookup"><span data-stu-id="96867-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="96867-123">Versione</span><span class="sxs-lookup"><span data-stu-id="96867-123">Version</span></span><br/> | <span data-ttu-id="96867-124">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="96867-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96867-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96867-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96867-126">**Body (elemento)**</span><span class="sxs-lookup"><span data-stu-id="96867-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="96867-127">**Elemento Head**</span><span class="sxs-lookup"><span data-stu-id="96867-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="96867-128">**Riferimento agli elementi della playlist Windows Media**</span><span class="sxs-lookup"><span data-stu-id="96867-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






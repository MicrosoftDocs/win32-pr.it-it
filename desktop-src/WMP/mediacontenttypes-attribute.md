---
title: Attributo MediaContentTypes
description: L'attributo MediaContentTypes specifica il tipo di contenuto nell'elemento.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Attributo MediaContentTypes Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327153"
---
# <a name="mediacontenttypes-attribute"></a><span data-ttu-id="e77c7-104">Attributo MediaContentTypes</span><span class="sxs-lookup"><span data-stu-id="e77c7-104">MediaContentTypes Attribute</span></span>

<span data-ttu-id="e77c7-105">L'attributo **MediaContentTypes** specifica il tipo di contenuto nell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e77c7-105">The **MediaContentTypes** attribute specifies the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e77c7-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="e77c7-106">Applies To</span></span>

-   [<span data-ttu-id="e77c7-107">Playlist</span><span class="sxs-lookup"><span data-stu-id="e77c7-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="e77c7-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e77c7-108">Remarks</span></span>

<span data-ttu-id="e77c7-109">Questo attributo può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e77c7-109">This attribute can be one of the following values:</span></span>



| <span data-ttu-id="e77c7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e77c7-110">Value</span></span> | <span data-ttu-id="e77c7-111">Significato</span><span class="sxs-lookup"><span data-stu-id="e77c7-111">Meaning</span></span>                                |
|-------|----------------------------------------|
| <span data-ttu-id="e77c7-112">1</span><span class="sxs-lookup"><span data-stu-id="e77c7-112">1</span></span>     | <span data-ttu-id="e77c7-113">La playlist contiene contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="e77c7-113">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="e77c7-114">2</span><span class="sxs-lookup"><span data-stu-id="e77c7-114">2</span></span>     | <span data-ttu-id="e77c7-115">Da fornire.</span><span class="sxs-lookup"><span data-stu-id="e77c7-115">To be supplied.</span></span>                        |
| <span data-ttu-id="e77c7-116">3</span><span class="sxs-lookup"><span data-stu-id="e77c7-116">3</span></span>     | <span data-ttu-id="e77c7-117">La playlist contiene contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="e77c7-117">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="e77c7-118">4</span><span class="sxs-lookup"><span data-stu-id="e77c7-118">4</span></span>     | <span data-ttu-id="e77c7-119">La playlist contiene contenuto video.</span><span class="sxs-lookup"><span data-stu-id="e77c7-119">The playlist contains video content.</span></span>   |
| <span data-ttu-id="e77c7-120">5</span><span class="sxs-lookup"><span data-stu-id="e77c7-120">5</span></span>     | <span data-ttu-id="e77c7-121">La playlist contiene contenuto immagine.</span><span class="sxs-lookup"><span data-stu-id="e77c7-121">The playlist contains picture content.</span></span> |
| <span data-ttu-id="e77c7-122">6</span><span class="sxs-lookup"><span data-stu-id="e77c7-122">6</span></span>     | <span data-ttu-id="e77c7-123">La playlist contiene contenuto TV.</span><span class="sxs-lookup"><span data-stu-id="e77c7-123">The playlist contains TV content.</span></span>      |



 

<span data-ttu-id="e77c7-124">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e77c7-124">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e77c7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e77c7-125">Requirements</span></span>



| <span data-ttu-id="e77c7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e77c7-126">Requirement</span></span> | <span data-ttu-id="e77c7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e77c7-127">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e77c7-128">Versione</span><span class="sxs-lookup"><span data-stu-id="e77c7-128">Version</span></span><br/> | <span data-ttu-id="e77c7-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e77c7-129">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e77c7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e77c7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e77c7-131">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="e77c7-131">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






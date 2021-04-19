---
title: Attributo MediaType
description: L'attributo MediaType è il tipo di contenuto dell'elemento.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Attributo MediaType Windows Media Player
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327150"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="33c87-104">Attributo MediaType</span><span class="sxs-lookup"><span data-stu-id="33c87-104">MediaType Attribute</span></span>

<span data-ttu-id="33c87-105">L'attributo **mediaType** è il tipo di contenuto dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="33c87-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="33c87-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="33c87-106">Applies To</span></span>

-   [<span data-ttu-id="33c87-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="33c87-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="33c87-108">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="33c87-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="33c87-109">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="33c87-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="33c87-110">Playlist</span><span class="sxs-lookup"><span data-stu-id="33c87-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="33c87-111">Elementi radio</span><span class="sxs-lookup"><span data-stu-id="33c87-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="33c87-112">Elementi video</span><span class="sxs-lookup"><span data-stu-id="33c87-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="33c87-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="33c87-113">Remarks</span></span>

<span data-ttu-id="33c87-114">Questo attributo viene archiviato solo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="33c87-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="33c87-115">Questo attributo ha uno dei valori seguenti: "audio", "altro", "Photo", "playlist", "Radio" o "video".</span><span class="sxs-lookup"><span data-stu-id="33c87-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="33c87-116">Utilizzare questo attributo con *mediacollection*. metodo **getByAttribute** per recuperare una playlist contenente tutti gli elementi di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="33c87-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="33c87-117">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="33c87-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c87-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33c87-118">Requirements</span></span>



| <span data-ttu-id="33c87-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c87-119">Requirement</span></span> | <span data-ttu-id="33c87-120">Valore</span><span class="sxs-lookup"><span data-stu-id="33c87-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="33c87-121">Versione</span><span class="sxs-lookup"><span data-stu-id="33c87-121">Version</span></span><br/> | <span data-ttu-id="33c87-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="33c87-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33c87-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33c87-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c87-124">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="33c87-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="33c87-125">**Mediacollection. getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="33c87-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 






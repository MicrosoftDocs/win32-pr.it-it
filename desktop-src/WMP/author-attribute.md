---
title: Author (attributo)
description: L'attributo Author è il nome di un artista multimediale o di un attore associato al contenuto.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Attributo autore Media Player Windows
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329949"
---
# <a name="author-attribute"></a><span data-ttu-id="3a60c-104">Author (attributo)</span><span class="sxs-lookup"><span data-stu-id="3a60c-104">Author Attribute</span></span>

<span data-ttu-id="3a60c-105">L'attributo **Author** è il nome di un artista multimediale o di un attore associato al contenuto.</span><span class="sxs-lookup"><span data-stu-id="3a60c-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3a60c-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="3a60c-106">Applies To</span></span>

-   [<span data-ttu-id="3a60c-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="3a60c-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3a60c-108">Playlist CD</span><span class="sxs-lookup"><span data-stu-id="3a60c-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="3a60c-109">Tracce CD</span><span class="sxs-lookup"><span data-stu-id="3a60c-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="3a60c-110">File di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="3a60c-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="3a60c-111">DVD</span><span class="sxs-lookup"><span data-stu-id="3a60c-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="3a60c-112">Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="3a60c-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="3a60c-113">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="3a60c-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="3a60c-114">Playlist</span><span class="sxs-lookup"><span data-stu-id="3a60c-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="3a60c-115">Elementi radio</span><span class="sxs-lookup"><span data-stu-id="3a60c-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="3a60c-116">Elementi video</span><span class="sxs-lookup"><span data-stu-id="3a60c-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3a60c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a60c-117">Remarks</span></span>

<span data-ttu-id="3a60c-118">Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale.</span><span class="sxs-lookup"><span data-stu-id="3a60c-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="3a60c-119">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="3a60c-119">This attribute may have multiple values.</span></span> <span data-ttu-id="3a60c-120">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il *supporto*. il metodo **getItemInfoByType** , non il *supporto*. metodo **GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="3a60c-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="3a60c-121">La costante Windows Media Format SDK per questo attributo è g \_ wszWMAuthor.</span><span class="sxs-lookup"><span data-stu-id="3a60c-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="3a60c-122">**Actor** e **Artist** sono alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="3a60c-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="3a60c-123">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3a60c-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a60c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a60c-124">Requirements</span></span>



| <span data-ttu-id="3a60c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a60c-125">Requirement</span></span> | <span data-ttu-id="3a60c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3a60c-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3a60c-127">Versione</span><span class="sxs-lookup"><span data-stu-id="3a60c-127">Version</span></span><br/> | <span data-ttu-id="3a60c-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3a60c-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a60c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a60c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a60c-130">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="3a60c-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






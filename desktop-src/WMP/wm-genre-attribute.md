---
title: Attributo WM/genre
description: L'attributo WM/genre è il genere del contenuto.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Windows Media Player attributo WM/genre
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327017"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="386da-104">Attributo WM/genre</span><span class="sxs-lookup"><span data-stu-id="386da-104">WM/Genre Attribute</span></span>

<span data-ttu-id="386da-105">L'attributo **WM/genre** è il genere del contenuto.</span><span class="sxs-lookup"><span data-stu-id="386da-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="386da-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="386da-106">Applies To</span></span>

-   [<span data-ttu-id="386da-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="386da-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="386da-108">Playlist CD</span><span class="sxs-lookup"><span data-stu-id="386da-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="386da-109">Tracce CD</span><span class="sxs-lookup"><span data-stu-id="386da-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="386da-110">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="386da-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="386da-111">DVD</span><span class="sxs-lookup"><span data-stu-id="386da-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="386da-112">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="386da-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="386da-113">Playlist</span><span class="sxs-lookup"><span data-stu-id="386da-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="386da-114">Elementi video</span><span class="sxs-lookup"><span data-stu-id="386da-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="386da-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="386da-115">Remarks</span></span>

<span data-ttu-id="386da-116">Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="386da-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="386da-117">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="386da-117">This attribute may have multiple values.</span></span> <span data-ttu-id="386da-118">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="386da-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="386da-119">**Genre** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="386da-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="386da-120">La costante Windows Media Format SDK per questo attributo è g \_ wszWMGenre.</span><span class="sxs-lookup"><span data-stu-id="386da-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="386da-121">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="386da-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="386da-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="386da-122">Requirements</span></span>



| <span data-ttu-id="386da-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="386da-123">Requirement</span></span> | <span data-ttu-id="386da-124">Valore</span><span class="sxs-lookup"><span data-stu-id="386da-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="386da-125">Versione</span><span class="sxs-lookup"><span data-stu-id="386da-125">Version</span></span><br/> | <span data-ttu-id="386da-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="386da-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="386da-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="386da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386da-128">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="386da-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="386da-129">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="386da-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






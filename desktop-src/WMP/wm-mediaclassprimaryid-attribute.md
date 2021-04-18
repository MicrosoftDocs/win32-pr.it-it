---
title: Attributo WM/MediaClassPrimaryID
description: L'attributo WM/MediaClassPrimaryID è un GUID che specifica una delle classi multimediali primarie Music, audio non musicale, video o altro.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Media Player Windows per gli attributi WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327005"
---
# <a name="wmmediaclassprimaryid-attribute"></a><span data-ttu-id="1d075-104">Attributo WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="1d075-104">WM/MediaClassPrimaryID Attribute</span></span>

<span data-ttu-id="1d075-105">L'attributo **WM/MediaClassPrimaryID** è un GUID che specifica una delle classi multimediali primarie: musica, audio non musicale, video o altro.</span><span class="sxs-lookup"><span data-stu-id="1d075-105">The **WM/MediaClassPrimaryID** attribute is a GUID specifying one of the primary media classes: music, non-music audio, video, or other.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1d075-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="1d075-106">Applies To</span></span>

-   [<span data-ttu-id="1d075-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="1d075-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1d075-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="1d075-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="1d075-109">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="1d075-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="1d075-110">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="1d075-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="1d075-111">Playlist</span><span class="sxs-lookup"><span data-stu-id="1d075-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="1d075-112">Elementi radio</span><span class="sxs-lookup"><span data-stu-id="1d075-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="1d075-113">Elementi video</span><span class="sxs-lookup"><span data-stu-id="1d075-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1d075-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d075-114">Remarks</span></span>

<span data-ttu-id="1d075-115">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="1d075-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="1d075-116">**MediaClassPrimaryID** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="1d075-116">**MediaClassPrimaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="1d075-117">La costante Windows Media Format SDK per questo attributo è g \_ wszWMMediaClassPrimaryID.</span><span class="sxs-lookup"><span data-stu-id="1d075-117">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassPrimaryID.</span></span>

<span data-ttu-id="1d075-118">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1d075-118">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d075-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d075-119">Requirements</span></span>



| <span data-ttu-id="1d075-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d075-120">Requirement</span></span> | <span data-ttu-id="1d075-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1d075-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d075-122">Versione</span><span class="sxs-lookup"><span data-stu-id="1d075-122">Version</span></span><br/> | <span data-ttu-id="1d075-123">Windows Media Player 9 Series o versione successiva (l'elemento Photo è supportato solo in Windows Media Player 10 o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="1d075-123">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d075-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d075-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d075-125">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="1d075-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






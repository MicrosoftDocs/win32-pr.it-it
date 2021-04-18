---
title: Attributo DisplayArtist
description: L'attributo DisplayArtist è il nome dell'artista visualizzato per un elemento.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Attributo DisplayArtist Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327624"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="f4705-104">Attributo DisplayArtist</span><span class="sxs-lookup"><span data-stu-id="f4705-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="f4705-105">L'attributo **DisplayArtist** è il nome dell'artista visualizzato per un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4705-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f4705-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="f4705-106">Applies To</span></span>

-   [<span data-ttu-id="f4705-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="f4705-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f4705-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4705-108">Remarks</span></span>

<span data-ttu-id="f4705-109">In genere, **DisplayArtist** avrà lo stesso valore dell'attributo **WM/AlbumArtist** quando viene impostato l'attributo.</span><span class="sxs-lookup"><span data-stu-id="f4705-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="f4705-110">In caso contrario, il valore sarà il nome dell'artista associato alla prima traccia sull'album.</span><span class="sxs-lookup"><span data-stu-id="f4705-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="f4705-111">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f4705-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4705-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4705-112">Requirements</span></span>



| <span data-ttu-id="f4705-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4705-113">Requirement</span></span> | <span data-ttu-id="f4705-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f4705-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="f4705-115">Versione</span><span class="sxs-lookup"><span data-stu-id="f4705-115">Version</span></span><br/> | <span data-ttu-id="f4705-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="f4705-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4705-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4705-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4705-118">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="f4705-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="f4705-119">**Attributo WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="f4705-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 






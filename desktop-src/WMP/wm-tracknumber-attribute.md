---
title: Attributo WM/numero
description: L'attributo WM/numero è il numero di traccia dell'elemento sull'album in cui è stato rilasciato originariamente.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Media Player Windows per gli attributi WM/numero
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329701"
---
# <a name="wmtracknumber-attribute"></a><span data-ttu-id="8b58b-104">Attributo WM/numero</span><span class="sxs-lookup"><span data-stu-id="8b58b-104">WM/TrackNumber Attribute</span></span>

<span data-ttu-id="8b58b-105">L'attributo **WM/numero** è il numero di traccia dell'elemento sull'album in cui è stato rilasciato originariamente.</span><span class="sxs-lookup"><span data-stu-id="8b58b-105">The **WM/TrackNumber** attribute is the track number of the item on the album on which it was originally released.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8b58b-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="8b58b-106">Applies To</span></span>

-   [<span data-ttu-id="8b58b-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="8b58b-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="8b58b-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="8b58b-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="8b58b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b58b-109">Remarks</span></span>

<span data-ttu-id="8b58b-110">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="8b58b-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="8b58b-111">I numeri di traccia per un album iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="8b58b-111">Track numbers for an album start at 1.</span></span>

<span data-ttu-id="8b58b-112">**OriginalIndex** e **OriginalIndexLeft** sono alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="8b58b-112">**OriginalIndex** and **OriginalIndexLeft** are aliases for this attribute.</span></span>

<span data-ttu-id="8b58b-113">La costante Windows Media Format SDK per questo attributo è g \_ wszWMTrackNumber.</span><span class="sxs-lookup"><span data-stu-id="8b58b-113">The Windows Media Format SDK constant for this attribute is g\_wszWMTrackNumber.</span></span>

<span data-ttu-id="8b58b-114">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8b58b-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b58b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b58b-115">Requirements</span></span>



| <span data-ttu-id="8b58b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b58b-116">Requirement</span></span> | <span data-ttu-id="8b58b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8b58b-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8b58b-118">Versione</span><span class="sxs-lookup"><span data-stu-id="8b58b-118">Version</span></span><br/> | <span data-ttu-id="8b58b-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8b58b-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b58b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b58b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b58b-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="8b58b-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






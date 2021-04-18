---
title: Attributo WM/MediaClassSecondaryID
description: L'attributo WM/MediaClassSecondaryID è un GUID che specifica la classe multimediale secondaria, che è una sottoclasse della classe multimediale primaria.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Media Player Windows per gli attributi WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327003"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="5a510-104">Attributo WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="5a510-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="5a510-105">L'attributo **WM/MediaClassSecondaryID** è un GUID che specifica la classe multimediale secondaria, che è una sottoclasse della classe multimediale primaria.</span><span class="sxs-lookup"><span data-stu-id="5a510-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5a510-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="5a510-106">Applies To</span></span>

-   [<span data-ttu-id="5a510-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="5a510-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5a510-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="5a510-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="5a510-109">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="5a510-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="5a510-110">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="5a510-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="5a510-111">Playlist</span><span class="sxs-lookup"><span data-stu-id="5a510-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="5a510-112">Elementi radio</span><span class="sxs-lookup"><span data-stu-id="5a510-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="5a510-113">Elementi video</span><span class="sxs-lookup"><span data-stu-id="5a510-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5a510-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a510-114">Remarks</span></span>

<span data-ttu-id="5a510-115">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="5a510-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="5a510-116">La tabella seguente elenca i GUID supportati e le relative descrizioni.</span><span class="sxs-lookup"><span data-stu-id="5a510-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="5a510-117">GUID</span><span class="sxs-lookup"><span data-stu-id="5a510-117">GUID</span></span>                                 | <span data-ttu-id="5a510-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a510-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="5a510-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="5a510-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="5a510-120">L'oggetto multimediale rappresenta una playlist statica.</span><span class="sxs-lookup"><span data-stu-id="5a510-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="5a510-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="5a510-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="5a510-122">L'oggetto multimediale rappresenta una playlist automatica.</span><span class="sxs-lookup"><span data-stu-id="5a510-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="5a510-123">**MediaClassSecondaryID** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="5a510-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="5a510-124">La costante Windows Media Format SDK per questo attributo è g \_ wszWMMediaClassSecondaryID.</span><span class="sxs-lookup"><span data-stu-id="5a510-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="5a510-125">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5a510-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a510-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a510-126">Requirements</span></span>



| <span data-ttu-id="5a510-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a510-127">Requirement</span></span> | <span data-ttu-id="5a510-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5a510-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a510-129">Versione</span><span class="sxs-lookup"><span data-stu-id="5a510-129">Version</span></span><br/> | <span data-ttu-id="5a510-130">L'elemento Photo è supportato solo in Windows Media Player 10 o versioni successive l'elemento radio è supportato solo in Windows Media Player 9 Series tutti gli altri elementi sono supportati in Windows Media Player 9 Series e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5a510-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a510-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a510-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a510-132">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="5a510-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






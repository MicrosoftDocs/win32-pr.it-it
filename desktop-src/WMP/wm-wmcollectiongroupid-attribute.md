---
title: Attributo WM/WMCollectionGroupID
description: L'attributo WM/WMCollectionGroupID è un GUID che identifica il gruppo che contiene la raccolta a cui appartiene l'elemento.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Media Player Windows per gli attributi WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329693"
---
# <a name="wmwmcollectiongroupid-attribute"></a><span data-ttu-id="77550-104">Attributo WM/WMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="77550-104">WM/WMCollectionGroupID Attribute</span></span>

<span data-ttu-id="77550-105">L'attributo **WM/WMCollectionGroupID** è un GUID che identifica il gruppo che contiene la raccolta a cui appartiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="77550-105">The **WM/WMCollectionGroupID** attribute is a GUID identifying the group containing the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="77550-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="77550-106">Applies To</span></span>

-   [<span data-ttu-id="77550-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="77550-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="77550-108">Playlist CD</span><span class="sxs-lookup"><span data-stu-id="77550-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="77550-109">Tracce CD</span><span class="sxs-lookup"><span data-stu-id="77550-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="77550-110">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="77550-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="77550-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="77550-111">Remarks</span></span>

<span data-ttu-id="77550-112">Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="77550-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="77550-113">**WMCollectionGroupID** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="77550-113">**WMCollectionGroupID** is an alias for this attribute.</span></span>

<span data-ttu-id="77550-114">La costante Windows Media Format SDK per questo attributo è g \_ wszWMCollectionGroupID.</span><span class="sxs-lookup"><span data-stu-id="77550-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionGroupID.</span></span>

<span data-ttu-id="77550-115">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="77550-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="77550-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77550-116">Requirements</span></span>



| <span data-ttu-id="77550-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77550-117">Requirement</span></span> | <span data-ttu-id="77550-118">Valore</span><span class="sxs-lookup"><span data-stu-id="77550-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="77550-119">Versione</span><span class="sxs-lookup"><span data-stu-id="77550-119">Version</span></span><br/> | <span data-ttu-id="77550-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="77550-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77550-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77550-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77550-122">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="77550-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






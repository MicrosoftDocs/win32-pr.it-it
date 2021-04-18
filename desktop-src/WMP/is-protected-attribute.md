---
title: Attributo Is_Protected
description: L' \_ attributo is protected indica se il contenuto è protetto tramite Digital Rights Management (DRM).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected attributo di Windows Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333755"
---
# <a name="is_protected-attribute"></a><span data-ttu-id="1a363-104">\_Attributo protetto</span><span class="sxs-lookup"><span data-stu-id="1a363-104">Is\_Protected Attribute</span></span>

<span data-ttu-id="1a363-105">L'attributo **is \_ protected** indica se il contenuto è protetto tramite Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="1a363-105">The **Is\_Protected** attribute indicates whether the content is protected using digital rights management (DRM).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1a363-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="1a363-106">Applies To</span></span>

-   [<span data-ttu-id="1a363-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="1a363-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1a363-108">File di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="1a363-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="1a363-109">Elementi video</span><span class="sxs-lookup"><span data-stu-id="1a363-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1a363-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a363-110">Remarks</span></span>

<span data-ttu-id="1a363-111">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="1a363-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="1a363-112">**DigitallySecure** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="1a363-112">**DigitallySecure** is an alias for this attribute.</span></span>

<span data-ttu-id="1a363-113">La costante Windows Media Format SDK per questo attributo è g \_ wszWMProtected.</span><span class="sxs-lookup"><span data-stu-id="1a363-113">The Windows Media Format SDK constant for this attribute is g\_wszWMProtected.</span></span>

<span data-ttu-id="1a363-114">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1a363-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a363-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a363-115">Requirements</span></span>



| <span data-ttu-id="1a363-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a363-116">Requirement</span></span> | <span data-ttu-id="1a363-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1a363-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1a363-118">Versione</span><span class="sxs-lookup"><span data-stu-id="1a363-118">Version</span></span><br/> | <span data-ttu-id="1a363-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1a363-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a363-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a363-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a363-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="1a363-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






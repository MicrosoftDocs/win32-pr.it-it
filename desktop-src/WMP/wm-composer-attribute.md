---
title: Attributo WM/Composer
description: L'attributo WM/Composer è il nome del compositore di Music.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Windows Media Player attributo WM/Composer
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327030"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="b23bc-104">Attributo WM/Composer</span><span class="sxs-lookup"><span data-stu-id="b23bc-104">WM/Composer Attribute</span></span>

<span data-ttu-id="b23bc-105">L'attributo **WM/Composer** è il nome del compositore di Music.</span><span class="sxs-lookup"><span data-stu-id="b23bc-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b23bc-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b23bc-106">Applies To</span></span>

-   [<span data-ttu-id="b23bc-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="b23bc-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b23bc-108">Playlist CD</span><span class="sxs-lookup"><span data-stu-id="b23bc-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="b23bc-109">Tracce CD</span><span class="sxs-lookup"><span data-stu-id="b23bc-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="b23bc-110">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="b23bc-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b23bc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b23bc-111">Remarks</span></span>

<span data-ttu-id="b23bc-112">Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="b23bc-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="b23bc-113">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="b23bc-113">This attribute may have multiple values.</span></span> <span data-ttu-id="b23bc-114">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="b23bc-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="b23bc-115">**Composer** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b23bc-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="b23bc-116">La costante Windows Media Format SDK per questo attributo è g \_ wszWMComposer.</span><span class="sxs-lookup"><span data-stu-id="b23bc-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="b23bc-117">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b23bc-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b23bc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b23bc-118">Requirements</span></span>



| <span data-ttu-id="b23bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b23bc-119">Requirement</span></span> | <span data-ttu-id="b23bc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b23bc-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b23bc-121">Versione</span><span class="sxs-lookup"><span data-stu-id="b23bc-121">Version</span></span><br/> | <span data-ttu-id="b23bc-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b23bc-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b23bc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b23bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23bc-124">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="b23bc-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b23bc-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b23bc-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






---
title: Attributo WM/Conductor
description: L'attributo WM/Conductor è il nome del conduttore della musica.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- Attributi WM/Conductor Media Player Windows
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327029"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="83644-104">Attributo WM/Conductor</span><span class="sxs-lookup"><span data-stu-id="83644-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="83644-105">L'attributo **WM/Conductor** è il nome del conduttore della musica.</span><span class="sxs-lookup"><span data-stu-id="83644-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="83644-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="83644-106">Applies To</span></span>

-   [<span data-ttu-id="83644-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="83644-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="83644-108">Tracce CD</span><span class="sxs-lookup"><span data-stu-id="83644-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="83644-109">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="83644-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="83644-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="83644-110">Remarks</span></span>

<span data-ttu-id="83644-111">Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="83644-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="83644-112">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="83644-112">This attribute may have multiple values.</span></span> <span data-ttu-id="83644-113">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="83644-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="83644-114">Il **conduttore** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="83644-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="83644-115">La costante Windows Media Format SDK per questo attributo è g \_ wszWMConductor.</span><span class="sxs-lookup"><span data-stu-id="83644-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="83644-116">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="83644-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="83644-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83644-117">Requirements</span></span>



| <span data-ttu-id="83644-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83644-118">Requirement</span></span> | <span data-ttu-id="83644-119">Valore</span><span class="sxs-lookup"><span data-stu-id="83644-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="83644-120">Versione</span><span class="sxs-lookup"><span data-stu-id="83644-120">Version</span></span><br/> | <span data-ttu-id="83644-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="83644-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83644-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83644-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83644-123">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="83644-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="83644-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="83644-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






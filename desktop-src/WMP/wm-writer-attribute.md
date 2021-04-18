---
title: Attributo WM/writer
description: L'attributo WM/writer è il nome del writer che ha scritto le parole del contenuto.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Attributo WM/Writer Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329681"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="70dd2-104">Attributo WM/writer</span><span class="sxs-lookup"><span data-stu-id="70dd2-104">WM/Writer Attribute</span></span>

<span data-ttu-id="70dd2-105">L'attributo **WM/writer** è il nome del writer che ha scritto le parole del contenuto.</span><span class="sxs-lookup"><span data-stu-id="70dd2-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="70dd2-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="70dd2-106">Applies To</span></span>

-   [<span data-ttu-id="70dd2-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="70dd2-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="70dd2-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="70dd2-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="70dd2-109">Elementi video</span><span class="sxs-lookup"><span data-stu-id="70dd2-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="70dd2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="70dd2-110">Remarks</span></span>

<span data-ttu-id="70dd2-111">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="70dd2-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="70dd2-112">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="70dd2-112">This attribute may have multiple values.</span></span> <span data-ttu-id="70dd2-113">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="70dd2-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="70dd2-114">**Writer** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="70dd2-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="70dd2-115">La costante Windows Media Format SDK per questo attributo è g \_ wszWMWriter.</span><span class="sxs-lookup"><span data-stu-id="70dd2-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="70dd2-116">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="70dd2-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70dd2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70dd2-117">Requirements</span></span>



| <span data-ttu-id="70dd2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="70dd2-118">Requirement</span></span> | <span data-ttu-id="70dd2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="70dd2-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="70dd2-120">Versione</span><span class="sxs-lookup"><span data-stu-id="70dd2-120">Version</span></span><br/> | <span data-ttu-id="70dd2-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="70dd2-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70dd2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70dd2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70dd2-123">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="70dd2-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="70dd2-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="70dd2-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






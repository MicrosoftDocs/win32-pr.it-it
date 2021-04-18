---
title: Attributo WM/Language
description: L'attributo WM/Language è la lingua dell'elemento.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Finestra degli attributi WM/Language Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327011"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="2a5c0-104">Attributo WM/Language</span><span class="sxs-lookup"><span data-stu-id="2a5c0-104">WM/Language Attribute</span></span>

<span data-ttu-id="2a5c0-105">L'attributo **WM/Language** è la lingua dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2a5c0-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="2a5c0-106">Applies To</span></span>

-   [<span data-ttu-id="2a5c0-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="2a5c0-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="2a5c0-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="2a5c0-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="2a5c0-109">Elementi radio</span><span class="sxs-lookup"><span data-stu-id="2a5c0-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="2a5c0-110">Elementi video</span><span class="sxs-lookup"><span data-stu-id="2a5c0-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="2a5c0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a5c0-111">Remarks</span></span>

<span data-ttu-id="2a5c0-112">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="2a5c0-113">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-113">This attribute may have multiple values.</span></span> <span data-ttu-id="2a5c0-114">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="2a5c0-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="2a5c0-115">**Language** è un alias per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="2a5c0-116">La costante Windows Media Format SDK per questo attributo è g \_ wszWMLanguage.</span><span class="sxs-lookup"><span data-stu-id="2a5c0-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="2a5c0-117">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2a5c0-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a5c0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a5c0-118">Requirements</span></span>



| <span data-ttu-id="2a5c0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a5c0-119">Requirement</span></span> | <span data-ttu-id="2a5c0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2a5c0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5c0-121">Versione</span><span class="sxs-lookup"><span data-stu-id="2a5c0-121">Version</span></span><br/> | <span data-ttu-id="2a5c0-122">Windows Media Player 9 Series o versione successiva (l'elemento radio è supportato solo nella serie Windows Media Player 9)</span><span class="sxs-lookup"><span data-stu-id="2a5c0-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a5c0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a5c0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a5c0-124">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="2a5c0-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="2a5c0-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="2a5c0-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






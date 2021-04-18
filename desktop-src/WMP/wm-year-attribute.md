---
title: Attributo WM/Year
description: L'attributo WM/Year è l'anno in cui è stato pubblicato il contenuto.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Media Player di Windows per gli attributi WM/Year
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329679"
---
# <a name="wmyear-attribute"></a><span data-ttu-id="53495-104">Attributo WM/Year</span><span class="sxs-lookup"><span data-stu-id="53495-104">WM/Year Attribute</span></span>

<span data-ttu-id="53495-105">L'attributo **WM/Year** è l'anno in cui è stato pubblicato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="53495-105">The **WM/Year** attribute is the year the content was published.</span></span>

## <a name="applies-to"></a><span data-ttu-id="53495-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="53495-106">Applies To</span></span>

-   [<span data-ttu-id="53495-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="53495-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="53495-108">Attributi di file di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="53495-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="53495-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="53495-109">Remarks</span></span>

<span data-ttu-id="53495-110">Questo attributo viene archiviato solo nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="53495-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="53495-111">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="53495-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

<span data-ttu-id="53495-112">Questo attributo non deve essere utilizzato come parte di una condizione di query.</span><span class="sxs-lookup"><span data-stu-id="53495-112">This attribute should not be used as part of a query condition.</span></span> <span data-ttu-id="53495-113">È derivato da un altro attributo e non può essere sottoposto a query direttamente in una raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="53495-113">It is derived from another attribute and cannot be directly queried against in a media collection.</span></span>

<span data-ttu-id="53495-114">La costante Windows Media Format SDK per questo attributo è g \_ wszWMYear.</span><span class="sxs-lookup"><span data-stu-id="53495-114">The Windows Media Format SDK constant for this attribute is g\_wszWMYear.</span></span>

## <a name="requirements"></a><span data-ttu-id="53495-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53495-115">Requirements</span></span>



| <span data-ttu-id="53495-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="53495-116">Requirement</span></span> | <span data-ttu-id="53495-117">Valore</span><span class="sxs-lookup"><span data-stu-id="53495-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53495-118">Versione</span><span class="sxs-lookup"><span data-stu-id="53495-118">Version</span></span><br/> | <span data-ttu-id="53495-119">Windows Media Player 9 Series Windows Media Player 10 o versioni successive non supporta questo attributo</span><span class="sxs-lookup"><span data-stu-id="53495-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53495-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53495-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53495-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="53495-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






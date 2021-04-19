---
title: Attributo PeakValue
description: L'attributo PeakValue è un valore di ampiezza a 16 bit che indica il livello di picco del volume.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Attributo PeakValue Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332678"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="5f932-104">Attributo PeakValue</span><span class="sxs-lookup"><span data-stu-id="5f932-104">PeakValue Attribute</span></span>

<span data-ttu-id="5f932-105">L'attributo **PeakValue** è un valore di ampiezza a 16 bit che indica il livello di picco del volume.</span><span class="sxs-lookup"><span data-stu-id="5f932-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5f932-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="5f932-106">Applies To</span></span>

-   [<span data-ttu-id="5f932-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="5f932-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5f932-108">File di Windows Media usati di frequente</span><span class="sxs-lookup"><span data-stu-id="5f932-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5f932-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f932-109">Remarks</span></span>

<span data-ttu-id="5f932-110">Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="5f932-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="5f932-111">Windows Media Player imposta questo valore in una delle istanze seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f932-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="5f932-112">Dopo l'estrazione di un file.</span><span class="sxs-lookup"><span data-stu-id="5f932-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="5f932-113">Dopo aver riprodotto un file (quando è abilitata la funzionalità avanzata di livellamento automatico del volume).</span><span class="sxs-lookup"><span data-stu-id="5f932-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="5f932-114">La costante Windows Media Format SDK per questo attributo è g \_ wszPeakValue.</span><span class="sxs-lookup"><span data-stu-id="5f932-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="5f932-115">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5f932-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f932-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f932-116">Requirements</span></span>



| <span data-ttu-id="5f932-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f932-117">Requirement</span></span> | <span data-ttu-id="5f932-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f932-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="5f932-119">Versione</span><span class="sxs-lookup"><span data-stu-id="5f932-119">Version</span></span><br/> | <span data-ttu-id="5f932-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5f932-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f932-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f932-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f932-122">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="5f932-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






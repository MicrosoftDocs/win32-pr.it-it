---
description: Contiene la decodifica timestamp (DTS) per l'esempio.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Attributo MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309097"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="1c28b-103">\_Attributo DecodeTimestamp di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="1c28b-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="1c28b-104">Contiene la decodifica timestamp (DTS) per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="1c28b-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c28b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1c28b-105">Data type</span></span>

<span data-ttu-id="1c28b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1c28b-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c28b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c28b-107">Remarks</span></span>

<span data-ttu-id="1c28b-108">Il valore dell'attributo è il DTS in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1c28b-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="1c28b-109">DTS è definito in alcuni standard di codifica, incluso MPEG.</span><span class="sxs-lookup"><span data-stu-id="1c28b-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="1c28b-110">Il DTS specifica quando l'immagine codificata deve essere decodificata.</span><span class="sxs-lookup"><span data-stu-id="1c28b-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="1c28b-111">Se il video codificato contiene i frame B, DTS può differire dall'ora di presentazione, perché le immagini B appaiono fuori dall'ordine temporale nel bitstream.</span><span class="sxs-lookup"><span data-stu-id="1c28b-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c28b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c28b-112">Requirements</span></span>



| <span data-ttu-id="1c28b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c28b-113">Requirement</span></span> | <span data-ttu-id="1c28b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1c28b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c28b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c28b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1c28b-116">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1c28b-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1c28b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c28b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1c28b-118">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c28b-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1c28b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c28b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c28b-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c28b-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c28b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c28b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c28b-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c28b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c28b-123">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="1c28b-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 





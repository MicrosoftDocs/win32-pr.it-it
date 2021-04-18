---
description: Offset tra il timestamp di ogni campione ricevuto dal grabber di esempio e l'ora in cui l'esempio Grabber presenta l'esempio.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Attributo MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308456"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="0269b-103">\_Attributo di \_ offset dell'ora di esempio MF SAMPLEGRABBERSINK \_ \_</span><span class="sxs-lookup"><span data-stu-id="0269b-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="0269b-104">Offset tra il timestamp di ogni campione ricevuto dal grabber di esempio e l'ora in cui l'esempio Grabber presenta l'esempio.</span><span class="sxs-lookup"><span data-stu-id="0269b-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="0269b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0269b-105">Data type</span></span>

<span data-ttu-id="0269b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0269b-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="0269b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="0269b-107">Remarks</span></span>

<span data-ttu-id="0269b-108">È possibile impostare questo attributo sull'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito dalla funzione [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="0269b-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="0269b-109">Questo attributo consente alla funzione di callback del grabber di esempio di ricevere esempi prima dell'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="0269b-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="0269b-110">Quando l'esempio Grabber riceve un nuovo esempio, viene visualizzato il valore di esempio at time *t* - *offset*, dove *t* è il timestamp dell'esempio e *offset* è il valore di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="0269b-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="0269b-111">Se questo attributo non è impostato, il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="0269b-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="0269b-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0269b-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0269b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0269b-113">Requirements</span></span>



| <span data-ttu-id="0269b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0269b-114">Requirement</span></span> | <span data-ttu-id="0269b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0269b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0269b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0269b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0269b-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0269b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0269b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0269b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0269b-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0269b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0269b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0269b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0269b-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0269b-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0269b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0269b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0269b-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0269b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0269b-124">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="0269b-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="0269b-125">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="0269b-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="0269b-126">**IMFSampleGrabberSinkCallback**</span><span class="sxs-lookup"><span data-stu-id="0269b-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="0269b-127">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0269b-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 





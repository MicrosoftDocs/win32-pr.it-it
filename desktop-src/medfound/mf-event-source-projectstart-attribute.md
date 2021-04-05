---
description: Specifica l'ora di inizio per una topologia di segmento.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Attributo MF_EVENT_SOURCE_PROJECTSTART (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885761"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="b9e7c-103">\_ \_ Attributo PROJECTSTART dell'origine evento MF \_</span><span class="sxs-lookup"><span data-stu-id="b9e7c-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="b9e7c-104">Specifica l'ora di inizio per una topologia di segmento.</span><span class="sxs-lookup"><span data-stu-id="b9e7c-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9e7c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b9e7c-105">Data type</span></span>

<span data-ttu-id="b9e7c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b9e7c-106">**UINT64**</span></span>

<span data-ttu-id="b9e7c-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="b9e7c-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e7c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9e7c-108">Remarks</span></span>

<span data-ttu-id="b9e7c-109">Questo attributo viene utilizzato con l'evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="b9e7c-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="b9e7c-110">L'origine di Sequencer imposta questo attributo quando la topologia del segmento corrente ha l'attributo [**\_ \_ PROJECTSTART della topologia MF**](mf-topology-projectstart-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b9e7c-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="b9e7c-111">I due attributi hanno lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="b9e7c-111">The two attributes have the same value.</span></span>

<span data-ttu-id="b9e7c-112">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="b9e7c-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="b9e7c-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b9e7c-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e7c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9e7c-114">Requirements</span></span>



| <span data-ttu-id="b9e7c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9e7c-115">Requirement</span></span> | <span data-ttu-id="b9e7c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b9e7c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e7c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9e7c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e7c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9e7c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b9e7c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9e7c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e7c-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9e7c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9e7c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9e7c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e7c-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e7c-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e7c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9e7c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e7c-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9e7c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9e7c-125">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="b9e7c-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9e7c-126">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="b9e7c-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="b9e7c-127">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="b9e7c-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





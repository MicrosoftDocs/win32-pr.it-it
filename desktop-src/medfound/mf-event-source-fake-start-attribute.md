---
description: Specifica se la topologia del segmento corrente è vuota.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Attributo MF_EVENT_SOURCE_FAKE_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885762"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="34ce9-103">\_Attributo di \_ \_ avvio Fake \_ origine evento MF</span><span class="sxs-lookup"><span data-stu-id="34ce9-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="34ce9-104">Specifica se la topologia del segmento corrente è vuota.</span><span class="sxs-lookup"><span data-stu-id="34ce9-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="34ce9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="34ce9-105">Data type</span></span>

<span data-ttu-id="34ce9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="34ce9-106">**UINT32**</span></span>

<span data-ttu-id="34ce9-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="34ce9-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34ce9-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="34ce9-108">Remarks</span></span>

<span data-ttu-id="34ce9-109">Questo attributo viene utilizzato con l'evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="34ce9-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="34ce9-110">L'origine di Sequencer imposta questo attributo su **true** se la topologia del segmento corrente è vuota.</span><span class="sxs-lookup"><span data-stu-id="34ce9-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="34ce9-111">Se questo attributo è **true**, la riproduzione non è ancora stata avviata.</span><span class="sxs-lookup"><span data-stu-id="34ce9-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="34ce9-112">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="34ce9-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="34ce9-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="34ce9-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ce9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34ce9-114">Requirements</span></span>



| <span data-ttu-id="34ce9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ce9-115">Requirement</span></span> | <span data-ttu-id="34ce9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="34ce9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34ce9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34ce9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="34ce9-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34ce9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34ce9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34ce9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="34ce9-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34ce9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34ce9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34ce9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="34ce9-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="34ce9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34ce9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34ce9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ce9-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34ce9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="34ce9-125">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="34ce9-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="34ce9-126">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="34ce9-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="34ce9-127">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="34ce9-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 





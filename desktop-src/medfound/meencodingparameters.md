---
description: Inviato dalla pipeline al codificatore MFTs seriale con esempi di supporti tramite IMFTransform::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Evento MEEncodingParameters (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226664"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="0a6e9-103">Evento MEEncodingParameters</span><span class="sxs-lookup"><span data-stu-id="0a6e9-103">MEEncodingParameters event</span></span>

<span data-ttu-id="0a6e9-104">Inviato dalla pipeline al codificatore MFTs seriale con esempi di supporti tramite [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="0a6e9-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="0a6e9-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="0a6e9-105">Event values</span></span>

<span data-ttu-id="0a6e9-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0a6e9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a6e9-107">VARTYPE</span></span>              | <span data-ttu-id="0a6e9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a6e9-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0a6e9-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="0a6e9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0a6e9-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="0a6e9-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="0a6e9-111">Attributes</span></span>

<span data-ttu-id="0a6e9-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="0a6e9-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="0a6e9-113">Attribute</span></span>                                         | <span data-ttu-id="0a6e9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a6e9-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a6e9-115">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="0a6e9-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="0a6e9-116">Contiene le nuove impostazioni basate su ICodecAPI che il codificatore deve applicare ai successivi esempi in arrivo.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0a6e9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a6e9-117">Remarks</span></span>

<span data-ttu-id="0a6e9-118">Il payload dell'evento è un archivio di attributi (puntatore IMFAttributes) che contiene le nuove impostazioni basate su ICodecAPI///che il codificatore deve applicare ai successivi esempi in arrivo.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6e9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a6e9-119">Requirements</span></span>



| <span data-ttu-id="0a6e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a6e9-120">Requirement</span></span> | <span data-ttu-id="0a6e9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0a6e9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6e9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a6e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6e9-123">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a6e9-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0a6e9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a6e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6e9-125">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a6e9-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="0a6e9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a6e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a6e9-127"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a6e9-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a6e9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a6e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6e9-129">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a6e9-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





---
description: Il flusso multimediale usa questo evento per inviare metadati specifici del sistema di protezione al decodificatore.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879822"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="b2dc3-103">Evento MEContentProtectionMetadata</span><span class="sxs-lookup"><span data-stu-id="b2dc3-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="b2dc3-104">Il flusso multimediale usa questo evento per inviare metadati specifici del sistema di protezione al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="b2dc3-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="b2dc3-105">Event values</span></span>

<span data-ttu-id="b2dc3-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b2dc3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b2dc3-107">VARTYPE</span></span>              | <span data-ttu-id="b2dc3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2dc3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b2dc3-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="b2dc3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b2dc3-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="b2dc3-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="b2dc3-111">Attributes</span></span>

<span data-ttu-id="b2dc3-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="b2dc3-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="b2dc3-113">Attribute</span></span>                                                                                              | <span data-ttu-id="b2dc3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2dc3-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2dc3-115">\_dati di \_ metadati del flusso di eventi MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2dc3-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="b2dc3-116">Questo è un attributo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-116">This is an optional attribute.</span></span> <span data-ttu-id="b2dc3-117">Dati specifici del sistema di protezione.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="b2dc3-118">\_ \_ \_ \_ KEYIDS contenuto metadati flusso di eventi MF \_</span><span class="sxs-lookup"><span data-stu-id="b2dc3-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="b2dc3-119">ID della chiave simmetrica a cui è associato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="b2dc3-120">\_ \_ SYSTEMID metadati del flusso di eventi MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2dc3-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="b2dc3-121">Questo è un attributo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-121">This is an optional attribute.</span></span> <span data-ttu-id="b2dc3-122">ID di sistema per il quale sono previsti i dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b2dc3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2dc3-123">Remarks</span></span>

<span data-ttu-id="b2dc3-124">Questo evento viene usato, ad esempio, per la comunicazione dell'evento di rotazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="b2dc3-125">In questo caso deve essere inviato il prima possibile per fornire al decodificatore il tempo necessario per prepararsi prima che i campioni crittografati con il nuovo ID chiave inizino ad arrivare.</span><span class="sxs-lookup"><span data-stu-id="b2dc3-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2dc3-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2dc3-126">Requirements</span></span>



| <span data-ttu-id="b2dc3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2dc3-127">Requirement</span></span> | <span data-ttu-id="b2dc3-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b2dc3-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2dc3-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2dc3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2dc3-130">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b2dc3-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b2dc3-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2dc3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2dc3-132">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2dc3-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="b2dc3-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2dc3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2dc3-134"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2dc3-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2dc3-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2dc3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2dc3-136">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2dc3-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





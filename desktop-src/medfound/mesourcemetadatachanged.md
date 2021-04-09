---
description: Generato da un'origine multimediale durante l'aggiornamento dei relativi metadati.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966804"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="3c246-103">Evento MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="3c246-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="3c246-104">Generato da un'origine multimediale durante l'aggiornamento dei relativi metadati.</span><span class="sxs-lookup"><span data-stu-id="3c246-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="3c246-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="3c246-105">Event values</span></span>

<span data-ttu-id="3c246-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c246-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3c246-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3c246-107">VARTYPE</span></span>              | <span data-ttu-id="3c246-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c246-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3c246-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="3c246-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3c246-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3c246-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3c246-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c246-111">Remarks</span></span>

<span data-ttu-id="3c246-112">Se l'origine del supporto non può fornire tutti i metadati quando l'origine viene creata per la prima volta, deve generare questo evento dopo che i metadati sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="3c246-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="3c246-113">L'origine multimediale deve creare un nuovo descrittore di presentazione e copiare tutti gli attributi dal descrittore della presentazione (PD) nell'oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="3c246-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="3c246-114">L'applicazione può usare l'oggetto evento per enumerare i nuovi attributi PD.</span><span class="sxs-lookup"><span data-stu-id="3c246-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="3c246-115">In particolare, i valori per le [ \_ \_ \_ \_ dimensioni del file](mf-pd-total-file-size-attribute.md) [MF \_ PD \_ Duration](mf-pd-duration-attribute.md) e MF PD possono essere sconosciuti fino a quando il file non viene scaricato completamente.</span><span class="sxs-lookup"><span data-stu-id="3c246-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c246-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c246-116">Requirements</span></span>



| <span data-ttu-id="3c246-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c246-117">Requirement</span></span> | <span data-ttu-id="3c246-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3c246-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c246-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c246-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c246-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c246-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c246-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c246-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c246-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c246-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c246-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c246-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c246-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c246-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c246-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c246-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c246-126">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3c246-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3c246-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="3c246-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





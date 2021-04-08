---
description: Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Evento MEStreamFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880246"
---
# <a name="mestreamformatchanged-event"></a><span data-ttu-id="5a8be-103">Evento MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="5a8be-103">MEStreamFormatChanged event</span></span>

<span data-ttu-id="5a8be-104">Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.</span><span class="sxs-lookup"><span data-stu-id="5a8be-104">Raised by a media stream when the media type of the stream changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="5a8be-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="5a8be-105">Event values</span></span>

<span data-ttu-id="5a8be-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a8be-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5a8be-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5a8be-107">VARTYPE</span></span>                | <span data-ttu-id="5a8be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a8be-108">Description</span></span>                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8be-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="5a8be-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="5a8be-110">Puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="5a8be-110">Pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the new media type.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5a8be-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a8be-111">Remarks</span></span>

<span data-ttu-id="5a8be-112">Utilizzare questo evento per segnalare le modifiche al formato nel flusso.</span><span class="sxs-lookup"><span data-stu-id="5a8be-112">Use this event to signal format changes in the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a8be-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a8be-113">Requirements</span></span>



| <span data-ttu-id="5a8be-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a8be-114">Requirement</span></span> | <span data-ttu-id="5a8be-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5a8be-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8be-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a8be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8be-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a8be-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a8be-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a8be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8be-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a8be-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a8be-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a8be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a8be-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a8be-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a8be-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a8be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8be-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a8be-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





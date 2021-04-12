---
description: Segnala che un'origine multimediale ha completato un tentativo di riconnessione al server.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Evento MEReconnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528267"
---
# <a name="mereconnectend-event"></a><span data-ttu-id="d98bc-103">Evento MEReconnectEnd</span><span class="sxs-lookup"><span data-stu-id="d98bc-103">MEReconnectEnd event</span></span>

<span data-ttu-id="d98bc-104">Segnala che un'origine multimediale ha completato un tentativo di riconnessione al server.</span><span class="sxs-lookup"><span data-stu-id="d98bc-104">Signals that a media source has completed an attempt to reconnect to the server.</span></span>

<span data-ttu-id="d98bc-105">Generato da un'origine multimediale al termine di un tentativo di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="d98bc-105">Raised by a media source at the end of a reconnection attempt.</span></span> <span data-ttu-id="d98bc-106">L'origine di rete genera questo evento se si riconnette al server.</span><span class="sxs-lookup"><span data-stu-id="d98bc-106">The network source raises this event if it reconnects to the server.</span></span> <span data-ttu-id="d98bc-107">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d98bc-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="d98bc-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="d98bc-108">Event values</span></span>

<span data-ttu-id="d98bc-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="d98bc-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d98bc-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d98bc-110">VARTYPE</span></span>              | <span data-ttu-id="d98bc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d98bc-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d98bc-112">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="d98bc-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d98bc-113">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d98bc-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d98bc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d98bc-114">Requirements</span></span>



| <span data-ttu-id="d98bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98bc-115">Requirement</span></span> | <span data-ttu-id="d98bc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d98bc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98bc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d98bc-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d98bc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d98bc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d98bc-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d98bc-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d98bc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d98bc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d98bc-122"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d98bc-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98bc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d98bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98bc-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d98bc-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





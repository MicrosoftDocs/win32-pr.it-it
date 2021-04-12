---
description: Segnala che è in corso un tentativo di riconnessione di un'origine multimediale al server.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Evento MEReconnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130742"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="d16c3-103">Evento MEReconnectStart</span><span class="sxs-lookup"><span data-stu-id="d16c3-103">MEReconnectStart event</span></span>

<span data-ttu-id="d16c3-104">Segnala che è in corso un tentativo di riconnessione di un'origine multimediale al server.</span><span class="sxs-lookup"><span data-stu-id="d16c3-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="d16c3-105">Generato da un'origine multimediale all'inizio di un tentativo di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="d16c3-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="d16c3-106">L'origine di rete genera questo evento se tenta di riconnettersi al server.</span><span class="sxs-lookup"><span data-stu-id="d16c3-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="d16c3-107">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d16c3-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="d16c3-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="d16c3-108">Event values</span></span>

<span data-ttu-id="d16c3-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="d16c3-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d16c3-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d16c3-110">VARTYPE</span></span>              | <span data-ttu-id="d16c3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d16c3-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d16c3-112">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="d16c3-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d16c3-113">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d16c3-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d16c3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d16c3-114">Requirements</span></span>



| <span data-ttu-id="d16c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d16c3-115">Requirement</span></span> | <span data-ttu-id="d16c3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d16c3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d16c3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d16c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d16c3-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d16c3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d16c3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d16c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d16c3-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d16c3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d16c3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d16c3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d16c3-122"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d16c3-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d16c3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d16c3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16c3-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d16c3-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





---
description: Generato dalla sessione multimediale al termine della riproduzione dell'ultima presentazione nella coda di riproduzione.
ms.assetid: e593e51f-c239-49e9-bba8-c6d8238eff24
title: Evento MESessionEnded (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447b222be48dccc0f190329ab0bb6d56d09b266e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309615"
---
# <a name="mesessionended-event"></a><span data-ttu-id="b7a58-103">Evento MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="b7a58-103">MESessionEnded event</span></span>

<span data-ttu-id="b7a58-104">Generato dalla sessione multimediale al termine della riproduzione dell'ultima presentazione nella coda di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b7a58-104">Raised by the Media Session when it has finished playing the last presentation in the playback queue.</span></span>

## <a name="event-values"></a><span data-ttu-id="b7a58-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="b7a58-105">Event values</span></span>

<span data-ttu-id="b7a58-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7a58-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b7a58-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b7a58-107">VARTYPE</span></span>              | <span data-ttu-id="b7a58-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7a58-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b7a58-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="b7a58-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b7a58-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b7a58-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b7a58-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7a58-111">Requirements</span></span>



| <span data-ttu-id="b7a58-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7a58-112">Requirement</span></span> | <span data-ttu-id="b7a58-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b7a58-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7a58-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7a58-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b7a58-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7a58-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7a58-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7a58-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b7a58-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7a58-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7a58-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7a58-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7a58-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7a58-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7a58-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7a58-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7a58-121">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7a58-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





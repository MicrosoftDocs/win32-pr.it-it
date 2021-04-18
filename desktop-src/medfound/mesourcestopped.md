---
description: "Generato da un'origine multimediale quando il metodo IMFMediaSource:: Stop viene completato in modo asincrono."
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: Evento MESourceStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307997"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="1cad4-103">Evento MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="1cad4-103">MESourceStopped event</span></span>

<span data-ttu-id="1cad4-104">Generato da un'origine multimediale quando il metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="1cad4-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="1cad4-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="1cad4-105">Event values</span></span>

<span data-ttu-id="1cad4-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1cad4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1cad4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1cad4-107">VARTYPE</span></span>              | <span data-ttu-id="1cad4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cad4-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="1cad4-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="1cad4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="1cad4-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1cad4-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1cad4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cad4-111">Requirements</span></span>



| <span data-ttu-id="1cad4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cad4-112">Requirement</span></span> | <span data-ttu-id="1cad4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1cad4-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cad4-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cad4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1cad4-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1cad4-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1cad4-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cad4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1cad4-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1cad4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1cad4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cad4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cad4-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cad4-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cad4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cad4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cad4-121">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1cad4-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





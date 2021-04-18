---
description: Generato dall'origine di rete al termine dell'apertura di un URL.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Evento MEConnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308472"
---
# <a name="meconnectend-event"></a><span data-ttu-id="8aec8-103">Evento MEConnectEnd</span><span class="sxs-lookup"><span data-stu-id="8aec8-103">MEConnectEnd event</span></span>

<span data-ttu-id="8aec8-104">Generato dall'origine di rete al termine dell'apertura di un URL.</span><span class="sxs-lookup"><span data-stu-id="8aec8-104">Raised by the network source when it finishes opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="8aec8-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="8aec8-105">Event values</span></span>

<span data-ttu-id="8aec8-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="8aec8-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8aec8-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8aec8-107">VARTYPE</span></span>              | <span data-ttu-id="8aec8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aec8-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="8aec8-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="8aec8-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="8aec8-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="8aec8-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8aec8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aec8-111">Remarks</span></span>

<span data-ttu-id="8aec8-112">L'origine di rete invia questo evento direttamente all'applicazione tramite il metodo [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) dell'applicazione, non tramite la consueta interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="8aec8-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aec8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8aec8-113">Requirements</span></span>



| <span data-ttu-id="8aec8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aec8-114">Requirement</span></span> | <span data-ttu-id="8aec8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8aec8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aec8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aec8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8aec8-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8aec8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8aec8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aec8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8aec8-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8aec8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8aec8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8aec8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aec8-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8aec8-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aec8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8aec8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aec8-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="8aec8-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="8aec8-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8aec8-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





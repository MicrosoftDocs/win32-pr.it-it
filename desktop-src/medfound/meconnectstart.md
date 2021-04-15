---
description: Generato dall'origine di rete quando inizia ad aprire un URL.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Evento MEConnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8e45d723a62854c34ba7b297e462d03fed97a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527432"
---
# <a name="meconnectstart-event"></a><span data-ttu-id="bde8e-103">Evento MEConnectStart</span><span class="sxs-lookup"><span data-stu-id="bde8e-103">MEConnectStart event</span></span>

<span data-ttu-id="bde8e-104">Generato dall'origine di rete quando inizia ad aprire un URL.</span><span class="sxs-lookup"><span data-stu-id="bde8e-104">Raised by the network source when it starts opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="bde8e-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="bde8e-105">Event values</span></span>

<span data-ttu-id="bde8e-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="bde8e-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bde8e-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bde8e-107">VARTYPE</span></span>              | <span data-ttu-id="bde8e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bde8e-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="bde8e-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="bde8e-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bde8e-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bde8e-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bde8e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bde8e-111">Remarks</span></span>

<span data-ttu-id="bde8e-112">L'origine di rete invia questo evento direttamente all'applicazione tramite il metodo [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) dell'applicazione, non tramite la consueta interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="bde8e-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde8e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bde8e-113">Requirements</span></span>



| <span data-ttu-id="bde8e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde8e-114">Requirement</span></span> | <span data-ttu-id="bde8e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bde8e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde8e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bde8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bde8e-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bde8e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bde8e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bde8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bde8e-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bde8e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bde8e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bde8e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde8e-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bde8e-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde8e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bde8e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde8e-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="bde8e-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="bde8e-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bde8e-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





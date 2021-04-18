---
description: Lo stato del grafico filtro è stato modificato.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327429"
---
# <a name="ec_state_change"></a><span data-ttu-id="8483a-103">\_modifica dello stato EC \_</span><span class="sxs-lookup"><span data-stu-id="8483a-103">EC\_STATE\_CHANGE</span></span>

<span data-ttu-id="8483a-104">Lo stato del grafico filtro è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8483a-104">The filter graph has changed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="8483a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8483a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8483a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8483a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8483a-107">(**DWORD**) Membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica il nuovo stato del grafico.</span><span class="sxs-lookup"><span data-stu-id="8483a-107">(**DWORD**) Member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the new graph state.</span></span>

</dd> <dt>

<span data-ttu-id="8483a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8483a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8483a-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="8483a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="8483a-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="8483a-110">Default Action</span></span>

<span data-ttu-id="8483a-111">Nessuna azione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8483a-111">No default action.</span></span> <span data-ttu-id="8483a-112">L'evento non viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8483a-112">The event is not sent to the application.</span></span>

> [!Note]  
> <span data-ttu-id="8483a-113">Questo evento può verificarsi quando il grafico si arresta.</span><span class="sxs-lookup"><span data-stu-id="8483a-113">This event can occur when the graph shuts down.</span></span> <span data-ttu-id="8483a-114">Se si sostituisce l'azione predefinita e si è in ascolto di questo evento, è necessario prestare particolare attenzione a non elaborare gli eventi dopo aver rilasciato il gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="8483a-114">If you override the default action and listen for this event, you must be especially careful not to process events after releasing the Filter Graph Manager.</span></span> <span data-ttu-id="8483a-115">In caso contrario, l'applicazione potrebbe fare riferimento a un puntatore [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) non valido e un arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="8483a-115">Otherwise, your application might reference an invalid [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) pointer and crash.</span></span> <span data-ttu-id="8483a-116">Per altre informazioni, vedere [rispondere agli eventi](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="8483a-116">For more information, see [Responding to Events](responding-to-events.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8483a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8483a-117">Requirements</span></span>



| <span data-ttu-id="8483a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8483a-118">Requirement</span></span> | <span data-ttu-id="8483a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8483a-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8483a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8483a-120">Header</span></span><br/> | <dl> <span data-ttu-id="8483a-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="8483a-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8483a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8483a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8483a-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="8483a-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8483a-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8483a-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





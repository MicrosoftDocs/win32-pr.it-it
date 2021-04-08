---
title: Messaggio di WM_CAP_SET_PREVIEWRATE (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ PREVIEWRATE imposta la frequenza di visualizzazione dei frame in modalità anteprima. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964886"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="8c43a-105">\_ \_ Messaggio PREVIEWRATE set di estremità WM \_</span><span class="sxs-lookup"><span data-stu-id="8c43a-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="8c43a-106">Il messaggio **WM \_ Cap \_ set \_ PREVIEWRATE** imposta la frequenza di visualizzazione dei frame in modalità anteprima.</span><span class="sxs-lookup"><span data-stu-id="8c43a-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="8c43a-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .</span><span class="sxs-lookup"><span data-stu-id="8c43a-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="8c43a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c43a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c43a-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span><span class="sxs-lookup"><span data-stu-id="8c43a-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="8c43a-110">Frequenza, in millisecondi, in base alla quale vengono acquisiti e visualizzati nuovi frame.</span><span class="sxs-lookup"><span data-stu-id="8c43a-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c43a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c43a-111">Return Value</span></span>

<span data-ttu-id="8c43a-112">Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="8c43a-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c43a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c43a-113">Remarks</span></span>

<span data-ttu-id="8c43a-114">La modalità di anteprima usa risorse di CPU sostanziali.</span><span class="sxs-lookup"><span data-stu-id="8c43a-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="8c43a-115">Le applicazioni possono disabilitare l'anteprima o abbassare la frequenza di anteprima quando un'altra applicazione ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="8c43a-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="8c43a-116">Durante lo streaming di acquisizione video, l'attività di anteprima è più bassa rispetto alla scrittura di frame su disco e i frame di anteprima vengono visualizzati solo se non sono disponibili altri buffer per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="8c43a-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c43a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c43a-117">Requirements</span></span>



| <span data-ttu-id="8c43a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c43a-118">Requirement</span></span> | <span data-ttu-id="8c43a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8c43a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8c43a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c43a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c43a-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8c43a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8c43a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c43a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c43a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8c43a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8c43a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c43a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c43a-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c43a-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c43a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c43a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c43a-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="8c43a-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8c43a-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="8c43a-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






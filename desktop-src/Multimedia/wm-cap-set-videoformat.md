---
title: Messaggio di WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ VIDEOFORMAT imposta il formato dei dati video acquisiti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964885"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="b3cdc-105">\_ \_ Messaggio VIDEOFORMAT set di estremità WM \_</span><span class="sxs-lookup"><span data-stu-id="b3cdc-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="b3cdc-106">Il messaggio **WM \_ Cap \_ set \_ VIDEOFORMAT** imposta il formato dei dati video acquisiti.</span><span class="sxs-lookup"><span data-stu-id="b3cdc-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="b3cdc-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="b3cdc-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="b3cdc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3cdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3cdc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="b3cdc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="b3cdc-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="b3cdc-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="b3cdc-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="b3cdc-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="b3cdc-112">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="b3cdc-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3cdc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3cdc-113">Return Value</span></span>

<span data-ttu-id="b3cdc-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b3cdc-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cdc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3cdc-115">Remarks</span></span>

<span data-ttu-id="b3cdc-116">Poiché i formati video sono specifici del dispositivo, le applicazioni devono controllare il valore restituito da questa funzione per determinare se il formato è accettato dal driver.</span><span class="sxs-lookup"><span data-stu-id="b3cdc-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3cdc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3cdc-117">Requirements</span></span>



| <span data-ttu-id="b3cdc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cdc-118">Requirement</span></span> | <span data-ttu-id="b3cdc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b3cdc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3cdc-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cdc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cdc-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3cdc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3cdc-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cdc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cdc-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3cdc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b3cdc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3cdc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3cdc-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3cdc-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3cdc-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3cdc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3cdc-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="b3cdc-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b3cdc-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="b3cdc-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 


---
title: Messaggio di WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ Sequence \_ Setup recupera le impostazioni correnti dei parametri di acquisizione del flusso. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963737"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="e9cc3-105">\_Messaggio di \_ \_ installazione sequenza \_ WM Cap Get</span><span class="sxs-lookup"><span data-stu-id="e9cc3-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="e9cc3-106">Il messaggio **WM \_ Cap \_ get \_ Sequence \_ Setup** recupera le impostazioni correnti dei parametri di acquisizione del flusso.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="e9cc3-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .</span><span class="sxs-lookup"><span data-stu-id="e9cc3-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="e9cc3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9cc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cc3-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="e9cc3-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e9cc3-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="e9cc3-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="e9cc3-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="e9cc3-112">Puntatore a una struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="e9cc3-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cc3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9cc3-113">Return Value</span></span>

<span data-ttu-id="e9cc3-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9cc3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9cc3-115">Remarks</span></span>

<span data-ttu-id="e9cc3-116">Per informazioni sui parametri usati per controllare l'acquisizione di flussi, vedere la struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="e9cc3-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9cc3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9cc3-117">Requirements</span></span>



| <span data-ttu-id="e9cc3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9cc3-118">Requirement</span></span> | <span data-ttu-id="e9cc3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e9cc3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e9cc3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9cc3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cc3-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9cc3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e9cc3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9cc3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cc3-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9cc3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e9cc3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9cc3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9cc3-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9cc3-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cc3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9cc3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cc3-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e9cc3-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e9cc3-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e9cc3-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






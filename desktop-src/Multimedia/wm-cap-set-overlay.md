---
title: Messaggio di WM_CAP_SET_OVERLAY (VFW. h)
description: Il \_ messaggio overlay del set di estremità WM \_ \_ Abilita o Disabilita la modalità overlay. In modalità sovrapposizione, il video viene visualizzato con la sovrimpressione hardware. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302582"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="0f534-106">\_ \_ \_ Messaggio sovrimpressione set Cap WM</span><span class="sxs-lookup"><span data-stu-id="0f534-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="0f534-107">Il **messaggio \_ \_ \_ overlay del set di estremità WM** Abilita o Disabilita la modalità overlay.</span><span class="sxs-lookup"><span data-stu-id="0f534-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="0f534-108">In modalità sovrapposizione, il video viene visualizzato con la sovrimpressione hardware.</span><span class="sxs-lookup"><span data-stu-id="0f534-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="0f534-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .</span><span class="sxs-lookup"><span data-stu-id="0f534-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="0f534-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f534-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f534-111"><span id="f"></span><span id="F"></span>*f*</span><span class="sxs-lookup"><span data-stu-id="0f534-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="0f534-112">Flag di sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="0f534-112">Overlay flag.</span></span> <span data-ttu-id="0f534-113">Specificare **true** per questo parametro per abilitare la modalità overlay o **false** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="0f534-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f534-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f534-114">Return Value</span></span>

<span data-ttu-id="0f534-115">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0f534-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f534-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f534-116">Remarks</span></span>

<span data-ttu-id="0f534-117">L'uso di una sovrapposizione non richiede risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="0f534-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="0f534-118">Il membro **fHasOverlay** della struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica se il dispositivo è in grado di sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="0f534-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="0f534-119">Il membro **fOverlayWindow** della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se la modalità overlay è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="0f534-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="0f534-120">L'abilitazione della modalità sovrapposizione Disabilita automaticamente la modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="0f534-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f534-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f534-121">Requirements</span></span>



| <span data-ttu-id="0f534-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f534-122">Requirement</span></span> | <span data-ttu-id="0f534-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0f534-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f534-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f534-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0f534-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f534-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0f534-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f534-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0f534-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f534-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f534-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f534-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f534-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f534-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f534-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f534-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f534-131">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0f534-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0f534-132">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0f534-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






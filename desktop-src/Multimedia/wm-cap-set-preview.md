---
title: Messaggio di WM_CAP_SET_PREVIEW (VFW. h)
description: Il messaggio di anteprima di WM \_ Cap \_ set \_ Abilita o Disabilita la modalità di anteprima.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121394"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="d8b5e-104">\_Messaggio di \_ \_ Anteprima set di WM Cap</span><span class="sxs-lookup"><span data-stu-id="d8b5e-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="d8b5e-105">Il messaggio di **Anteprima di WM \_ Cap \_ set \_** Abilita o Disabilita la modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="d8b5e-106">In modalità di anteprima, i frame vengono trasferiti dall'hardware di acquisizione alla memoria di sistema e quindi visualizzati nella finestra di acquisizione utilizzando le funzioni GDI.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="d8b5e-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .</span><span class="sxs-lookup"><span data-stu-id="d8b5e-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="d8b5e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8b5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b5e-109"><span id="f"></span><span id="F"></span>*f*</span><span class="sxs-lookup"><span data-stu-id="d8b5e-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="d8b5e-110">Flag di anteprima.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-110">Preview flag.</span></span> <span data-ttu-id="d8b5e-111">Specificare **true** per questo parametro per abilitare la modalità di anteprima o **false** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b5e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8b5e-112">Return Value</span></span>

<span data-ttu-id="d8b5e-113">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b5e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8b5e-114">Remarks</span></span>

<span data-ttu-id="d8b5e-115">La modalità di anteprima usa risorse di CPU sostanziali.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="d8b5e-116">Le applicazioni possono disabilitare l'anteprima o abbassare la frequenza di anteprima quando un'altra applicazione ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="d8b5e-117">Il membro **fLiveWindow** della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se la modalità di anteprima è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="d8b5e-118">L'abilitazione della modalità di anteprima Disabilita automaticamente la modalità overlay.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b5e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8b5e-119">Requirements</span></span>



| <span data-ttu-id="d8b5e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b5e-120">Requirement</span></span> | <span data-ttu-id="d8b5e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d8b5e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8b5e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8b5e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b5e-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8b5e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8b5e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8b5e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b5e-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8b5e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8b5e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8b5e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b5e-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b5e-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b5e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8b5e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b5e-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8b5e-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d8b5e-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8b5e-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






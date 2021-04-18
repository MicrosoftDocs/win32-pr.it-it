---
title: Messaggio di WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ frame imposta una funzione di callback di anteprima nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione acquisisce i frame di anteprima. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301815"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="0451e-106">Messaggio del frame di callback di WM \_ Cap \_ set \_ \_</span><span class="sxs-lookup"><span data-stu-id="0451e-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="0451e-107">Il messaggio **WM \_ Cap \_ set \_ callback \_ frame** imposta una funzione di callback di anteprima nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0451e-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="0451e-108">AVICap chiama questa procedura quando la finestra di acquisizione acquisisce i frame di anteprima.</span><span class="sxs-lookup"><span data-stu-id="0451e-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="0451e-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="0451e-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="0451e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0451e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0451e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="0451e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="0451e-112">Puntatore alla funzione di callback di anteprima, di tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="0451e-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="0451e-113">Specificare **null** per questo parametro per disabilitare una funzione di callback installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0451e-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0451e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0451e-114">Return Value</span></span>

<span data-ttu-id="0451e-115">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.</span><span class="sxs-lookup"><span data-stu-id="0451e-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="0451e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0451e-116">Remarks</span></span>

<span data-ttu-id="0451e-117">La finestra di acquisizione chiama la funzione di callback prima di visualizzare i frame di anteprima.</span><span class="sxs-lookup"><span data-stu-id="0451e-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="0451e-118">Questo consente a un'applicazione di modificare il frame se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="0451e-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="0451e-119">Questa funzione di callback non viene usata durante l'acquisizione video di streaming.</span><span class="sxs-lookup"><span data-stu-id="0451e-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0451e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0451e-120">Requirements</span></span>



| <span data-ttu-id="0451e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0451e-121">Requirement</span></span> | <span data-ttu-id="0451e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0451e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0451e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0451e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0451e-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0451e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0451e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0451e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0451e-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0451e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0451e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0451e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0451e-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0451e-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0451e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0451e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0451e-130">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0451e-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0451e-131">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0451e-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






---
title: Messaggio di WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ WAVESTREAM imposta una funzione di callback nell'applicazione.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479055"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="f6aac-104">\_ \_ \_ Messaggio WAVESTREAM di richiamata di WM Cap Set \_</span><span class="sxs-lookup"><span data-stu-id="f6aac-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="f6aac-105">Il messaggio **WM \_ Cap \_ set \_ callback \_ WAVESTREAM** imposta una funzione di callback nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6aac-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="f6aac-106">AVICap chiama questa procedura durante l'acquisizione del flusso quando diventa disponibile un nuovo buffer audio.</span><span class="sxs-lookup"><span data-stu-id="f6aac-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="f6aac-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .</span><span class="sxs-lookup"><span data-stu-id="f6aac-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="f6aac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6aac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6aac-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="f6aac-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="f6aac-110">Puntatore alla funzione di callback del flusso Wave, di tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span><span class="sxs-lookup"><span data-stu-id="f6aac-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="f6aac-111">Specificare **null** per questo parametro per disabilitare una funzione di callback del flusso Wave installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f6aac-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6aac-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6aac-112">Return Value</span></span>

<span data-ttu-id="f6aac-113">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.</span><span class="sxs-lookup"><span data-stu-id="f6aac-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6aac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6aac-114">Remarks</span></span>

<span data-ttu-id="f6aac-115">La finestra di acquisizione chiama la procedura prima di scrivere il buffer audio su disco.</span><span class="sxs-lookup"><span data-stu-id="f6aac-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="f6aac-116">Ciò consente alle applicazioni di modificare il buffer audio se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="f6aac-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="f6aac-117">Se viene usata una funzione di callback del flusso Wave, è necessario installarla prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione.</span><span class="sxs-lookup"><span data-stu-id="f6aac-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="f6aac-118">Può essere disabilitato al termine dell'acquisizione di streaming.</span><span class="sxs-lookup"><span data-stu-id="f6aac-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6aac-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6aac-119">Requirements</span></span>



| <span data-ttu-id="f6aac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6aac-120">Requirement</span></span> | <span data-ttu-id="f6aac-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f6aac-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f6aac-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6aac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6aac-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6aac-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f6aac-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6aac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6aac-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6aac-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f6aac-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6aac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6aac-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6aac-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6aac-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6aac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6aac-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f6aac-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f6aac-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f6aac-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






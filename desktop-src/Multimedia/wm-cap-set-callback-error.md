---
title: Messaggio di WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: Il \_ \_ \_ messaggio di errore del set di richiamata di WM Cap \_ imposta una funzione di callback di errore nell'applicazione client. AVICap chiama questa procedura quando si verificano errori. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477248"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="c371e-106">\_Messaggio di \_ errore di callback del set di estremità WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="c371e-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="c371e-107">Il messaggio di **\_ errore del set di \_ \_ richiamata \_ di WM Cap** imposta una funzione di callback di errore nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="c371e-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="c371e-108">AVICap chiama questa procedura quando si verificano errori.</span><span class="sxs-lookup"><span data-stu-id="c371e-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="c371e-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="c371e-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="c371e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c371e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c371e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="c371e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="c371e-112">Puntatore alla funzione di callback di errore, di tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span><span class="sxs-lookup"><span data-stu-id="c371e-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="c371e-113">Specificare **null** per questo parametro per disabilitare una funzione di callback degli errori installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c371e-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c371e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c371e-114">Return Value</span></span>

<span data-ttu-id="c371e-115">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.</span><span class="sxs-lookup"><span data-stu-id="c371e-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="c371e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c371e-116">Remarks</span></span>

<span data-ttu-id="c371e-117">Le applicazioni possono facoltativamente impostare una funzione di callback degli errori.</span><span class="sxs-lookup"><span data-stu-id="c371e-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="c371e-118">Se impostata, AVICap chiama la procedura di errore nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c371e-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="c371e-119">Disco pieno.</span><span class="sxs-lookup"><span data-stu-id="c371e-119">The disk is full.</span></span>
-   <span data-ttu-id="c371e-120">Una finestra di acquisizione non può essere connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c371e-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="c371e-121">Non è possibile aprire un dispositivo audio waveform.</span><span class="sxs-lookup"><span data-stu-id="c371e-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="c371e-122">Il numero di frame eliminati durante l'acquisizione supera la percentuale specificata.</span><span class="sxs-lookup"><span data-stu-id="c371e-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="c371e-123">Impossibile acquisire i frame a causa di problemi di interrupt della sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="c371e-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="c371e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c371e-124">Requirements</span></span>



| <span data-ttu-id="c371e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c371e-125">Requirement</span></span> | <span data-ttu-id="c371e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c371e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c371e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c371e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c371e-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c371e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c371e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c371e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c371e-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c371e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c371e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c371e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c371e-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c371e-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c371e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c371e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c371e-134">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c371e-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c371e-135">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c371e-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






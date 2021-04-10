---
title: Comando MCI_DELETE (mmsystem. h)
description: Il \_ comando MCI Delete rimuove i dati dal file. Digital-video e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- Comando MCI_DELETE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964529"
---
# <a name="mci_delete-command"></a><span data-ttu-id="90fc6-105">\_Comando MCI Delete</span><span class="sxs-lookup"><span data-stu-id="90fc6-105">MCI\_DELETE command</span></span>

<span data-ttu-id="90fc6-106">Il \_ comando MCI Delete rimuove i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="90fc6-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="90fc6-107">Digital-video e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="90fc6-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="90fc6-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="90fc6-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="90fc6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="90fc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90fc6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="90fc6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="90fc6-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="90fc6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi video digitali, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="90fc6-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="90fc6-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="90fc6-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span><span class="sxs-lookup"><span data-stu-id="90fc6-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="90fc6-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="90fc6-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90fc6-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90fc6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90fc6-118">Return Value</span></span>

<span data-ttu-id="90fc6-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="90fc6-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="90fc6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="90fc6-120">Remarks</span></span>

<span data-ttu-id="90fc6-121">I flag seguenti si applicano al tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="90fc6-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="90fc6-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>\_DGV \_ di MCI Delete \_</span><span class="sxs-lookup"><span data-stu-id="90fc6-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-123">Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-124">Il rettangolo specifica la parte di ogni fotogramma da eliminare.</span><span class="sxs-lookup"><span data-stu-id="90fc6-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="90fc6-125">Quando si usa questo flag, il frame viene mantenuto nell'area di lavoro e l'area specificata dal rettangolo diventa nera.</span><span class="sxs-lookup"><span data-stu-id="90fc6-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="90fc6-126">Se il flag viene omesso, MCI \_ Delete viene impostato sull'intero frame e il frame viene rimosso dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="90fc6-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>\_ \_ flusso audio di eliminazione DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="90fc6-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-128">Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-129">Se si usa questo flag e si vuole anche eliminare il video, è necessario usare anche il \_ \_ flag DGV Delete \_ video \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="90fc6-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="90fc6-130">Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="90fc6-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_ \_ \_ flusso video DGV Delete \_ MCI</span><span class="sxs-lookup"><span data-stu-id="90fc6-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-132">Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-133">Se si utilizza questo flag e si desidera eliminare anche l'audio, è necessario utilizzare anche il \_ \_ flag del \_ flusso audio DGV Delete MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="90fc6-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="90fc6-134">Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="90fc6-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="90fc6-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-136">Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-137">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="90fc6-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-138"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="90fc6-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-139">Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-140">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="90fc6-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="90fc6-141">Per i dispositivi digitali video, il parametro *lpDelete* punta a una [**struttura \_ DGV \_ Delete \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .</span><span class="sxs-lookup"><span data-stu-id="90fc6-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="90fc6-142">I flag seguenti si applicano al tipo di dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="90fc6-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="90fc6-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="90fc6-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-144">Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-145">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del [ \_ set di MCI](mci-set.md).</span><span class="sxs-lookup"><span data-stu-id="90fc6-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="90fc6-146"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="90fc6-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="90fc6-147">Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="90fc6-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="90fc6-148">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="90fc6-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="90fc6-149">Per i dispositivi Waveform-Audio, il parametro *lpDelete* punta a una struttura [**\_ \_ \_ parametri Wave Delete MCI**](mci-wave-delete-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="90fc6-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="90fc6-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90fc6-150">Requirements</span></span>



| <span data-ttu-id="90fc6-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="90fc6-151">Requirement</span></span> | <span data-ttu-id="90fc6-152">Valore</span><span class="sxs-lookup"><span data-stu-id="90fc6-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90fc6-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90fc6-153">Minimum supported client</span></span><br/> | <span data-ttu-id="90fc6-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90fc6-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="90fc6-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90fc6-155">Minimum supported server</span></span><br/> | <span data-ttu-id="90fc6-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90fc6-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90fc6-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90fc6-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="90fc6-158"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90fc6-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90fc6-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90fc6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90fc6-160">MCI</span><span class="sxs-lookup"><span data-stu-id="90fc6-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="90fc6-161">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="90fc6-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


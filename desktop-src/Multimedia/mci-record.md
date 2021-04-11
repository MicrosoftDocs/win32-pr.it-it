---
title: Comando MCI_RECORD (mmsystem. h)
description: Il \_ comando MCI record avvia la registrazione dalla posizione corrente o da un percorso specificato a un altro percorso specificato.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Comando MCI_RECORD Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119991"
---
# <a name="mci_record-command"></a><span data-ttu-id="d83b1-104">\_Comando record MCI</span><span class="sxs-lookup"><span data-stu-id="d83b1-104">MCI\_RECORD command</span></span>

<span data-ttu-id="d83b1-105">Il comando [**MCI \_ record**](mci-record-parms.md) avvia la registrazione dalla posizione corrente o da un percorso specificato a un altro percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="d83b1-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="d83b1-106">VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d83b1-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="d83b1-107">Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.</span><span class="sxs-lookup"><span data-stu-id="d83b1-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="d83b1-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="d83b1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="d83b1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d83b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d83b1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d83b1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="d83b1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d83b1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d83b1-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="d83b1-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d83b1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span><span class="sxs-lookup"><span data-stu-id="d83b1-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-116">Puntatore a una [**struttura \_ \_ parametri del record MCI**](mci-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="d83b1-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d83b1-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d83b1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d83b1-118">Return Value</span></span>

<span data-ttu-id="d83b1-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d83b1-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d83b1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d83b1-120">Remarks</span></span>

<span data-ttu-id="d83b1-121">Questo comando è supportato dai dispositivi che restituiscono **true** quando si chiama il comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con MCI \_ GETDEVCAPS \_ can \_ record flag.</span><span class="sxs-lookup"><span data-stu-id="d83b1-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="d83b1-122">Per il driver MCIWAVE, tutti i dati registrati dopo l'apertura di un file vengono eliminati se il file viene chiuso senza salvarlo.</span><span class="sxs-lookup"><span data-stu-id="d83b1-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="d83b1-123">I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano il \_ record MCI:</span><span class="sxs-lookup"><span data-stu-id="d83b1-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="d83b1-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="d83b1-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-125">Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="d83b1-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="d83b1-126">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="d83b1-127">Se MCI \_ from non è specificato, per impostazione predefinita la posizione iniziale viene impostata sulla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d83b1-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_inserimento record \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d83b1-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-129">Le informazioni appena registrate devono essere inserite o incollate nei dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="d83b1-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="d83b1-130">Alcuni dispositivi potrebbero non supportare questo problema.</span><span class="sxs-lookup"><span data-stu-id="d83b1-130">Some devices might not support this.</span></span> <span data-ttu-id="d83b1-131">Se supportato, si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d83b1-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>sovrascrittura del \_ record MCI \_</span><span class="sxs-lookup"><span data-stu-id="d83b1-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-133">I dati devono sovrascrivere i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="d83b1-133">Data should overwrite existing data.</span></span> <span data-ttu-id="d83b1-134">MCIWAVE. Il dispositivo DRV restituisce MCIERR \_ funzione non supportata \_ in risposta a questo flag.</span><span class="sxs-lookup"><span data-stu-id="d83b1-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-135"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="d83b1-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-136">Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="d83b1-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="d83b1-137">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="d83b1-138">Se MCI \_ to non è specificato, il percorso finale viene impostato sul valore predefinito alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="d83b1-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="d83b1-139">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d83b1-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d83b1-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_ \_ flusso audio del record DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d83b1-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-141">Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="d83b1-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="d83b1-142">Se si omette questo flag, i dati audio vengono registrati nel primo flusso fisico.</span><span class="sxs-lookup"><span data-stu-id="d83b1-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_ \_ attesa record DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d83b1-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-144">Quando la registrazione viene arrestata, la schermata conterrà l'ultima immagine e non riprende a visualizzare il video fino a quando non viene emesso un comando di [ \_ monitoraggio MCI](mci-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_ \_ flusso video di record DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d83b1-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-146">Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="d83b1-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="d83b1-147">Se si omette questo flag, i dati video vengono registrati nel primo flusso fisico.</span><span class="sxs-lookup"><span data-stu-id="d83b1-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>DGV di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="d83b1-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-149">Un rettangolo viene specificato nel membro **RC** della struttura identificata da *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="d83b1-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="d83b1-150">Il rettangolo specifica l'area dell'input esterno usato come origine per i pixel compressi e salvati.</span><span class="sxs-lookup"><span data-stu-id="d83b1-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="d83b1-151">Per impostazione predefinita, questo rettangolo è il rettangolo specificato (o predefinito) dal \_ flag DGV \_ put \_ video per il comando [MCI \_ put](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="d83b1-152">Quando viene impostato in modo diverso rispetto al rettangolo video, ciò che viene visualizzato non è quello registrato</span><span class="sxs-lookup"><span data-stu-id="d83b1-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="d83b1-153">Per i dispositivi digitali video, *lpRecord* punta a una struttura di [**\_ \_ \_ parametri del record DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="d83b1-154">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d83b1-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d83b1-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_record MCI \_ VCR \_ in</span><span class="sxs-lookup"><span data-stu-id="d83b1-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-156">Il membro **dwAt** della struttura identificata da *lpRecord* contiene un'ora di inizio dell'intero comando o se il dispositivo viene riavviato quando il dispositivo raggiunge la posizione dalla posizione specificata dal comando cue.</span><span class="sxs-lookup"><span data-stu-id="d83b1-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="d83b1-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_ \_ inizializzazione record VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="d83b1-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="d83b1-158">Cercare il dispositivo all'inizio del supporto, iniziare la registrazione del video e dell'audio vuoti e registrare il timecode, se possibile.</span><span class="sxs-lookup"><span data-stu-id="d83b1-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="d83b1-159">Per i dispositivi VCR, *lpRecord* punta a una struttura [**\_ \_ \_ parametri del record VCR MCI**](mci-vcr-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d83b1-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d83b1-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d83b1-160">Requirements</span></span>



| <span data-ttu-id="d83b1-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="d83b1-161">Requirement</span></span> | <span data-ttu-id="d83b1-162">Valore</span><span class="sxs-lookup"><span data-stu-id="d83b1-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d83b1-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d83b1-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d83b1-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d83b1-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d83b1-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d83b1-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d83b1-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d83b1-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d83b1-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d83b1-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="d83b1-168"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d83b1-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d83b1-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d83b1-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d83b1-170">MCI</span><span class="sxs-lookup"><span data-stu-id="d83b1-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d83b1-171">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="d83b1-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


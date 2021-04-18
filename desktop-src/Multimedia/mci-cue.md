---
title: Comando MCI_CUE (mmsystem. h)
description: Il \_ comando MCI Cue viene segnalato da un dispositivo in modo che la riproduzione o la registrazione inizi con un ritardo minimo. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- Comando MCI_CUE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302029"
---
# <a name="mci_cue-command"></a><span data-ttu-id="934f1-105">\_Comando MCI cue</span><span class="sxs-lookup"><span data-stu-id="934f1-105">MCI\_CUE command</span></span>

<span data-ttu-id="934f1-106">Il \_ comando MCI Cue viene segnalato da un dispositivo in modo che la riproduzione o la registrazione inizi con un ritardo minimo.</span><span class="sxs-lookup"><span data-stu-id="934f1-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="934f1-107">Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="934f1-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="934f1-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="934f1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="934f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="934f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="934f1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="934f1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="934f1-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="934f1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="934f1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="934f1-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="934f1-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="934f1-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="934f1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="934f1-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span><span class="sxs-lookup"><span data-stu-id="934f1-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="934f1-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="934f1-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="934f1-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="934f1-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="934f1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="934f1-118">Return Value</span></span>

<span data-ttu-id="934f1-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="934f1-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="934f1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="934f1-120">Remarks</span></span>

<span data-ttu-id="934f1-121">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="934f1-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="934f1-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_ \_ input cue DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="934f1-123">Un'istanza di video digitale dovrebbe prepararsi per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="934f1-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="934f1-124">Se l'applicazione non dispone di spazio su disco riservato, il dispositivo riserva lo spazio su disco usando i parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="934f1-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="934f1-125">L'applicazione può omettere questo flag se l'origine della presentazione corrente è già l'input esterno.</span><span class="sxs-lookup"><span data-stu-id="934f1-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="934f1-126">Questo flag non ha alcun effetto sulla selezione dell'origine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="934f1-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="934f1-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>\_DGV \_ cue \_ noshow MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="934f1-128">Un'istanza di video digitale dovrebbe prepararsi a riprodurre il frame specificato con il comando senza visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="934f1-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="934f1-129">Quando questo flag viene specificato, la visualizzazione continua a mostrare l'immagine nel buffer del frame anche se il frame corrispondente non è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="934f1-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="934f1-130">Se, ad esempio, il buffer del frame contiene l'immagine del frame 7, il dispositivo continua a visualizzare il frame 7 quando questo flag viene usato per posizionare il dispositivo in un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="934f1-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="934f1-131">Un comando cue successivo senza questo flag e senza il \_ flag MCI to Visualizza il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="934f1-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>\_output del \_ cue \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="934f1-133">Un'istanza di video digitale dovrebbe prepararsi per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="934f1-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="934f1-134">Se l'area di lavoro è sospesa, non viene eseguito alcun posizionamento.</span><span class="sxs-lookup"><span data-stu-id="934f1-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="934f1-135">Se l'area di lavoro viene arrestata, la posizione potrebbe cambiare in un'immagine del fotogramma chiave precedente.</span><span class="sxs-lookup"><span data-stu-id="934f1-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="934f1-136">L'applicazione può omettere questo flag se l'origine della presentazione corrente è già l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="934f1-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-137"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="934f1-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="934f1-138">Una posizione dell'area di lavoro è inclusa nel membro **dwTo** della struttura identificata da *lpCue*.</span><span class="sxs-lookup"><span data-stu-id="934f1-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="934f1-139">Le unità assegnate ai valori di posizione vengono specificate usando il \_ \_ \_ flag di formato dell'ora del set di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="934f1-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="934f1-140">Questa operazione equivale alla ricerca di una posizione, ad eccezione del fatto che il dispositivo viene sospeso dopo il comando.</span><span class="sxs-lookup"><span data-stu-id="934f1-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="934f1-141">Per i dispositivi **digitalvideo** , il parametro *lpCue* punta a una struttura [**\_ DGV \_ cue \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .</span><span class="sxs-lookup"><span data-stu-id="934f1-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="934f1-142">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="934f1-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="934f1-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="934f1-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="934f1-144">Il membro **dwFrom** della struttura a cui punta *lpCue* contiene la posizione iniziale specificata nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="934f1-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-145"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="934f1-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="934f1-146">Il membro **dwTo** della struttura a cui punta *lpCue* contiene la posizione finale (sospensione) specificata nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="934f1-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_input di \_ cue \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="934f1-148">Prepararsi per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="934f1-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_output di \_ cue \_ VCR per MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="934f1-150">Prepararsi per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="934f1-150">Prepare for playing.</span></span> <span data-ttu-id="934f1-151">Se non è stato specificato né l'output della cue VCR MCI \_ \_ né l' \_ \_ \_ \_ output di cue VCR, \_ \_ viene utilizzato l'output di cue VCR \_ per MCI.</span><span class="sxs-lookup"><span data-stu-id="934f1-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>preroll di \_ cue VCR di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="934f1-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="934f1-153">Cue il dispositivo alla posizione corrente o alla posizione **dwFrom** , meno la durata della preregistrazione.</span><span class="sxs-lookup"><span data-stu-id="934f1-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="934f1-154">Questo consentirà al dispositivo di prepararsi prima di entrare in modalità registrazione o riproduzione.</span><span class="sxs-lookup"><span data-stu-id="934f1-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>\_ \_ segnale \_ inverso del VCR MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="934f1-156">La direzione del comando Play o record successivo è inversa.</span><span class="sxs-lookup"><span data-stu-id="934f1-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="934f1-157">Quando si esegue il ripasso per la riproduzione usando il \_ comando MCI cue con il \_ contrassegno MCI VCR \_ cue \_ output, è possibile annullare \_ la cue MCI eseguendo il comando [MCI \_ Play](mci-play.md) con MCI \_ from, MCI \_ to o MCI \_ VCR \_ Play \_ Reverse.</span><span class="sxs-lookup"><span data-stu-id="934f1-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="934f1-158">Quando si esegue il ripasso per la registrazione tramite MCI \_ cue con il \_ contrassegno MCI VCR \_ cue \_ input flag, è possibile annullare \_ la cue MCI inviando il comando [MCI \_ record](mci-record.md) con MCI \_ from, MCI \_ to o MCI \_ VCR \_ record \_ Initialize.</span><span class="sxs-lookup"><span data-stu-id="934f1-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="934f1-159">Per i dispositivi **VCR** , il parametro *lpCue* punta a una struttura [**\_ \_ \_ parametri cue VCR di MCI**](mci-vcr-cue-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="934f1-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="934f1-160">Con il tipo di dispositivo **WaveAudio** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="934f1-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="934f1-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_input wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="934f1-162">Un dispositivo di input della forma d'onda-audio deve essere sottomesso A cue.</span><span class="sxs-lookup"><span data-stu-id="934f1-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="934f1-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_Output Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="934f1-164">Un dispositivo di output della forma d'onda-audio deve essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="934f1-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="934f1-165">Si tratta del flag predefinito se non è specificato alcun flag.</span><span class="sxs-lookup"><span data-stu-id="934f1-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="934f1-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="934f1-166">Requirements</span></span>



| <span data-ttu-id="934f1-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="934f1-167">Requirement</span></span> | <span data-ttu-id="934f1-168">Valore</span><span class="sxs-lookup"><span data-stu-id="934f1-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="934f1-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="934f1-169">Minimum supported client</span></span><br/> | <span data-ttu-id="934f1-170">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="934f1-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="934f1-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="934f1-171">Minimum supported server</span></span><br/> | <span data-ttu-id="934f1-172">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="934f1-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="934f1-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="934f1-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="934f1-174"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="934f1-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="934f1-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="934f1-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934f1-176">MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="934f1-177">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="934f1-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


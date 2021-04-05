---
title: Comando MCI_PLAY (mmsystem. h)
description: Il \_ comando MCI Play segnala al dispositivo di iniziare a trasmettere i dati di output. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Comando MCI_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874633"
---
# <a name="mci_play-command"></a><span data-ttu-id="d659a-105">\_Comando MCI Play</span><span class="sxs-lookup"><span data-stu-id="d659a-105">MCI\_PLAY command</span></span>

<span data-ttu-id="d659a-106">Il \_ comando MCI Play segnala al dispositivo di iniziare a trasmettere i dati di output.</span><span class="sxs-lookup"><span data-stu-id="d659a-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="d659a-107">CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d659a-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="d659a-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="d659a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="d659a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d659a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d659a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d659a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d659a-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="d659a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d659a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d659a-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d659a-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="d659a-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d659a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d659a-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span><span class="sxs-lookup"><span data-stu-id="d659a-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="d659a-116">Puntatore a una [**struttura \_ \_ parametri di MCI Play**](mci-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d659a-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="d659a-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d659a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d659a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d659a-118">Return Value</span></span>

<span data-ttu-id="d659a-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d659a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d659a-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d659a-120">Remarks</span></span>

<span data-ttu-id="d659a-121">I flag aggiuntivi seguenti si applicano a tutti i dispositivi che supportano MCI \_ Play:</span><span class="sxs-lookup"><span data-stu-id="d659a-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="d659a-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="d659a-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="d659a-123">Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="d659a-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="d659a-124">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="d659a-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="d659a-125">Se MCI \_ from non è specificato, per impostazione predefinita la posizione iniziale viene impostata sulla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d659a-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-126"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="d659a-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d659a-127">Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="d659a-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="d659a-128">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d659a-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="d659a-129">Se MCI \_ to non è specificato, il valore predefinito della posizione finale è la fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="d659a-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="d659a-130">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d659a-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d659a-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_ripetizione della \_ riproduzione \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="d659a-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="d659a-132">La riproduzione deve iniziare di nuovo all'inizio quando viene raggiunta la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="d659a-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>\_riesecuzione DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="d659a-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="d659a-134">La riproduzione deve essere eseguita in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="d659a-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>\_finestra di \_ riproduzione \_ MCIAVI MCI</span><span class="sxs-lookup"><span data-stu-id="d659a-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="d659a-136">La riproduzione deve essere eseguita nella finestra associata a un'istanza del dispositivo (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="d659a-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="d659a-137">Questo flag è specifico di MCIAVI. DRV.)</span><span class="sxs-lookup"><span data-stu-id="d659a-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="d659a-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>\_MCIAVI MCI \_ Play a \_ schermo intero</span><span class="sxs-lookup"><span data-stu-id="d659a-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="d659a-139">La riproduzione deve usare una visualizzazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="d659a-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="d659a-140">Utilizzare questo flag solo per la riproduzione di file compressi o a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="d659a-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="d659a-141">Per i dispositivi digitali video, *lpPlay* punta a una [**struttura \_ DGV \_ Play \_ parametri di MCI**](/previous-versions//dd743396(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d659a-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="d659a-142">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d659a-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d659a-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_riproduzione VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d659a-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="d659a-144">Il membro **dwAt** della struttura identificata da *lpPlay* contiene un'ora di inizio dell'intero comando o se il dispositivo viene riavviato, quando il dispositivo raggiunge la posizione dalla posizione specificata dal comando [MCI \_ cue](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="d659a-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>\_ \_ riproduzione \_ REverse VCR MCI</span><span class="sxs-lookup"><span data-stu-id="d659a-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="d659a-146">La riproduzione deve essere eseguita in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="d659a-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_ \_ analisi riproduzione VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d659a-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="d659a-148">La riproduzione dovrebbe essere il più veloce possibile mantenendo l'output del video.</span><span class="sxs-lookup"><span data-stu-id="d659a-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="d659a-149">Per i dispositivi VCR, *lpPlay* punta a una struttura parametri di [**riproduzione del \_ VCR \_ \_ MCI**](mci-vcr-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d659a-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="d659a-150">Con il tipo di dispositivo **videodisco** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d659a-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d659a-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>\_ \_ riproduzione \_ rapida di MCI VD</span><span class="sxs-lookup"><span data-stu-id="d659a-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="d659a-152">Riproduzione rapida.</span><span class="sxs-lookup"><span data-stu-id="d659a-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>\_Riproduci MCI VD \_ \_ Reverse</span><span class="sxs-lookup"><span data-stu-id="d659a-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="d659a-154">Riproduci in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="d659a-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>\_ \_ analisi riproduzione MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="d659a-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="d659a-156">Eseguire un'analisi rapida.</span><span class="sxs-lookup"><span data-stu-id="d659a-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>\_ \_ riproduzione \_ lenta di MCI VD</span><span class="sxs-lookup"><span data-stu-id="d659a-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="d659a-158">Riproduci lentamente.</span><span class="sxs-lookup"><span data-stu-id="d659a-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="d659a-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_velocità di \_ riproduzione MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="d659a-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="d659a-160">La velocità di riproduzione è inclusa nel membro **dwSpeed** della struttura identificata da *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="d659a-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d659a-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d659a-161">Requirements</span></span>



| <span data-ttu-id="d659a-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="d659a-162">Requirement</span></span> | <span data-ttu-id="d659a-163">Valore</span><span class="sxs-lookup"><span data-stu-id="d659a-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d659a-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d659a-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d659a-165">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d659a-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d659a-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d659a-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d659a-167">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d659a-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d659a-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d659a-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="d659a-169"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d659a-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d659a-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d659a-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d659a-171">MCI</span><span class="sxs-lookup"><span data-stu-id="d659a-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d659a-172">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="d659a-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


---
title: Comando MCI_SETAUDIO (mmsystem. h)
description: Il \_ comando MCI seaudio imposta i valori associati alla riproduzione audio e all'acquisizione. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- Comando MCI_SETAUDIO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225230"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="f7bb3-105">\_Comando MCI SEfonica</span><span class="sxs-lookup"><span data-stu-id="f7bb3-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="f7bb3-106">Il \_ comando MCI seaudio imposta i valori associati alla riproduzione audio e all'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="f7bb3-107">I dispositivi Digital-video e VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="f7bb3-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="f7bb3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7bb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7bb3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f7bb3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f7bb3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="f7bb3-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f7bb3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span><span class="sxs-lookup"><span data-stu-id="f7bb3-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f7bb3-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7bb3-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7bb3-118">Return Value</span></span>

<span data-ttu-id="f7bb3-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7bb3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7bb3-120">Remarks</span></span>

<span data-ttu-id="f7bb3-121">I flag seguenti si applicano al tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="f7bb3-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f7bb3-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ sefonica \_ ALG</span><span class="sxs-lookup"><span data-stu-id="f7bb3-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-123">Il membro **lpstrAlgorithm** della struttura identificata da *lpSetAudio* contiene un indirizzo di un buffer contenente il nome di un algoritmo di compressione audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="f7bb3-124">L'algoritmo di compressione viene usato dai comandi di [ \_ riserva MCI](mci-reserve.md) o del [ \_ record MCI](mci-record.md) successivi.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="f7bb3-125">Gli algoritmi disponibili sono dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="f7bb3-126">Se l'algoritmo non è compatibile con il formato di file corrente, il formato del file viene modificato nel formato predefinito per l'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>\_CLOCKTIME DGV \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-128">Il tempo specificato è in millisecondi ed è il tempo assoluto se usato con \_ DGV di MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="f7bb3-129">Questa volta non è al passo con la riproduzione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_input di DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-131">Modifica il flag Bass, Treble o volume in modo che influisca sul segnale di input e modifichi gli elementi registrati.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="f7bb3-132">Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_elemento DGV \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-134">Una costante audio è specificata nel membro **dwItem** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-135">La costante identifica il valore che viene impostato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="f7bb3-136">Sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7bb3-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>\_AVGBYTESPERSEC DGV \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-138">Il numero medio di byte viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-139">Questo valore consente di impostare il numero medio di byte al secondo per la riproduzione o la registrazione nei formati PCM (Pulse Code Modulation) e ADPCM (Adaptive differenziale Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="f7bb3-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="f7bb3-140">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>\_Bass DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-142">Il livello di frequenza bassa audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>\_BitsPerSample DGV \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-144">Il numero di bit per campione viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-145">Questo valore consente di impostare il numero di bit per campione riprodotto o registrato nel formato PCM.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="f7bb3-146">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>\_BLOCKALIGN DGV \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-148">L'allineamento dei blocchi di dati viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-149">Questo valore imposta l'allineamento dei blocchi di dati rispetto all'inizio dei dati della forma d'onda di input.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>\_SAMPLESPERSEC DGV \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-151">La frequenza di campionamento è specificata nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-152">Questo valore consente di impostare la frequenza di campionamento per la riproduzione e la registrazione con gli algoritmi PCM e ADPCM.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="f7bb3-153">Il file viene salvato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_origine DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-155">Una costante che specifica l'origine dell'input audio è inclusa nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-156">Per le origini di input audio sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7bb3-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="f7bb3-157">\_ \_ \_ media origine DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="f7bb3-158">Media dei canali audio sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="f7bb3-159">\_origine DGV \_ \_ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="f7bb3-160">Canale audio sinistro.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-160">Left audio channel.</span></span>

<span data-ttu-id="f7bb3-161">DGV di origine del file MCI- \_ \_ \_ \_ right</span><span class="sxs-lookup"><span data-stu-id="f7bb3-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="f7bb3-162">Canale audio corretto.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-162">Right audio channel.</span></span>

<span data-ttu-id="f7bb3-163">\_stereo di \_ origine DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="f7bb3-164">Stereo.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_flusso DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-166">Un flusso audio viene specificato nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-167">Il valore integer specifica il flusso audio riprodotto dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="f7bb3-168">Se il flusso non è specificato, viene riprodotto il primo flusso audio con interfoliazione fisico.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>gli \_ \_ acuti DGV di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-170">Il livello di frequenza elevata audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_volume DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-172">Il livello audio per uno o entrambi i canali audio viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-173">Se i volumi sinistro e destro sono stati impostati su valori diversi, il rapporto tra il volume da sinistra a destra è approssimativamente invariato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ \_ Left</span><span class="sxs-lookup"><span data-stu-id="f7bb3-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-175">Abilita il canale audio sinistro se usato con MCI \_ impostato \_ su.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="f7bb3-176">Disabilita il canale audio sinistro se usato con MCI \_ impostato su \_ off.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="f7bb3-177">Quando questo flag viene usato con la combinazione di \_ DGV \_ \_ e MCI DGV del volume MCI \_ \_ \_ , imposta il volume del canale audio sinistro.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="f7bb3-178">Quando questo flag viene usato con l' \_ \_ \_ origine DGV di MCI, specifica il canale audio sinistro come origine per il digitalizzatore di input audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>\_DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-180">Un parametro della lunghezza della transizione è incluso nel membro **dwOver** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-181">Il valore length specifica la durata (in unità del formato dell'ora corrente) da eseguire per apportare una modifica che utilizza un fattore.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="f7bb3-182">Se questo flag non viene utilizzato, le modifiche vengono eseguite immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_qualità dell' \_ audio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-184">Il membro **lpstrQuality** della struttura identificata da *lpSetAudio* contiene un indirizzo di un buffer che definisce la qualità audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="f7bb3-185">Una stringa di testo all'interno del buffer specifica le caratteristiche dell'algoritmo di compressione audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="f7bb3-186">Per \_ \_ \_ selezionare un descrittore di qualità per l'algoritmo specificato, è possibile usare il flag DGV di MCI.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="f7bb3-187">Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="f7bb3-188">Gli algoritmi e i nomi dei descrittori disponibili dipendono dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="f7bb3-189">Ogni dispositivo fornisce la documentazione per gli algoritmi disponibili e una descrizione dei nomi di descrittori applicabili.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="f7bb3-190">Il comando [MCI \_ Quality](mci-quality.md) può definire nomi di descrittori aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_record DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-192">Specifica se la registrazione include o esclude i dati audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="f7bb3-193">In combinazione con MCI \_ impostato \_ su, vengono registrati i dati audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="f7bb3-194">In combinazione con MCI \_ impostato su \_ disattivato, i dati audio vengono esclusi.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="f7bb3-195">Il valore predefinito include i dati audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>DGV MCI a \_ \_ \_ destra</span><span class="sxs-lookup"><span data-stu-id="f7bb3-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-197">Abilita il canale audio corretto se usato con MCI \_ impostato \_ su.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="f7bb3-198">Disattiva il canale audio corretto se usato con MCI \_ impostato su \_ off.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="f7bb3-199">Quando questo flag viene usato con la combinazione di \_ DGV \_ \_ e MCI DGV del volume MCI \_ \_ \_ , imposta il volume del canale audio corretto.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_valore di DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-201">Viene specificato un valore nel membro **dwValue** della struttura identificata da *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="f7bb3-202">Il significato del valore viene specificato dalla costante definita per il \_ flag di elemento DGV di MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="f7bb3-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-204">Disabilita il canale audio specificato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="f7bb3-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-206">Abilita il canale audio specificato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f7bb3-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>OUTPUT di MCI \_ SEfonica \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-208">Modifica il flag Bass, Treble o volume in modo che modifichi solo il segnale riprodotto e non quello registrato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="f7bb3-209">Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="f7bb3-210">Per i dispositivi digitali video, il parametro *lpSetAudio* punta a una struttura [**MCI \_ DGV \_ \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="f7bb3-211">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7bb3-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f7bb3-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_record di \_ disaudio \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f7bb3-213">Imposta la registrazione audio su on o off, che viene utilizzata insieme a uno dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7bb3-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="f7bb3-214">MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="f7bb3-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="f7bb3-215">Registrazione audio in.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-215">Audio recording on.</span></span>

<span data-ttu-id="f7bb3-216">\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="f7bb3-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="f7bb3-217">Registrazione audio disattivata.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-217">Audio recording off.</span></span> <span data-ttu-id="f7bb3-218">Prima di disattivare la registrazione audio, potrebbe essere necessario disattivare la registrazione di assemblaggio (usando il comando [MCI \_ set](mci-set.md) con il \_ flag MCI \_ set \_ assembla \_ record impostato su OFF).</span><span class="sxs-lookup"><span data-stu-id="f7bb3-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="f7bb3-219">\_traccia MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-219">MCI\_TRACK</span></span>

<span data-ttu-id="f7bb3-220">Il membro **dwTrack** della struttura identificata da *lpSetAudio* specifica la traccia interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="f7bb3-221">\_origine file VCR VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7bb3-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="f7bb3-222">Imposta l'origine audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-222">Sets the audio source.</span></span> <span data-ttu-id="f7bb3-223">Questo flag deve essere utilizzato con l' \_ \_ \_ opzione per il flag di MCI VCR per il flag.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="f7bb3-224">\_ \_ monitoraggio sefonica VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="f7bb3-225">Imposta il monitor di origine audio.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-225">Sets the audio source monitor.</span></span> <span data-ttu-id="f7bb3-226">Questo flag deve essere utilizzato con l' \_ \_ \_ opzione per il flag di MCI VCR per il flag.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="f7bb3-227">\_VCR VCR MCI \_ \_ per</span><span class="sxs-lookup"><span data-stu-id="f7bb3-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="f7bb3-228">Il membro **dwTo** della struttura identificata da *lpSetAudio* contiene una costante che descrive il tipo di input o di input monitorato.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="f7bb3-229">Deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7bb3-229">It must be one of the following:</span></span>

<span data-ttu-id="f7bb3-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="f7bb3-230"><dl> <dd></span></span>

<span data-ttu-id="f7bb3-231">\_Tuner di \_ \_ tipo src VCR di \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="f7bb3-232">Il tipo è Tuner.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="f7bb3-233">\_ \_ \_ riga tipo src VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="f7bb3-234">Il tipo è line.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="f7bb3-235">\_ \_ tipo src VCR \_ MCI \_ aux</span><span class="sxs-lookup"><span data-stu-id="f7bb3-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="f7bb3-236">Il tipo è ausiliario.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="f7bb3-237">\_ \_ tipo src VCR \_ MCI \_ generico</span><span class="sxs-lookup"><span data-stu-id="f7bb3-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="f7bb3-238">Il tipo è generico.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="f7bb3-239">\_silenziamento del \_ \_ tipo src del VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="f7bb3-240">Il tipo è mute.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-240">Type is mute.</span></span> <span data-ttu-id="f7bb3-241">Questa operazione può essere utilizzata solo con il \_ \_ flag di origine sefonica VCR MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="f7bb3-242">\_ \_ \_ output tipo src VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="f7bb3-243">Il tipo è output.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="f7bb3-244">\_numero di \_ file VCR \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="f7bb3-245">Il membro dwNumber della struttura identificata da lpSetAudio contiene l'input audio (del tipo specificato nel membro dwTo) da usare.</span><span class="sxs-lookup"><span data-stu-id="f7bb3-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="f7bb3-246">Per i dispositivi VCR, il parametro *lpSetAudio* punta a una struttura [**\_ \_ \_ parametri del videoregistratore MCI**](mci-vcr-setaudio-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f7bb3-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7bb3-247">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7bb3-247">Requirements</span></span>



| <span data-ttu-id="f7bb3-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7bb3-248">Requirement</span></span> | <span data-ttu-id="f7bb3-249">Valore</span><span class="sxs-lookup"><span data-stu-id="f7bb3-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bb3-250">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7bb3-250">Minimum supported client</span></span><br/> | <span data-ttu-id="f7bb3-251">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7bb3-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7bb3-252">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7bb3-252">Minimum supported server</span></span><br/> | <span data-ttu-id="f7bb3-253">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7bb3-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f7bb3-254">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7bb3-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7bb3-255"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7bb3-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7bb3-256">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7bb3-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7bb3-257">MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f7bb3-258">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="f7bb3-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


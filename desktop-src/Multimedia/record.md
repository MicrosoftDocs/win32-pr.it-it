---
title: comando record
description: Il comando record avvia la registrazione dei dati. VCR e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- registrare il comando Windows Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873349"
---
# <a name="record-command"></a><span data-ttu-id="7b8b0-106">comando record</span><span class="sxs-lookup"><span data-stu-id="7b8b0-106">record command</span></span>

<span data-ttu-id="7b8b0-107">Il comando record avvia la registrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-107">The record command starts recording data.</span></span> <span data-ttu-id="7b8b0-108">VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="7b8b0-109">Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo implementano.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="7b8b0-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7b8b0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b8b0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b8b0-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7b8b0-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-113">Identifier of an MCI device.</span></span> <span data-ttu-id="7b8b0-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7b8b0-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7b8b0-116">Flag per la registrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-116">Flag for recording data.</span></span> <span data-ttu-id="7b8b0-117">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **registra** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="7b8b0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7b8b0-118">Value</span></span>        | <span data-ttu-id="7b8b0-119">Significato</span><span class="sxs-lookup"><span data-stu-id="7b8b0-119">Meaning</span></span>                                                | <span data-ttu-id="7b8b0-120">Significato</span><span class="sxs-lookup"><span data-stu-id="7b8b0-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="7b8b0-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="7b8b0-121">digitalvideo</span></span> | <span data-ttu-id="7b8b0-122">al *flusso* del flusso audio *rettangolare* dalla *posizione* in attesa</span><span class="sxs-lookup"><span data-stu-id="7b8b0-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="7b8b0-123">Inserisci Sovrascrivi per *posizionare* il *flusso* del flusso video</span><span class="sxs-lookup"><span data-stu-id="7b8b0-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="7b8b0-124">sequencer</span><span class="sxs-lookup"><span data-stu-id="7b8b0-124">sequencer</span></span>    | <span data-ttu-id="7b8b0-125">da *position* Insert</span><span class="sxs-lookup"><span data-stu-id="7b8b0-125">from *position* insert</span></span>                                  | <span data-ttu-id="7b8b0-126">Sovrascrivi in *posizione*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="7b8b0-127">VCR</span><span class="sxs-lookup"><span data-stu-id="7b8b0-127">vcr</span></span>          | <span data-ttu-id="7b8b0-128">al *momento* dall'inizializzazione della *posizione*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="7b8b0-129">Inserisci sovrascrittura nella *posizione*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="7b8b0-130">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="7b8b0-130">waveaudio</span></span>    | <span data-ttu-id="7b8b0-131">da *position* Insert</span><span class="sxs-lookup"><span data-stu-id="7b8b0-131">from *position* insert</span></span>                                  | <span data-ttu-id="7b8b0-132">Sovrascrivi in *posizione*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="7b8b0-133">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszRecordFlags** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="7b8b0-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7b8b0-134">Value</span></span>                 | <span data-ttu-id="7b8b0-135">Significato</span><span class="sxs-lookup"><span data-stu-id="7b8b0-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8b0-136">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-136">at *rectangle*</span></span>        | <span data-ttu-id="7b8b0-137">Specifica un'area rettangolare dell'input esterno usato come origine per i pixel compressi e salvati.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="7b8b0-138">Se non specificato, per impostazione predefinita il rettangolo è il rettangolo specificato per [put](put.md) "video".</span><span class="sxs-lookup"><span data-stu-id="7b8b0-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="7b8b0-139">Quando viene impostato in modo diverso rispetto al rettangolo "video", l'immagine visualizzata non è quella registrata.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="7b8b0-140">al *momento*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-140">at *time*</span></span>             | <span data-ttu-id="7b8b0-141">Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato riavviato, quando viene avviato il comando.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="7b8b0-142">Per ulteriori informazioni, vedere il comando [cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="7b8b0-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="7b8b0-143">*flusso* del flusso audio</span><span class="sxs-lookup"><span data-stu-id="7b8b0-143">audio stream *stream*</span></span> | <span data-ttu-id="7b8b0-144">Specifica il flusso audio usato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="7b8b0-145">Se questo flag non è specificato e il formato di file non definisce un valore predefinito, viene registrato nel flusso fisicamente per primo.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="7b8b0-146">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-146">from *position*</span></span>       | <span data-ttu-id="7b8b0-147">Specifica una posizione iniziale per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="7b8b0-148">Se il flag "from" non è specificato, il dispositivo avvia la registrazione nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="7b8b0-149">contenere</span><span class="sxs-lookup"><span data-stu-id="7b8b0-149">hold</span></span>                  | <span data-ttu-id="7b8b0-150">Blocca l'immagine al termine della registrazione anziché visualizzare il video in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="7b8b0-151">Quando la registrazione viene arrestata, viene eseguito un comando di [monitoraggio](monitor.md) automatico "file".</span><span class="sxs-lookup"><span data-stu-id="7b8b0-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="7b8b0-152">Per tornare al video live, eseguire il comando **Monitor** "input".</span><span class="sxs-lookup"><span data-stu-id="7b8b0-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="7b8b0-153">inizializzazione</span><span class="sxs-lookup"><span data-stu-id="7b8b0-153">initialize</span></span>            | <span data-ttu-id="7b8b0-154">Inizializzare il nastro (supporto), che prevede la registrazione del codice temporale (se possibile) per video e audio vuoti.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="7b8b0-155">Questo comando può richiedere diverse ore se è necessario inizializzare l'intero nastro.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="7b8b0-156">insert</span><span class="sxs-lookup"><span data-stu-id="7b8b0-156">insert</span></span>                | <span data-ttu-id="7b8b0-157">Specifica che i nuovi dati vengono aggiunti al file nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="7b8b0-158">overwrite</span><span class="sxs-lookup"><span data-stu-id="7b8b0-158">overwrite</span></span>             | <span data-ttu-id="7b8b0-159">Consente di specificare che i nuovi dati sostituiranno i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7b8b0-160">*posizione*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-160">to *position*</span></span>         | <span data-ttu-id="7b8b0-161">Specifica una posizione finale per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="7b8b0-162">Se il flag "to" non è specificato, il dispositivo viene registrato fino a quando non viene ricevuto un comando [Stop](stop.md) o [pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="7b8b0-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="7b8b0-163">*flusso* del flusso video</span><span class="sxs-lookup"><span data-stu-id="7b8b0-163">video stream *stream*</span></span> | <span data-ttu-id="7b8b0-164">Specifica il flusso video usato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="7b8b0-165">Se questo parametro non viene specificato e il formato del file non definisce un valore predefinito, viene registrato nel flusso fisicamente per primo.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="7b8b0-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7b8b0-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7b8b0-167">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="7b8b0-168">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="7b8b0-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="7b8b0-169">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7b8b0-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b8b0-170">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b8b0-170">Return Value</span></span>

<span data-ttu-id="7b8b0-171">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8b0-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b8b0-172">Remarks</span></span>

<span data-ttu-id="7b8b0-173">La registrazione si interrompe quando viene eseguito un comando di [arresto](stop.md) o [sospensione](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="7b8b0-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="7b8b0-174">Per il driver MCIWAVE, tutti i dati registrati dopo l'apertura di un file vengono eliminati se il file viene chiuso senza salvarlo.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="7b8b0-175">Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="7b8b0-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="7b8b0-176">Le tracce da registrare sono specificate dal [setimecode](settimecode.md) "record", impostare i comandi "assembla record", [sevideo](setvideo.md) "record [" e "record".](setaudio.md)</span><span class="sxs-lookup"><span data-stu-id="7b8b0-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="7b8b0-177">Esempio</span><span class="sxs-lookup"><span data-stu-id="7b8b0-177">Examples</span></span>

<span data-ttu-id="7b8b0-178">Il comando seguente avvia la registrazione nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b8b0-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="7b8b0-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b8b0-179">Requirements</span></span>



| <span data-ttu-id="7b8b0-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b8b0-180">Requirement</span></span> | <span data-ttu-id="7b8b0-181">Valore</span><span class="sxs-lookup"><span data-stu-id="7b8b0-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7b8b0-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b8b0-182">Minimum supported client</span></span><br/> | <span data-ttu-id="7b8b0-183">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b8b0-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7b8b0-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b8b0-184">Minimum supported server</span></span><br/> | <span data-ttu-id="7b8b0-185">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b8b0-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7b8b0-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b8b0-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b8b0-187">MCI</span><span class="sxs-lookup"><span data-stu-id="7b8b0-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-188">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="7b8b0-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-189">segnale</span><span class="sxs-lookup"><span data-stu-id="7b8b0-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-190">monitoraggio</span><span class="sxs-lookup"><span data-stu-id="7b8b0-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-191">pause</span><span class="sxs-lookup"><span data-stu-id="7b8b0-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-192">mettere</span><span class="sxs-lookup"><span data-stu-id="7b8b0-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-193">set</span><span class="sxs-lookup"><span data-stu-id="7b8b0-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-194">SetAudio</span><span class="sxs-lookup"><span data-stu-id="7b8b0-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-195">codice temporale</span><span class="sxs-lookup"><span data-stu-id="7b8b0-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-196">video</span><span class="sxs-lookup"><span data-stu-id="7b8b0-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="7b8b0-197">stop</span><span class="sxs-lookup"><span data-stu-id="7b8b0-197">stop</span></span>](stop.md)
</dt> </dl>

 


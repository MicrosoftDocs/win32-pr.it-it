---
title: comando seek
description: Il comando Seek passa alla posizione specificata e si arresta. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- comando Cerca Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400257"
---
# <a name="seek-command"></a><span data-ttu-id="c769b-105">comando seek</span><span class="sxs-lookup"><span data-stu-id="c769b-105">seek command</span></span>

<span data-ttu-id="c769b-106">Il comando Seek passa alla posizione specificata e si arresta.</span><span class="sxs-lookup"><span data-stu-id="c769b-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="c769b-107">CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c769b-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="c769b-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c769b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c769b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c769b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c769b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c769b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c769b-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c769b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c769b-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="c769b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c769b-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span><span class="sxs-lookup"><span data-stu-id="c769b-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c769b-114">Flag per lo stato di passaggio a una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c769b-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="c769b-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Seek** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="c769b-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="c769b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c769b-116">Value</span></span>        | <span data-ttu-id="c769b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c769b-117">Meaning</span></span>                          | <span data-ttu-id="c769b-118">Significato</span><span class="sxs-lookup"><span data-stu-id="c769b-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="c769b-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="c769b-119">cdaudio</span></span>      | <span data-ttu-id="c769b-120">per terminare la *posizione*</span><span class="sxs-lookup"><span data-stu-id="c769b-120">to end to *position*</span></span>             | <span data-ttu-id="c769b-121">per iniziare</span><span class="sxs-lookup"><span data-stu-id="c769b-121">to start</span></span>                     |
| <span data-ttu-id="c769b-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c769b-122">digitalvideo</span></span> | <span data-ttu-id="c769b-123">per terminare la *posizione*</span><span class="sxs-lookup"><span data-stu-id="c769b-123">to end to *position*</span></span>             | <span data-ttu-id="c769b-124">per iniziare</span><span class="sxs-lookup"><span data-stu-id="c769b-124">to start</span></span>                     |
| <span data-ttu-id="c769b-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="c769b-125">sequencer</span></span>    | <span data-ttu-id="c769b-126">per terminare la *posizione*</span><span class="sxs-lookup"><span data-stu-id="c769b-126">to end to *position*</span></span>             | <span data-ttu-id="c769b-127">per iniziare</span><span class="sxs-lookup"><span data-stu-id="c769b-127">to start</span></span>                     |
| <span data-ttu-id="c769b-128">VCR</span><span class="sxs-lookup"><span data-stu-id="c769b-128">vcr</span></span>          | <span data-ttu-id="c769b-129">al *segno* di *spunta \_ num*</span><span class="sxs-lookup"><span data-stu-id="c769b-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="c769b-130">per terminare la *posizione* iniziale</span><span class="sxs-lookup"><span data-stu-id="c769b-130">to end to *position* to start</span></span> |
| <span data-ttu-id="c769b-131">videodisco</span><span class="sxs-lookup"><span data-stu-id="c769b-131">videodisc</span></span>    | <span data-ttu-id="c769b-132">Inverti alla fine</span><span class="sxs-lookup"><span data-stu-id="c769b-132">reverse to end</span></span>                   | <span data-ttu-id="c769b-133">per *posizionare* l'avvio</span><span class="sxs-lookup"><span data-stu-id="c769b-133">to *position* to start</span></span>        |
| <span data-ttu-id="c769b-134">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="c769b-134">waveaudio</span></span>    | <span data-ttu-id="c769b-135">per terminare la *posizione*</span><span class="sxs-lookup"><span data-stu-id="c769b-135">to end to *position*</span></span>             | <span data-ttu-id="c769b-136">per iniziare</span><span class="sxs-lookup"><span data-stu-id="c769b-136">to start</span></span>                     |



 

<span data-ttu-id="c769b-137">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszSeekFlags** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="c769b-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="c769b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="c769b-138">Value</span></span>            | <span data-ttu-id="c769b-139">Significato</span><span class="sxs-lookup"><span data-stu-id="c769b-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c769b-140">al *momento*</span><span class="sxs-lookup"><span data-stu-id="c769b-140">at *time*</span></span>        | <span data-ttu-id="c769b-141">Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato riavviato, quando viene avviato il comando.</span><span class="sxs-lookup"><span data-stu-id="c769b-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="c769b-142">Per ulteriori informazioni, vedere il comando [cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="c769b-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="c769b-143">segno *di \_ spunta*</span><span class="sxs-lookup"><span data-stu-id="c769b-143">mark *mark\_num*</span></span> | <span data-ttu-id="c769b-144">Cerca il contrassegno relativo indicato da *Mark \_ num*, che deve essere un valore intero positivo.</span><span class="sxs-lookup"><span data-stu-id="c769b-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="c769b-145">I contrassegni sono segnali scritti sul nastro VCR usando il comando [Mark](mark.md) e vengono usati per la ricerca ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="c769b-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="c769b-146">reverse</span><span class="sxs-lookup"><span data-stu-id="c769b-146">reverse</span></span>          | <span data-ttu-id="c769b-147">Indica che la direzione di ricerca nei VCR e videodischi CAV è precedente.</span><span class="sxs-lookup"><span data-stu-id="c769b-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="c769b-148">Questo flag non è valido se è specificato il flag "to".</span><span class="sxs-lookup"><span data-stu-id="c769b-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="c769b-149">Per i VCR, questo flag deve essere usato con il flag "Mark".</span><span class="sxs-lookup"><span data-stu-id="c769b-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="c769b-150">alla fine</span><span class="sxs-lookup"><span data-stu-id="c769b-150">to end</span></span>           | <span data-ttu-id="c769b-151">Cerca alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="c769b-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="c769b-152">*posizione*</span><span class="sxs-lookup"><span data-stu-id="c769b-152">to *position*</span></span>    | <span data-ttu-id="c769b-153">Specifica la posizione in cui arrestare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="c769b-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="c769b-154">Per i dispositivi **CDAudio** , MCI restituisce un errore non compreso nell'intervallo se la posizione specificata è maggiore della lunghezza del disco.</span><span class="sxs-lookup"><span data-stu-id="c769b-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="c769b-155">per iniziare</span><span class="sxs-lookup"><span data-stu-id="c769b-155">to start</span></span>         | <span data-ttu-id="c769b-156">Cerca l'inizio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="c769b-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="c769b-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c769b-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c769b-158">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c769b-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c769b-159">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="c769b-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c769b-160">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c769b-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c769b-161">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c769b-161">Return Value</span></span>

<span data-ttu-id="c769b-162">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c769b-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c769b-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="c769b-163">Remarks</span></span>

<span data-ttu-id="c769b-164">Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="c769b-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="c769b-165">I dispositivi digitali video supportano due modalità di ricerca, che è possibile modificare usando il comando [imposta](set.md) .</span><span class="sxs-lookup"><span data-stu-id="c769b-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="c769b-166">La modalità "seek exactly on" causa il passaggio del comando seek al frame specificato.</span><span class="sxs-lookup"><span data-stu-id="c769b-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="c769b-167">La modalità "seek exactly off" causa il passaggio del comando seek al fotogramma chiave più vicino prima del frame specificato.</span><span class="sxs-lookup"><span data-stu-id="c769b-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="c769b-168">Se un dispositivo audio CD viene riprodotto quando viene emesso il comando seek, la riproduzione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="c769b-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="c769b-169">Quando il comando Seek viene emesso con un dispositivo videodisco, il dispositivo esegue la ricerca con l'opzione di avanzamento rapido o veloce con audio e video.</span><span class="sxs-lookup"><span data-stu-id="c769b-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="c769b-170">Quando il comando Seek viene emesso con un dispositivo audio Waveform, il comportamento dipende dalle dimensioni del campione.</span><span class="sxs-lookup"><span data-stu-id="c769b-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="c769b-171">Se le dimensioni del campione sono pari o superiori a 16 bit, Seek si sposta all'inizio dell'esempio più vicino quando una posizione specificata non coincide con l'inizio di un campione.</span><span class="sxs-lookup"><span data-stu-id="c769b-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="c769b-172">Esempio</span><span class="sxs-lookup"><span data-stu-id="c769b-172">Examples</span></span>

<span data-ttu-id="c769b-173">Il comando seguente consente di cercare l'inizio del file multimediale associato al dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="c769b-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="c769b-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c769b-174">Requirements</span></span>



| <span data-ttu-id="c769b-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="c769b-175">Requirement</span></span> | <span data-ttu-id="c769b-176">Valore</span><span class="sxs-lookup"><span data-stu-id="c769b-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c769b-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c769b-177">Minimum supported client</span></span><br/> | <span data-ttu-id="c769b-178">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c769b-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c769b-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c769b-179">Minimum supported server</span></span><br/> | <span data-ttu-id="c769b-180">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c769b-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c769b-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c769b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c769b-182">MCI</span><span class="sxs-lookup"><span data-stu-id="c769b-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c769b-183">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="c769b-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c769b-184">segnale</span><span class="sxs-lookup"><span data-stu-id="c769b-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="c769b-185">contrassegnare</span><span class="sxs-lookup"><span data-stu-id="c769b-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="c769b-186">set</span><span class="sxs-lookup"><span data-stu-id="c769b-186">set</span></span>](set.md)
</dt> </dl>

 


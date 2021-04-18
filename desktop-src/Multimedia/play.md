---
title: comando Play
description: Il comando Play avvia la riproduzione di un dispositivo. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- comando Riproduci Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301372"
---
# <a name="play-command"></a><span data-ttu-id="eda37-105">comando Play</span><span class="sxs-lookup"><span data-stu-id="eda37-105">play command</span></span>

<span data-ttu-id="eda37-106">Il comando Play avvia la riproduzione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eda37-106">The play command starts playing a device.</span></span> <span data-ttu-id="eda37-107">CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="eda37-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="eda37-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="eda37-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="eda37-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="eda37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda37-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="eda37-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="eda37-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="eda37-111">Identifier of an MCI device.</span></span> <span data-ttu-id="eda37-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="eda37-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="eda37-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span><span class="sxs-lookup"><span data-stu-id="eda37-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="eda37-114">Flag per la riproduzione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eda37-114">Flag for playing a device.</span></span> <span data-ttu-id="eda37-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Play** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="eda37-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="eda37-116">Valore</span><span class="sxs-lookup"><span data-stu-id="eda37-116">Value</span></span>        | <span data-ttu-id="eda37-117">Significato</span><span class="sxs-lookup"><span data-stu-id="eda37-117">Meaning</span></span>                          | <span data-ttu-id="eda37-118">Significato</span><span class="sxs-lookup"><span data-stu-id="eda37-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="eda37-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="eda37-119">cdaudio</span></span>      | <span data-ttu-id="eda37-120">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-120">from *position*</span></span>                  | <span data-ttu-id="eda37-121">*posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-121">to *position*</span></span>                     |
| <span data-ttu-id="eda37-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="eda37-122">digitalvideo</span></span> | <span data-ttu-id="eda37-123">dalla *posizione* di ripetizione a schermo intero</span><span class="sxs-lookup"><span data-stu-id="eda37-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="eda37-124">Inverti alla finestra *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="eda37-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="eda37-125">sequencer</span></span>    | <span data-ttu-id="eda37-126">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-126">from *position*</span></span>                  | <span data-ttu-id="eda37-127">*posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-127">to *position*</span></span>                     |
| <span data-ttu-id="eda37-128">VCR</span><span class="sxs-lookup"><span data-stu-id="eda37-128">vcr</span></span>          | <span data-ttu-id="eda37-129">al *momento* dalla *posizione* inversa</span><span class="sxs-lookup"><span data-stu-id="eda37-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="eda37-130">analizza in *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-130">scan to *position*</span></span>                |
| <span data-ttu-id="eda37-131">videodisco</span><span class="sxs-lookup"><span data-stu-id="eda37-131">videodisc</span></span>    | <span data-ttu-id="eda37-132">analisi inversa rapida dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="eda37-133">velocità *intera* lenta nella *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="eda37-134">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="eda37-134">waveaudio</span></span>    | <span data-ttu-id="eda37-135">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-135">from *position*</span></span>                  | <span data-ttu-id="eda37-136">*posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-136">to *position*</span></span>                     |



 

<span data-ttu-id="eda37-137">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszPlayFlags** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="eda37-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="eda37-138">Valore</span><span class="sxs-lookup"><span data-stu-id="eda37-138">Value</span></span>           | <span data-ttu-id="eda37-139">Significato</span><span class="sxs-lookup"><span data-stu-id="eda37-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eda37-140">al *momento*</span><span class="sxs-lookup"><span data-stu-id="eda37-140">at *time*</span></span>       | <span data-ttu-id="eda37-141">Indica quando il dispositivo deve iniziare a eseguire questo comando o, se il dispositivo è stato riavviato, quando viene avviato il comando.</span><span class="sxs-lookup"><span data-stu-id="eda37-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="eda37-142">Per ulteriori informazioni, vedere il comando [cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="eda37-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="eda37-143">veloce</span><span class="sxs-lookup"><span data-stu-id="eda37-143">fast</span></span>            | <span data-ttu-id="eda37-144">Indica che il dispositivo deve essere riprodotto più velocemente del normale.</span><span class="sxs-lookup"><span data-stu-id="eda37-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="eda37-145">Per determinare la velocità esatta in un lettore videodisco, usare il flag "Speed" del comando [status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="eda37-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="eda37-146">Per specificare la velocità più precisa, usare il flag "Speed" del comando.</span><span class="sxs-lookup"><span data-stu-id="eda37-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="eda37-147">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-147">from *position*</span></span> | <span data-ttu-id="eda37-148">Specifica una posizione iniziale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eda37-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="eda37-149">Se il flag "from" non è specificato, la riproduzione inizia in corrispondenza della posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="eda37-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="eda37-150">Per i dispositivi **CDAudio** , se la posizione "da" è maggiore della posizione finale del disco o se la posizione "da" è maggiore della posizione "a", il driver restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="eda37-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="eda37-151">Per i dispositivi **videodisco** , le posizioni predefinite sono in frame per i dischi CAV e in ore, minuti e secondi per i dischi CLV.</span><span class="sxs-lookup"><span data-stu-id="eda37-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="eda37-152">schermo intero</span><span class="sxs-lookup"><span data-stu-id="eda37-152">fullscreen</span></span>      | <span data-ttu-id="eda37-153">Specifica che deve essere utilizzata una visualizzazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="eda37-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="eda37-154">Utilizzare questo flag solo per la riproduzione di file compressi.</span><span class="sxs-lookup"><span data-stu-id="eda37-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="eda37-155">I file non compressi non verranno riprodotti a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="eda37-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="eda37-156">ripetere</span><span class="sxs-lookup"><span data-stu-id="eda37-156">repeat</span></span>          | <span data-ttu-id="eda37-157">Specifica che la riproduzione deve essere riavviata quando viene raggiunta la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="eda37-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="eda37-158">reverse</span><span class="sxs-lookup"><span data-stu-id="eda37-158">reverse</span></span>         | <span data-ttu-id="eda37-159">Specifica che la direzione della riproduzione è precedente.</span><span class="sxs-lookup"><span data-stu-id="eda37-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="eda37-160">Non è possibile specificare un percorso finale con il flag "Reverse".</span><span class="sxs-lookup"><span data-stu-id="eda37-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="eda37-161">Per videodischi, "Scan" si applica solo al formato CAV.</span><span class="sxs-lookup"><span data-stu-id="eda37-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="eda37-162">scansione</span><span class="sxs-lookup"><span data-stu-id="eda37-162">scan</span></span>            | <span data-ttu-id="eda37-163">Riproduce il più rapidamente possibile senza disabilitare i video (anche se l'audio potrebbe essere disabilitato).</span><span class="sxs-lookup"><span data-stu-id="eda37-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="eda37-164">Per videodischi, "Scan" si applica solo al formato CAV.</span><span class="sxs-lookup"><span data-stu-id="eda37-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="eda37-165">lento</span><span class="sxs-lookup"><span data-stu-id="eda37-165">slow</span></span>            | <span data-ttu-id="eda37-166">Viene riprodotto lentamente.</span><span class="sxs-lookup"><span data-stu-id="eda37-166">Plays slowly.</span></span> <span data-ttu-id="eda37-167">Per determinare la velocità esatta in un lettore videodisco, usare il flag "Speed" del comando [status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="eda37-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="eda37-168">Per specificare la velocità più precisa, usare il flag "Speed" del comando.</span><span class="sxs-lookup"><span data-stu-id="eda37-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="eda37-169">Per videodischi, "Slow" si applica solo al formato CAV.</span><span class="sxs-lookup"><span data-stu-id="eda37-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="eda37-170">velocità *Integer*</span><span class="sxs-lookup"><span data-stu-id="eda37-170">speed *integer*</span></span> | <span data-ttu-id="eda37-171">Riproduce un videodisco alla velocità specificata, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="eda37-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="eda37-172">Questo flag si applica solo ai dischi CAV.</span><span class="sxs-lookup"><span data-stu-id="eda37-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="eda37-173">*posizione*</span><span class="sxs-lookup"><span data-stu-id="eda37-173">to *position*</span></span>   | <span data-ttu-id="eda37-174">Specifica una posizione finale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eda37-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="eda37-175">Se il flag "to" non è specificato, la riproduzione si interrompe alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="eda37-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="eda37-176">Per i dispositivi **CDAudio** , se la posizione "a" è maggiore della posizione finale del disco, il driver restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="eda37-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="eda37-177">Per i dispositivi **videodisco** , le posizioni predefinite sono in frame per i dischi CAV e in ore, minuti e secondi per i dischi CLV.</span><span class="sxs-lookup"><span data-stu-id="eda37-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="eda37-178">Finestra</span><span class="sxs-lookup"><span data-stu-id="eda37-178">window</span></span>          | <span data-ttu-id="eda37-179">Specifica che la riproduzione deve usare la finestra associata all'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eda37-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="eda37-180">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="eda37-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="eda37-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="eda37-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="eda37-182">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="eda37-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="eda37-183">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="eda37-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="eda37-184">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="eda37-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eda37-185">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eda37-185">Return Value</span></span>

<span data-ttu-id="eda37-186">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="eda37-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eda37-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="eda37-187">Remarks</span></span>

<span data-ttu-id="eda37-188">Prima di emettere comandi che usano valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="eda37-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="eda37-189">Questo comando inizia la riproduzione alla velocità corrente, come impostato con il comando set "Speed".</span><span class="sxs-lookup"><span data-stu-id="eda37-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="eda37-190">La direzione è inversa se viene specificato il flag "Reverse" o se il flag "to" viene specificato come valore minore del flag "from".</span><span class="sxs-lookup"><span data-stu-id="eda37-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="eda37-191">Se il flag "from" non è specificato, la riproduzione inizia in corrispondenza della posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="eda37-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="eda37-192">Impossibile utilizzare contemporaneamente i flag "to" e "Reverse".</span><span class="sxs-lookup"><span data-stu-id="eda37-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="eda37-193">Esempio</span><span class="sxs-lookup"><span data-stu-id="eda37-193">Examples</span></span>

<span data-ttu-id="eda37-194">Il comando seguente riproduce il dispositivo "audio" dalla posizione 1000 alla posizione 2000, inviando un messaggio di notifica al termine della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eda37-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="eda37-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eda37-195">Requirements</span></span>



| <span data-ttu-id="eda37-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="eda37-196">Requirement</span></span> | <span data-ttu-id="eda37-197">Valore</span><span class="sxs-lookup"><span data-stu-id="eda37-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="eda37-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eda37-198">Minimum supported client</span></span><br/> | <span data-ttu-id="eda37-199">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eda37-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eda37-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eda37-200">Minimum supported server</span></span><br/> | <span data-ttu-id="eda37-201">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eda37-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="eda37-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eda37-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda37-203">MCI</span><span class="sxs-lookup"><span data-stu-id="eda37-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="eda37-204">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="eda37-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="eda37-205">segnale</span><span class="sxs-lookup"><span data-stu-id="eda37-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="eda37-206">set</span><span class="sxs-lookup"><span data-stu-id="eda37-206">set</span></span>](set.md)
</dt> </dl>

 


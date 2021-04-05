---
title: CUE (comando)
description: Il comando CUE si prepara per la riproduzione o la registrazione. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Cue Command Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874638"
---
# <a name="cue-command"></a><span data-ttu-id="ab5c2-105">CUE (comando)</span><span class="sxs-lookup"><span data-stu-id="ab5c2-105">cue command</span></span>

<span data-ttu-id="ab5c2-106">Il comando CUE si prepara per la riproduzione o la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="ab5c2-107">Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="ab5c2-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ab5c2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab5c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab5c2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ab5c2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ab5c2-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="ab5c2-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ab5c2-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span><span class="sxs-lookup"><span data-stu-id="ab5c2-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="ab5c2-114">Flag che prepara un dispositivo per la riproduzione o la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="ab5c2-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **cue** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab5c2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ab5c2-116">Value</span></span></th>
<th><span data-ttu-id="ab5c2-117">Segnale</span><span class="sxs-lookup"><span data-stu-id="ab5c2-117">Cue</span></span></th>
<th><span data-ttu-id="ab5c2-118">Segnale</span><span class="sxs-lookup"><span data-stu-id="ab5c2-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab5c2-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="ab5c2-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="ab5c2-120">input</span><span class="sxs-lookup"><span data-stu-id="ab5c2-120">input</span></span></li>
<li><span data-ttu-id="ab5c2-121">noshow</span><span class="sxs-lookup"><span data-stu-id="ab5c2-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ab5c2-122">output</span><span class="sxs-lookup"><span data-stu-id="ab5c2-122">output</span></span></li>
<li><span data-ttu-id="ab5c2-123"><em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="ab5c2-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab5c2-124">VCR</span><span class="sxs-lookup"><span data-stu-id="ab5c2-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="ab5c2-125">dalla <em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="ab5c2-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="ab5c2-126">input</span><span class="sxs-lookup"><span data-stu-id="ab5c2-126">input</span></span></li>
<li><span data-ttu-id="ab5c2-127">output</span><span class="sxs-lookup"><span data-stu-id="ab5c2-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ab5c2-128">preroll</span><span class="sxs-lookup"><span data-stu-id="ab5c2-128">preroll</span></span></li>
<li><span data-ttu-id="ab5c2-129">reverse</span><span class="sxs-lookup"><span data-stu-id="ab5c2-129">reverse</span></span></li>
<li><span data-ttu-id="ab5c2-130"><em>posizione</em></span><span class="sxs-lookup"><span data-stu-id="ab5c2-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab5c2-131">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="ab5c2-131">waveaudio</span></span></td>
<td><span data-ttu-id="ab5c2-132">input</span><span class="sxs-lookup"><span data-stu-id="ab5c2-132">input</span></span></td>
<td><span data-ttu-id="ab5c2-133">output</span><span class="sxs-lookup"><span data-stu-id="ab5c2-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ab5c2-134">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszInOutTo* e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="ab5c2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ab5c2-135">Value</span></span>           | <span data-ttu-id="ab5c2-136">Significato</span><span class="sxs-lookup"><span data-stu-id="ab5c2-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5c2-137">dalla *posizione*</span><span class="sxs-lookup"><span data-stu-id="ab5c2-137">from *position*</span></span> | <span data-ttu-id="ab5c2-138">Indica dove iniziare.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ab5c2-139">input</span><span class="sxs-lookup"><span data-stu-id="ab5c2-139">input</span></span>           | <span data-ttu-id="ab5c2-140">Prepara la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-140">Prepares for recording.</span></span> <span data-ttu-id="ab5c2-141">Per i dispositivi video digitali, questo flag può essere omesso se l'origine della presentazione corrente è già l'input esterno.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="ab5c2-142">noshow</span><span class="sxs-lookup"><span data-stu-id="ab5c2-142">noshow</span></span>          | <span data-ttu-id="ab5c2-143">Prepara la riproduzione di un frame senza visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="ab5c2-144">Quando questo flag viene specificato, la visualizzazione continua a mostrare l'immagine nel buffer del frame anche se il frame corrispondente non è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="ab5c2-145">Un comando cue successivo senza questo flag e senza il flag "to" Visualizza il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="ab5c2-146">output</span><span class="sxs-lookup"><span data-stu-id="ab5c2-146">output</span></span>          | <span data-ttu-id="ab5c2-147">Prepara per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-147">Prepares for playing.</span></span> <span data-ttu-id="ab5c2-148">Se non si specifica né "input" né "output", l'impostazione predefinita è "output".</span><span class="sxs-lookup"><span data-stu-id="ab5c2-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="ab5c2-149">preroll</span><span class="sxs-lookup"><span data-stu-id="ab5c2-149">preroll</span></span>         | <span data-ttu-id="ab5c2-150">Sposta la distanza di preroll dal *punto di partenza*.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="ab5c2-151">Il punto è la posizione corrente o la posizione specificata dal flag "from".</span><span class="sxs-lookup"><span data-stu-id="ab5c2-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="ab5c2-152">reverse</span><span class="sxs-lookup"><span data-stu-id="ab5c2-152">reverse</span></span>         | <span data-ttu-id="ab5c2-153">Indica che la direzione della riproduzione è in ordine inverso (indietro).</span><span class="sxs-lookup"><span data-stu-id="ab5c2-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ab5c2-154">*posizione*</span><span class="sxs-lookup"><span data-stu-id="ab5c2-154">to *position*</span></span>   | <span data-ttu-id="ab5c2-155">Sposta l'area di lavoro nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="ab5c2-156">Per i dispositivi VCR, questo flag indica dove arrestare.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="ab5c2-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="ab5c2-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ab5c2-158">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="ab5c2-159">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="ab5c2-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="ab5c2-160">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ab5c2-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab5c2-161">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab5c2-161">Return Value</span></span>

<span data-ttu-id="ab5c2-162">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab5c2-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab5c2-163">Remarks</span></span>

<span data-ttu-id="ab5c2-164">Sebbene non sia necessario, l'invio del comando cue prima della riproduzione o della registrazione su alcuni dispositivi potrebbe ridurre il ritardo prima che il dispositivo avvii l'azione.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="ab5c2-165">Questo comando ha esito negativo se la riproduzione o la registrazione è in corso o se il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="ab5c2-166">Quando si avvia la riproduzione (usando la cue "output"), l'invio del comando [Play](play.md) con il flag "from", "to" o "Reverse" Annulla il comando cue.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="ab5c2-167">Quando si esegue il ripasso per la registrazione (tramite cue "input"), l'invio del comando [record](record.md) con il flag "from", "to" o "Initialize" Annulla il comando cue.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="ab5c2-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="ab5c2-168">Examples</span></span>

<span data-ttu-id="ab5c2-169">Il comando seguente prepara il dispositivo "audio" per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ab5c2-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="ab5c2-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab5c2-170">Requirements</span></span>



| <span data-ttu-id="ab5c2-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab5c2-171">Requirement</span></span> | <span data-ttu-id="ab5c2-172">Valore</span><span class="sxs-lookup"><span data-stu-id="ab5c2-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ab5c2-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab5c2-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5c2-174">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab5c2-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ab5c2-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab5c2-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5c2-176">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab5c2-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ab5c2-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab5c2-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5c2-178">MCI</span><span class="sxs-lookup"><span data-stu-id="ab5c2-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ab5c2-179">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="ab5c2-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="ab5c2-180">Play</span><span class="sxs-lookup"><span data-stu-id="ab5c2-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="ab5c2-181">record</span><span class="sxs-lookup"><span data-stu-id="ab5c2-181">record</span></span>](record.md)
</dt> </dl>

 


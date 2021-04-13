---
title: comando info
description: Il comando info recupera una descrizione hardware da un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- comando informazioni Windows Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400865"
---
# <a name="info-command"></a><span data-ttu-id="a54d1-105">comando info</span><span class="sxs-lookup"><span data-stu-id="a54d1-105">info command</span></span>

<span data-ttu-id="a54d1-106">Il comando info recupera una descrizione hardware da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a54d1-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="a54d1-107">Tutti i dispositivi MCI riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a54d1-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="a54d1-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a54d1-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a54d1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a54d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a54d1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a54d1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a54d1-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a54d1-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a54d1-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="a54d1-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a54d1-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span><span class="sxs-lookup"><span data-stu-id="a54d1-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="a54d1-114">Flag che identifica il tipo di informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="a54d1-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="a54d1-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **info** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="a54d1-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="a54d1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a54d1-116">Value</span></span>        | <span data-ttu-id="a54d1-117">Significato</span><span class="sxs-lookup"><span data-stu-id="a54d1-117">Meaning</span></span>                                                             | <span data-ttu-id="a54d1-118">Significato</span><span class="sxs-lookup"><span data-stu-id="a54d1-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="a54d1-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="a54d1-119">cdaudio</span></span>      | <span data-ttu-id="a54d1-120">info IdentityInfo UPC</span><span class="sxs-lookup"><span data-stu-id="a54d1-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="a54d1-121">product</span><span class="sxs-lookup"><span data-stu-id="a54d1-121">product</span></span>                                             |
| <span data-ttu-id="a54d1-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="a54d1-122">digitalvideo</span></span> | <span data-ttu-id="a54d1-123">audio algorithmaudio qualityfileproductstill algorithmstill Quality</span><span class="sxs-lookup"><span data-stu-id="a54d1-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="a54d1-124">testo qualitywindow algorithmvideo usageversionvideo</span><span class="sxs-lookup"><span data-stu-id="a54d1-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="a54d1-125">overlay</span><span class="sxs-lookup"><span data-stu-id="a54d1-125">overlay</span></span>      | <span data-ttu-id="a54d1-126">fileproduct</span><span class="sxs-lookup"><span data-stu-id="a54d1-126">fileproduct</span></span>                                                         | <span data-ttu-id="a54d1-127">testo finestra</span><span class="sxs-lookup"><span data-stu-id="a54d1-127">window text</span></span>                                         |
| <span data-ttu-id="a54d1-128">sequencer</span><span class="sxs-lookup"><span data-stu-id="a54d1-128">sequencer</span></span>    | <span data-ttu-id="a54d1-129">copyrightfile</span><span class="sxs-lookup"><span data-stu-id="a54d1-129">copyrightfile</span></span>                                                       | <span data-ttu-id="a54d1-130">nameproduct</span><span class="sxs-lookup"><span data-stu-id="a54d1-130">nameproduct</span></span>                                         |
| <span data-ttu-id="a54d1-131">VCR</span><span class="sxs-lookup"><span data-stu-id="a54d1-131">vcr</span></span>          | <span data-ttu-id="a54d1-132">product</span><span class="sxs-lookup"><span data-stu-id="a54d1-132">product</span></span>                                                             | <span data-ttu-id="a54d1-133">version</span><span class="sxs-lookup"><span data-stu-id="a54d1-133">version</span></span>                                             |
| <span data-ttu-id="a54d1-134">videodisk</span><span class="sxs-lookup"><span data-stu-id="a54d1-134">videodisk</span></span>    | <span data-ttu-id="a54d1-135">product</span><span class="sxs-lookup"><span data-stu-id="a54d1-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="a54d1-136">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="a54d1-136">waveaudio</span></span>    | <span data-ttu-id="a54d1-137">FileInput</span><span class="sxs-lookup"><span data-stu-id="a54d1-137">fileinput</span></span>                                                           | <span data-ttu-id="a54d1-138">outputproduct</span><span class="sxs-lookup"><span data-stu-id="a54d1-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="a54d1-139">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszInfoType** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="a54d1-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="a54d1-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a54d1-140">Value</span></span>           | <span data-ttu-id="a54d1-141">Significato</span><span class="sxs-lookup"><span data-stu-id="a54d1-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54d1-142">algoritmo audio</span><span class="sxs-lookup"><span data-stu-id="a54d1-142">audio algorithm</span></span> | <span data-ttu-id="a54d1-143">Restituisce il nome dell'algoritmo di compressione audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="a54d1-144">qualità audio</span><span class="sxs-lookup"><span data-stu-id="a54d1-144">audio quality</span></span>   | <span data-ttu-id="a54d1-145">Restituisce il nome del descrittore di qualità audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="a54d1-146">Questo potrebbe restituire "Unknown" se l'applicazione dispone di parametri impostati su valori specifici che non corrispondono a qualità definite.</span><span class="sxs-lookup"><span data-stu-id="a54d1-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="a54d1-147">copyright</span><span class="sxs-lookup"><span data-stu-id="a54d1-147">copyright</span></span>       | <span data-ttu-id="a54d1-148">Recupera le informazioni sul copyright del file MIDI dall'evento meta del copyright.</span><span class="sxs-lookup"><span data-stu-id="a54d1-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="a54d1-149">file</span><span class="sxs-lookup"><span data-stu-id="a54d1-149">file</span></span>            | <span data-ttu-id="a54d1-150">Recupera il nome del file usato dal dispositivo composto.</span><span class="sxs-lookup"><span data-stu-id="a54d1-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="a54d1-151">Se il dispositivo viene aperto senza un file e non è stato usato il comando [Load](load.md) , viene restituita una stringa null.</span><span class="sxs-lookup"><span data-stu-id="a54d1-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="a54d1-152">identità informazioni</span><span class="sxs-lookup"><span data-stu-id="a54d1-152">info identity</span></span>   | <span data-ttu-id="a54d1-153">Produce un identificatore univoco per il CD audio attualmente caricato nel lettore sottoposto a query.</span><span class="sxs-lookup"><span data-stu-id="a54d1-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="a54d1-154">info UPC</span><span class="sxs-lookup"><span data-stu-id="a54d1-154">info upc</span></span>        | <span data-ttu-id="a54d1-155">Genera il codice di prodotto universale (UPC) codificato in un CD audio.</span><span class="sxs-lookup"><span data-stu-id="a54d1-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="a54d1-156">L'UPC è una stringa di cifre.</span><span class="sxs-lookup"><span data-stu-id="a54d1-156">The UPC is a string of digits.</span></span> <span data-ttu-id="a54d1-157">Potrebbe non essere disponibile per tutti i CDs.</span><span class="sxs-lookup"><span data-stu-id="a54d1-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="a54d1-158">input</span><span class="sxs-lookup"><span data-stu-id="a54d1-158">input</span></span>           | <span data-ttu-id="a54d1-159">Recupera la descrizione del dispositivo di input corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="a54d1-160">Restituisce "None" se non è impostato un dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="a54d1-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="a54d1-161">name</span><span class="sxs-lookup"><span data-stu-id="a54d1-161">name</span></span>            | <span data-ttu-id="a54d1-162">Recupera il nome della sequenza dall'evento meta del nome di sequenza/track.</span><span class="sxs-lookup"><span data-stu-id="a54d1-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="a54d1-163">output</span><span class="sxs-lookup"><span data-stu-id="a54d1-163">output</span></span>          | <span data-ttu-id="a54d1-164">Recupera la descrizione del dispositivo di output corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="a54d1-165">Restituisce "None" se non è impostato un dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="a54d1-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="a54d1-166">product</span><span class="sxs-lookup"><span data-stu-id="a54d1-166">product</span></span>         | <span data-ttu-id="a54d1-167">Recupera una descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a54d1-167">Retrieves a description of the device.</span></span> <span data-ttu-id="a54d1-168">Queste informazioni includono spesso il nome del prodotto e il modello.</span><span class="sxs-lookup"><span data-stu-id="a54d1-168">This information often includes the product name and model.</span></span> <span data-ttu-id="a54d1-169">La lunghezza della stringa sarà pari a 31 caratteri o meno.</span><span class="sxs-lookup"><span data-stu-id="a54d1-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="a54d1-170">algoritmo still</span><span class="sxs-lookup"><span data-stu-id="a54d1-170">still algorithm</span></span> | <span data-ttu-id="a54d1-171">Restituisce il nome dell'algoritmo di compressione delle immagini ancora corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="a54d1-172">qualità ancora</span><span class="sxs-lookup"><span data-stu-id="a54d1-172">still quality</span></span>   | <span data-ttu-id="a54d1-173">Restituisce il nome del descrittore di qualità dell'immagine ancora corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="a54d1-174">Questo potrebbe restituire "Unknown" se l'applicazione dispone di parametri impostati su valori specifici che non corrispondono a qualità definite.</span><span class="sxs-lookup"><span data-stu-id="a54d1-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="a54d1-175">utilizzo</span><span class="sxs-lookup"><span data-stu-id="a54d1-175">usage</span></span>           | <span data-ttu-id="a54d1-176">Restituisce una stringa che descrive le restrizioni di utilizzo che potrebbero essere imposte dal proprietario dei dati visivi o audio nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a54d1-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="a54d1-177">version</span><span class="sxs-lookup"><span data-stu-id="a54d1-177">version</span></span>         | <span data-ttu-id="a54d1-178">Restituisce il livello di rilascio del driver e dell'hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a54d1-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="a54d1-179">algoritmo video</span><span class="sxs-lookup"><span data-stu-id="a54d1-179">video algorithm</span></span> | <span data-ttu-id="a54d1-180">Restituisce il nome dell'algoritmo di compressione video corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="a54d1-181">qualità video</span><span class="sxs-lookup"><span data-stu-id="a54d1-181">video quality</span></span>   | <span data-ttu-id="a54d1-182">Restituisce il nome del descrittore di qualità video corrente.</span><span class="sxs-lookup"><span data-stu-id="a54d1-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="a54d1-183">Questo potrebbe restituire "Unknown" se l'applicazione dispone di parametri impostati su valori specifici che non corrispondono a qualità definite.</span><span class="sxs-lookup"><span data-stu-id="a54d1-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="a54d1-184">testo finestra</span><span class="sxs-lookup"><span data-stu-id="a54d1-184">window text</span></span>     | <span data-ttu-id="a54d1-185">Recupera la didascalia della finestra usata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a54d1-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="a54d1-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a54d1-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a54d1-187">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="a54d1-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a54d1-188">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="a54d1-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="a54d1-189">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a54d1-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a54d1-190">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a54d1-190">Return Value</span></span>

<span data-ttu-id="a54d1-191">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a54d1-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="a54d1-192">Esempio</span><span class="sxs-lookup"><span data-stu-id="a54d1-192">Examples</span></span>

<span data-ttu-id="a54d1-193">Il comando che segue recupera una descrizione dell'hardware associato al dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="a54d1-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="a54d1-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a54d1-194">Requirements</span></span>



| <span data-ttu-id="a54d1-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="a54d1-195">Requirement</span></span> | <span data-ttu-id="a54d1-196">Valore</span><span class="sxs-lookup"><span data-stu-id="a54d1-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a54d1-197">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a54d1-197">Minimum supported client</span></span><br/> | <span data-ttu-id="a54d1-198">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a54d1-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a54d1-199">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a54d1-199">Minimum supported server</span></span><br/> | <span data-ttu-id="a54d1-200">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a54d1-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a54d1-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a54d1-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54d1-202">MCI</span><span class="sxs-lookup"><span data-stu-id="a54d1-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a54d1-203">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="a54d1-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a54d1-204">carico</span><span class="sxs-lookup"><span data-stu-id="a54d1-204">load</span></span>](load.md)
</dt> </dl>

 


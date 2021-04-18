---
title: Salva comando
description: Il comando Save Salva un file MCI. Video-overlay e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo supportano.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Salva comando di Windows
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301012"
---
# <a name="save-command"></a><span data-ttu-id="f2218-106">Salva comando</span><span class="sxs-lookup"><span data-stu-id="f2218-106">save command</span></span>

<span data-ttu-id="f2218-107">Il comando Save Salva un file MCI.</span><span class="sxs-lookup"><span data-stu-id="f2218-107">The save command saves an MCI file.</span></span> <span data-ttu-id="f2218-108">Video-overlay e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="f2218-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="f2218-109">Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="f2218-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="f2218-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f2218-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f2218-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2218-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2218-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f2218-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f2218-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f2218-113">Identifier of an MCI device.</span></span> <span data-ttu-id="f2218-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="f2218-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f2218-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span><span class="sxs-lookup"><span data-stu-id="f2218-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="f2218-116">Flag che specifica il nome del file salvato e, facoltativamente, flag aggiuntivi che modificano l'operazione di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="f2218-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="f2218-117">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Salva** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="f2218-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="f2218-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f2218-118">Value</span></span>        | <span data-ttu-id="f2218-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f2218-119">Meaning</span></span>              | <span data-ttu-id="f2218-120">Significato</span><span class="sxs-lookup"><span data-stu-id="f2218-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="f2218-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f2218-121">digitalvideo</span></span> | <span data-ttu-id="f2218-122">Interrompi al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="f2218-122">abort at *rectangle*</span></span> | <span data-ttu-id="f2218-123">*nome file* keepreserve</span><span class="sxs-lookup"><span data-stu-id="f2218-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="f2218-124">overlay</span><span class="sxs-lookup"><span data-stu-id="f2218-124">overlay</span></span>      | <span data-ttu-id="f2218-125">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="f2218-125">at *rectangle*</span></span>       | <span data-ttu-id="f2218-126">*filename*</span><span class="sxs-lookup"><span data-stu-id="f2218-126">*filename*</span></span>            |
| <span data-ttu-id="f2218-127">sequencer</span><span class="sxs-lookup"><span data-stu-id="f2218-127">sequencer</span></span>    | <span data-ttu-id="f2218-128">*filename*</span><span class="sxs-lookup"><span data-stu-id="f2218-128">*filename*</span></span>           |                       |
| <span data-ttu-id="f2218-129">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="f2218-129">waveaudio</span></span>    | <span data-ttu-id="f2218-130">*filename*</span><span class="sxs-lookup"><span data-stu-id="f2218-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="f2218-131">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszFileName** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="f2218-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="f2218-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f2218-132">Value</span></span>          | <span data-ttu-id="f2218-133">Significato</span><span class="sxs-lookup"><span data-stu-id="f2218-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2218-134">abort</span><span class="sxs-lookup"><span data-stu-id="f2218-134">abort</span></span>          | <span data-ttu-id="f2218-135">Arresta un'operazione di **salvataggio** in corso.</span><span class="sxs-lookup"><span data-stu-id="f2218-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="f2218-136">Se utilizzato, deve essere l'unico elemento presente.</span><span class="sxs-lookup"><span data-stu-id="f2218-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f2218-137">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="f2218-137">at *rectangle*</span></span> | <span data-ttu-id="f2218-138">Specifica un rettangolo relativo all'origine del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="f2218-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="f2218-139">Il *rettangolo* viene specificato come *X1 Y1 Y1 2*.</span><span class="sxs-lookup"><span data-stu-id="f2218-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="f2218-140">Le coordinate *X1 Y1* specificano l'angolo superiore sinistro e le coordinate *X2 Y2* specificano la larghezza e l'altezza. Per i dispositivi digitali video, il comando [Acquisisci](capture.md) viene usato per acquisire il contenuto del buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="f2218-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="f2218-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="f2218-141">*filename*</span></span>     | <span data-ttu-id="f2218-142">Specifica il nome file da assegnare al file di dati.</span><span class="sxs-lookup"><span data-stu-id="f2218-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="f2218-143">Se non si specifica un percorso, il file verrà inserito sul disco e nella directory specificata in precedenza nel comando di [riserva](reserve.md) esplicito o implicito.</span><span class="sxs-lookup"><span data-stu-id="f2218-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="f2218-144">Se **Reserve** non è stato emesso, l'unità e la directory predefinite sono quelle associate all'attività dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2218-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="f2218-145">Se viene specificato un percorso, è possibile che il dispositivo lo richieda nell'unità disco specificata dalla **riserva** esplicita o implicita.</span><span class="sxs-lookup"><span data-stu-id="f2218-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="f2218-146">Questo flag è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f2218-146">This flag is required.</span></span> |
| <span data-ttu-id="f2218-147">keepreserve</span><span class="sxs-lookup"><span data-stu-id="f2218-147">keepreserve</span></span>    | <span data-ttu-id="f2218-148">Specifica che lo spazio su disco inutilizzato rimanente dal comando di **riserva** originale non viene deallocato.</span><span class="sxs-lookup"><span data-stu-id="f2218-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="f2218-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f2218-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f2218-150">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="f2218-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f2218-151">Per i dispositivi digitali video e VCR è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="f2218-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f2218-152">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f2218-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2218-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2218-153">Return Value</span></span>

<span data-ttu-id="f2218-154">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="f2218-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2218-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2218-155">Remarks</span></span>

<span data-ttu-id="f2218-156">La variabile *filename* è obbligatoria se il dispositivo è stato aperto con l'identificatore del dispositivo "nuovo".</span><span class="sxs-lookup"><span data-stu-id="f2218-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="f2218-157">Esempio</span><span class="sxs-lookup"><span data-stu-id="f2218-157">Examples</span></span>

<span data-ttu-id="f2218-158">Il seguente comando Salva l'intero buffer video in un file denominato VCAPFILE. TGA.</span><span class="sxs-lookup"><span data-stu-id="f2218-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="f2218-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2218-159">Requirements</span></span>



| <span data-ttu-id="f2218-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2218-160">Requirement</span></span> | <span data-ttu-id="f2218-161">Valore</span><span class="sxs-lookup"><span data-stu-id="f2218-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f2218-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2218-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f2218-163">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2218-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f2218-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2218-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f2218-165">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2218-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f2218-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2218-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2218-167">MCI</span><span class="sxs-lookup"><span data-stu-id="f2218-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f2218-168">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="f2218-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f2218-169">catturare</span><span class="sxs-lookup"><span data-stu-id="f2218-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="f2218-170">riserva</span><span class="sxs-lookup"><span data-stu-id="f2218-170">reserve</span></span>](reserve.md)
</dt> </dl>

 


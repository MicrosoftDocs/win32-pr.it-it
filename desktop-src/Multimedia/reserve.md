---
title: comando Reserve
description: Il comando Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del dispositivo. I dispositivi digitali video riconoscono questo comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando riserva Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963783"
---
# <a name="reserve-command"></a><span data-ttu-id="ce93c-105">comando Reserve</span><span class="sxs-lookup"><span data-stu-id="ce93c-105">reserve command</span></span>

<span data-ttu-id="ce93c-106">Il comando Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce93c-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="ce93c-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="ce93c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ce93c-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ce93c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ce93c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce93c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce93c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ce93c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ce93c-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ce93c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="ce93c-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="ce93c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ce93c-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span><span class="sxs-lookup"><span data-stu-id="ce93c-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="ce93c-114">Uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce93c-114">One or more of the following flags.</span></span>



| <span data-ttu-id="ce93c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ce93c-115">Value</span></span>           | <span data-ttu-id="ce93c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="ce93c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce93c-117">in *percorso*</span><span class="sxs-lookup"><span data-stu-id="ce93c-117">in *path*</span></span>       | <span data-ttu-id="ce93c-118">Specifica l'unità e il percorso della directory, ma non il nome, di un file temporaneo usato per conservare i dati registrati.</span><span class="sxs-lookup"><span data-stu-id="ce93c-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="ce93c-119">Il nome di questo file è specificato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce93c-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="ce93c-120">Il file temporaneo viene eliminato quando il dispositivo viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="ce93c-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="ce93c-121">Se questo flag viene omesso, il dispositivo specifica il percorso dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="ce93c-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ce93c-122">*durata* dimensioni</span><span class="sxs-lookup"><span data-stu-id="ce93c-122">size *duration*</span></span> | <span data-ttu-id="ce93c-123">Specifica la quantità approssimativa di spazio su disco da riservare nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce93c-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="ce93c-124">Il valore *Duration* viene specificato nel formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ce93c-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="ce93c-125">Il dispositivo basa la stima dello spazio su disco richiesto nei parametri seguenti: il tempo richiesto, il formato del file, l'algoritmo di compressione video e audio e i valori di qualità di compressione in vigore.</span><span class="sxs-lookup"><span data-stu-id="ce93c-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="ce93c-126">Se [sevideo](setvideo.md) "record" è disattivato, lo spazio è riservato solo per l'audio.</span><span class="sxs-lookup"><span data-stu-id="ce93c-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="ce93c-127">Se il [file](setaudio.md) "record" è disattivato, lo spazio è riservato solo per i video.</span><span class="sxs-lookup"><span data-stu-id="ce93c-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="ce93c-128">Se entrambi sono "off" o se *Duration* è zero, nessuno spazio viene riservato e lo spazio riservato esistente viene deallocato.</span><span class="sxs-lookup"><span data-stu-id="ce93c-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="ce93c-129">Se questo flag viene omesso, il dispositivo userà un valore predefinito definito dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce93c-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ce93c-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="ce93c-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ce93c-131">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="ce93c-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="ce93c-132">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ce93c-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce93c-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce93c-133">Return Value</span></span>

<span data-ttu-id="ce93c-134">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ce93c-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce93c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce93c-135">Remarks</span></span>

<span data-ttu-id="ce93c-136">Se necessario, i comandi [record](record.md) o [Save](save.md) successivi usano lo spazio riservato da questo comando.</span><span class="sxs-lookup"><span data-stu-id="ce93c-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="ce93c-137">Se l'area di lavoro contiene dati non salvati, i dati andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="ce93c-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="ce93c-138">Alcuni dispositivi non richiedono la riserva e lo ignorano.</span><span class="sxs-lookup"><span data-stu-id="ce93c-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="ce93c-139">Se lo spazio su disco non è riservato prima della registrazione, il comando record esegue una riserva implicita con i flag predefiniti specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce93c-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="ce93c-140">Utilizzare un comando di riserva esplicito se si desidera un migliore controllo del momento in cui si verifica l'allocazione dei dischi, il controllo della quantità di spazio allocato e il controllo della posizione di allocazione dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="ce93c-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="ce93c-141">L'applicazione può modificare la quantità e la posizione dello spazio su disco precedentemente riservato con i comandi di riserva successivi.</span><span class="sxs-lookup"><span data-stu-id="ce93c-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="ce93c-142">Qualsiasi spazio su disco allocato e ancora inutilizzato non viene deallocato fino al salvataggio dei dati registrati o fino alla chiusura dell'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce93c-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce93c-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce93c-143">Requirements</span></span>



| <span data-ttu-id="ce93c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce93c-144">Requirement</span></span> | <span data-ttu-id="ce93c-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ce93c-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ce93c-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce93c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ce93c-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce93c-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ce93c-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce93c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ce93c-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce93c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ce93c-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce93c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce93c-151">MCI</span><span class="sxs-lookup"><span data-stu-id="ce93c-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ce93c-152">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="ce93c-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="ce93c-153">record</span><span class="sxs-lookup"><span data-stu-id="ce93c-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="ce93c-154">salvataggio</span><span class="sxs-lookup"><span data-stu-id="ce93c-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="ce93c-155">SetAudio</span><span class="sxs-lookup"><span data-stu-id="ce93c-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="ce93c-156">video</span><span class="sxs-lookup"><span data-stu-id="ce93c-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 


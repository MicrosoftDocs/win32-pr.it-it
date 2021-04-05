---
title: comando di monitoraggio
description: Il comando di monitoraggio specifica l'origine della presentazione. L'origine della presentazione predefinita è l'area di lavoro. Il passaggio all'origine della presentazione commuta tutti i flussi audio e video nell'origine. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- monitoraggio del comando di Windows Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741426"
---
# <a name="monitor-command"></a><span data-ttu-id="3d634-106">comando di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="3d634-106">monitor command</span></span>

<span data-ttu-id="3d634-107">Il comando di monitoraggio specifica l'origine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="3d634-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="3d634-108">L'origine della presentazione predefinita è l'area di lavoro. Il passaggio all'origine della presentazione commuta tutti i flussi audio e video nell'origine.</span><span class="sxs-lookup"><span data-stu-id="3d634-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="3d634-109">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="3d634-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="3d634-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3d634-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3d634-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d634-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d634-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3d634-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3d634-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3d634-113">Identifier of an MCI device.</span></span> <span data-ttu-id="3d634-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="3d634-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3d634-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span><span class="sxs-lookup"><span data-stu-id="3d634-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="3d634-116">Uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d634-116">One or more of the following flags.</span></span>



| <span data-ttu-id="3d634-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3d634-117">Value</span></span>           | <span data-ttu-id="3d634-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3d634-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d634-119">file</span><span class="sxs-lookup"><span data-stu-id="3d634-119">file</span></span>            | <span data-ttu-id="3d634-120">Specifica che l'area di lavoro è l'origine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="3d634-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="3d634-121">Si tratta dell'origine predefinita.</span><span class="sxs-lookup"><span data-stu-id="3d634-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3d634-122">input</span><span class="sxs-lookup"><span data-stu-id="3d634-122">input</span></span>           | <span data-ttu-id="3d634-123">Specifica che l'input esterno è l'origine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="3d634-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="3d634-124">Se è in corso un comando [Play](play.md) , viene prima sospesa.</span><span class="sxs-lookup"><span data-stu-id="3d634-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="3d634-125">Se [sevideo](setvideo.md) è "on", questo flag Visualizza una finestra nascosta predefinita.</span><span class="sxs-lookup"><span data-stu-id="3d634-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="3d634-126">I dispositivi potrebbero limitare le operazioni che possono essere eseguite da altre istanze del dispositivo durante il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="3d634-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3d634-127">metodo *Metodo*</span><span class="sxs-lookup"><span data-stu-id="3d634-127">method *method*</span></span> | <span data-ttu-id="3d634-128">Se usato con il **monitoraggio** "input", questo flag seleziona il metodo di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="3d634-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="3d634-129">Il *Metodo* può essere "pre", "post" o "Direct".</span><span class="sxs-lookup"><span data-stu-id="3d634-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="3d634-130">Il monitoraggio diretto richiede che il dispositivo sia configurato per una qualità di visualizzazione ottimale durante il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="3d634-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="3d634-131">Il metodo di monitoraggio diretto potrebbe non essere compatibile con la registrazione video in movimento. Pre-e post-monitoraggio consentono la registrazione video in movimento.</span><span class="sxs-lookup"><span data-stu-id="3d634-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="3d634-132">Il pre-monitoraggio Mostra l'input esterno prima della compressione, mentre il post-monitoraggio Mostra l'input esterno dopo la compressione.</span><span class="sxs-lookup"><span data-stu-id="3d634-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="3d634-133">In genere, diversi metodi di monitoraggio hanno implicazioni hardware diverse.</span><span class="sxs-lookup"><span data-stu-id="3d634-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="3d634-134">Il metodo di monitoraggio predefinito è selezionato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d634-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3d634-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3d634-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3d634-136">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="3d634-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="3d634-137">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3d634-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d634-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d634-138">Return Value</span></span>

<span data-ttu-id="3d634-139">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3d634-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d634-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d634-140">Remarks</span></span>

<span data-ttu-id="3d634-141">L'origine della presentazione passa automaticamente all'area di lavoro dopo un comando [Play](play.md), [Step](step.md), [pause](pause.md), [cue](cue.md) "output" o [Seek](seek.md) .</span><span class="sxs-lookup"><span data-stu-id="3d634-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="3d634-142">Il comando [record](record.md) non cambia automaticamente le origini di presentazione, che consente all'applicazione di non visualizzare video mentre è in corso la registrazione.</span><span class="sxs-lookup"><span data-stu-id="3d634-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d634-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d634-143">Requirements</span></span>



| <span data-ttu-id="3d634-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d634-144">Requirement</span></span> | <span data-ttu-id="3d634-145">Valore</span><span class="sxs-lookup"><span data-stu-id="3d634-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3d634-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d634-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3d634-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d634-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d634-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d634-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3d634-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d634-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3d634-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d634-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d634-151">MCI</span><span class="sxs-lookup"><span data-stu-id="3d634-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3d634-152">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="3d634-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="3d634-153">segnale</span><span class="sxs-lookup"><span data-stu-id="3d634-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="3d634-154">pause</span><span class="sxs-lookup"><span data-stu-id="3d634-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="3d634-155">Play</span><span class="sxs-lookup"><span data-stu-id="3d634-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="3d634-156">record</span><span class="sxs-lookup"><span data-stu-id="3d634-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="3d634-157">cercare</span><span class="sxs-lookup"><span data-stu-id="3d634-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="3d634-158">passo</span><span class="sxs-lookup"><span data-stu-id="3d634-158">step</span></span>](step.md)
</dt> </dl>

 


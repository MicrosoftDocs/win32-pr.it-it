---
title: comando Incolla
description: Il comando Incolla copia il contenuto degli Appunti nell'area di lavoro. I dispositivi digitali video riconoscono questo comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- comando Incolla Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048050"
---
# <a name="paste-command"></a><span data-ttu-id="6142c-105">comando Incolla</span><span class="sxs-lookup"><span data-stu-id="6142c-105">paste command</span></span>

<span data-ttu-id="6142c-106">Il comando Incolla copia il contenuto degli Appunti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6142c-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="6142c-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="6142c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6142c-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6142c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6142c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6142c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6142c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6142c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6142c-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6142c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6142c-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="6142c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6142c-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="6142c-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="6142c-114">Uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="6142c-114">One or more of the following flags.</span></span>



| <span data-ttu-id="6142c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6142c-115">Value</span></span>                 | <span data-ttu-id="6142c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6142c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6142c-117">al *rettangolo*</span><span class="sxs-lookup"><span data-stu-id="6142c-117">at *rectangle*</span></span>        | <span data-ttu-id="6142c-118">Specifica la posizione all'interno del frame in cui vengono incollati i dati.</span><span class="sxs-lookup"><span data-stu-id="6142c-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="6142c-119">L'angolo superiore sinistro del *rettangolo* corrisponde all'angolo superiore sinistro dei dati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="6142c-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="6142c-120">Se il rettangolo ha una dimensione diversa da zero in X o Y, il contenuto degli Appunti viene ridimensionato in tali dimensioni quando vengono incollate nel frame.</span><span class="sxs-lookup"><span data-stu-id="6142c-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="6142c-121">Se omesso, il *rettangolo* viene impostato per impostazione predefinita sull'intero frame.</span><span class="sxs-lookup"><span data-stu-id="6142c-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="6142c-122">Se questo flag viene specificato in modalità "Insert" (impostazione predefinita), qualsiasi area esterna al rettangolo viene disegnata con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="6142c-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="6142c-123">*flusso* del flusso audio</span><span class="sxs-lookup"><span data-stu-id="6142c-123">audio stream *stream*</span></span> | <span data-ttu-id="6142c-124">Specifica il flusso audio nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="6142c-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="6142c-125">Se negli Appunti è presente un solo flusso audio, i dati audio vengono incollati nel *flusso* designato.</span><span class="sxs-lookup"><span data-stu-id="6142c-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="6142c-126">Se negli Appunti è presente più di un flusso audio, il *flusso* indica il numero iniziale per le sequenze di flusso.</span><span class="sxs-lookup"><span data-stu-id="6142c-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="6142c-127">Se si usa questo flag e si vuole anche incollare il video, è necessario usare anche il flag "flusso video".</span><span class="sxs-lookup"><span data-stu-id="6142c-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="6142c-128">Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati e mantengono i numeri di flusso originali.</span><span class="sxs-lookup"><span data-stu-id="6142c-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="6142c-129">insert</span><span class="sxs-lookup"><span data-stu-id="6142c-129">insert</span></span>                | <span data-ttu-id="6142c-130">Specifica che i dati vengono inseriti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6142c-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="6142c-131">Tutti i dati successivi al punto di inserimento vengono spostati nell'area di lavoro per fare spazio.</span><span class="sxs-lookup"><span data-stu-id="6142c-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="6142c-132">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6142c-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6142c-133">overwrite</span><span class="sxs-lookup"><span data-stu-id="6142c-133">overwrite</span></span>             | <span data-ttu-id="6142c-134">Specifica che i dati vengono copiati nell'area di lavoro scrivendo su tutti i dati esistenti dopo il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="6142c-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="6142c-135">I flag "Insert" e "overwrite" influiscono sul fatto che i frame vengano eliminati o spostati durante l'operazione Incolla, non su come i dati vengono incollati all'interno di ogni frame.</span><span class="sxs-lookup"><span data-stu-id="6142c-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="6142c-136">*posizione*</span><span class="sxs-lookup"><span data-stu-id="6142c-136">to *position*</span></span>         | <span data-ttu-id="6142c-137">Specifica la posizione nell'area di lavoro in cui vengono incollati i dati.</span><span class="sxs-lookup"><span data-stu-id="6142c-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="6142c-138">Se omesso, il valore predefinito è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6142c-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6142c-139">*flusso* del flusso video</span><span class="sxs-lookup"><span data-stu-id="6142c-139">video stream *stream*</span></span> | <span data-ttu-id="6142c-140">Specifica il flusso video nell'area di lavoro interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="6142c-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="6142c-141">Se negli Appunti è presente un solo flusso video, i dati video vengono incollati nel *flusso* designato.</span><span class="sxs-lookup"><span data-stu-id="6142c-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="6142c-142">Se negli Appunti è presente più di un flusso video, il *flusso* indica il numero iniziale per le sequenze di flusso.</span><span class="sxs-lookup"><span data-stu-id="6142c-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="6142c-143">Se si usa questo flag e si vuole anche incollare audio, è necessario usare anche il flag "flusso audio".</span><span class="sxs-lookup"><span data-stu-id="6142c-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="6142c-144">Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati e mantengono i numeri di flusso originali.</span><span class="sxs-lookup"><span data-stu-id="6142c-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="6142c-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6142c-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6142c-146">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="6142c-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6142c-147">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6142c-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6142c-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6142c-148">Return Value</span></span>

<span data-ttu-id="6142c-149">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="6142c-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6142c-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="6142c-150">Remarks</span></span>

<span data-ttu-id="6142c-151">Nessun segnale presente nei dati copiati dagli Appunti.</span><span class="sxs-lookup"><span data-stu-id="6142c-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="6142c-152">La modifica diventa permanente solo quando i dati vengono salvati in modo esplicito; Tuttavia, la riproduzione funge da se i dati sono stati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="6142c-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="6142c-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6142c-153">Requirements</span></span>



| <span data-ttu-id="6142c-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="6142c-154">Requirement</span></span> | <span data-ttu-id="6142c-155">Valore</span><span class="sxs-lookup"><span data-stu-id="6142c-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6142c-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6142c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="6142c-157">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6142c-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6142c-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6142c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="6142c-159">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6142c-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6142c-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6142c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6142c-161">MCI</span><span class="sxs-lookup"><span data-stu-id="6142c-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6142c-162">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="6142c-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 


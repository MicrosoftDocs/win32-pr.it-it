---
title: Comando MCI_PASTE (mmsystem. h)
description: Il \_ comando MCI paste Incolla i dati dagli Appunti in un file. I dispositivi digitali video riconoscono questo comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Comando MCI_PASTE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739826"
---
# <a name="mci_paste-command"></a><span data-ttu-id="d8ae0-105">\_Comando di Incolla MCI</span><span class="sxs-lookup"><span data-stu-id="d8ae0-105">MCI\_PASTE command</span></span>

<span data-ttu-id="d8ae0-106">Il \_ comando MCI paste Incolla i dati dagli Appunti in un file.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="d8ae0-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d8ae0-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="d8ae0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8ae0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ae0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d8ae0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d8ae0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d8ae0-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d8ae0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span><span class="sxs-lookup"><span data-stu-id="d8ae0-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-116">Puntatore a una [**struttura \_ \_ \_ parametri DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ae0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8ae0-117">Return Value</span></span>

<span data-ttu-id="d8ae0-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8ae0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8ae0-119">Remarks</span></span>

<span data-ttu-id="d8ae0-120">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="d8ae0-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="d8ae0-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_Incolla DGV \_ MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="d8ae0-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-122">Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d8ae0-123">I primi due valori del rettangolo specificano il punto all'interno del frame in cui inserire le informazioni degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="d8ae0-124">Se l'altezza e la larghezza del rettangolo sono diversi da zero, il contenuto degli Appunti viene ridimensionato a tali dimensioni quando vengono incollate nel frame.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="d8ae0-125">Se il flag viene omesso, \_ l'impostazione predefinita di MCI paste viene impostata sull'intero rettangolo del frame.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>\_ \_ \_ flusso audio incolla DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d8ae0-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-127">Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d8ae0-128">Se negli Appunti è presente un solo flusso audio, i dati audio vengono incollati nel flusso designato.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="d8ae0-129">Se negli Appunti è presente più di un flusso audio, il flusso indica il numero iniziale per le sequenze di flusso.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d8ae0-130">Se si usa questo flag e si vuole anche incollare il video, è necessario usare anche il \_ \_ flag di flusso del video DGV paste MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="d8ae0-131">Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati a partire dal primo flusso audio e video.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="d8ae0-132">Ogni flusso incollato mantiene il numero di flusso originale.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_inserimento di DGV per MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="d8ae0-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-134">I dati degli Appunti devono essere inseriti nell'area di lavoro esistente in corrispondenza della posizione specificata dall'oggetto MCI \_ da contrassegnare.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="d8ae0-135">Tutti i dati esistenti dopo il punto di inserimento vengono spostati nell'area di lavoro per creare spazio.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="d8ae0-136">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>\_sovrascrittura \_ Incolla DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="d8ae0-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-138">I dati degli Appunti devono sostituire i dati già presenti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="d8ae0-139">I dati dell'area di lavoro sostituiti seguono il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_ \_ \_ flusso video incolla DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d8ae0-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-141">Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d8ae0-142">Se negli Appunti è presente un solo flusso video, i dati video vengono incollati nel flusso designato.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="d8ae0-143">Se negli Appunti è presente più di un flusso video, il flusso indica il numero iniziale per le sequenze di flusso.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d8ae0-144">Se si usa questo flag e si vuole anche incollare l'audio, è necessario usare anche il \_ \_ flag di \_ flusso audio DGV incolla MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="d8ae0-145">Se non viene specificato alcun flag, tutti i flussi audio e video vengono incollati a partire dal primo flusso audio e video.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="d8ae0-146">Ogni flusso incollato mantiene il numero di flusso originale.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="d8ae0-147"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="d8ae0-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d8ae0-148">Un valore di posizione è incluso nel membro **dwTo** della struttura identificata da *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="d8ae0-149">Il valore position specifica la posizione in cui iniziare a incollare i dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="d8ae0-150">Se questo flag viene omesso, per impostazione predefinita la posizione corrisponde alla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8ae0-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8ae0-151">Requirements</span></span>



| <span data-ttu-id="d8ae0-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8ae0-152">Requirement</span></span> | <span data-ttu-id="d8ae0-153">Valore</span><span class="sxs-lookup"><span data-stu-id="d8ae0-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ae0-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8ae0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ae0-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8ae0-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8ae0-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8ae0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ae0-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8ae0-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8ae0-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8ae0-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8ae0-159"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8ae0-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ae0-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8ae0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ae0-161">MCI</span><span class="sxs-lookup"><span data-stu-id="d8ae0-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d8ae0-162">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="d8ae0-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


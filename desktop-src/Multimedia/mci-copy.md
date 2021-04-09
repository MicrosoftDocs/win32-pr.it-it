---
title: Comando MCI_COPY (mmsystem. h)
description: Il \_ comando di copia MCI copia i dati negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- Comando MCI_COPY Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964280"
---
# <a name="mci_copy-command"></a><span data-ttu-id="7b7b3-105">\_Comando di copia MCI</span><span class="sxs-lookup"><span data-stu-id="7b7b3-105">MCI\_COPY command</span></span>

<span data-ttu-id="7b7b3-106">Il \_ comando di copia MCI copia i dati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="7b7b3-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7b7b3-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="7b7b3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b7b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b7b3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7b7b3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7b7b3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7b7b3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7b7b3-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="7b7b3-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7b7b3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b7b3-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span><span class="sxs-lookup"><span data-stu-id="7b7b3-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-116">Puntatore a una struttura di [**\_ \_ Copia \_ parametri di DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .</span><span class="sxs-lookup"><span data-stu-id="7b7b3-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b7b3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b7b3-117">Return Value</span></span>

<span data-ttu-id="7b7b3-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b7b3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b7b3-119">Remarks</span></span>

<span data-ttu-id="7b7b3-120">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="7b7b3-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="7b7b3-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_ \_ copia di DGV MCI \_ in</span><span class="sxs-lookup"><span data-stu-id="7b7b3-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-122">Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="7b7b3-123">Il rettangolo specifica la parte di ogni fotogramma da copiare.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="7b7b3-124">Se il flag viene omesso, \_ la copia di MCI copia l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="7b7b3-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_ \_ \_ flusso audio copia DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="7b7b3-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-126">Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="7b7b3-127">Se si usa questo flag e si vuole anche copiare il video, è necessario usare anche il \_ flag di flusso del video DGV della \_ copia MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b7b3-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="7b7b3-128">Se non viene specificato alcun flag, vengono copiati i dati provenienti da tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="7b7b3-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_ \_ \_ flusso video copia DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="7b7b3-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-130">Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="7b7b3-131">Se si usa questo flag e si vuole anche copiare l'audio, è necessario usare anche il \_ \_ flag del \_ flusso audio DGV di copia MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="7b7b3-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="7b7b3-132">Se non viene specificato alcun flag, vengono copiati i dati provenienti da tutti i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="7b7b3-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="7b7b3-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-134">Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="7b7b3-135">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="7b7b3-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="7b7b3-136"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="7b7b3-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="7b7b3-137">Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="7b7b3-138">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del \_ comando set di MCI.</span><span class="sxs-lookup"><span data-stu-id="7b7b3-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b7b3-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b7b3-139">Requirements</span></span>



| <span data-ttu-id="7b7b3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b7b3-140">Requirement</span></span> | <span data-ttu-id="7b7b3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="7b7b3-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7b3-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b7b3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7b7b3-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b7b3-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7b7b3-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b7b3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7b7b3-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b7b3-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7b7b3-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b7b3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b7b3-147"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b7b3-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b7b3-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b7b3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b7b3-149">MCI</span><span class="sxs-lookup"><span data-stu-id="7b7b3-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7b7b3-150">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="7b7b3-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


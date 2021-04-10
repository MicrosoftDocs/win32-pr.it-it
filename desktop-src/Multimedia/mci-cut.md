---
title: Comando MCI_CUT (mmsystem. h)
description: Il \_ comando MCI Cut rimuove i dati dal file e li copia negli Appunti. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Comando MCI_CUT Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964530"
---
# <a name="mci_cut-command"></a><span data-ttu-id="8af7b-105">\_Comando taglia MCI</span><span class="sxs-lookup"><span data-stu-id="8af7b-105">MCI\_CUT command</span></span>

<span data-ttu-id="8af7b-106">Il \_ comando MCI Cut rimuove i dati dal file e li copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="8af7b-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="8af7b-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="8af7b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8af7b-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="8af7b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="8af7b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8af7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af7b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8af7b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="8af7b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8af7b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8af7b-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="8af7b-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8af7b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span><span class="sxs-lookup"><span data-stu-id="8af7b-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-116">Puntatore a una [**struttura \_ \_ \_ parametri DGV Cut di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .</span><span class="sxs-lookup"><span data-stu-id="8af7b-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af7b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8af7b-117">Return Value</span></span>

<span data-ttu-id="8af7b-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="8af7b-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af7b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8af7b-119">Remarks</span></span>

<span data-ttu-id="8af7b-120">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="8af7b-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="8af7b-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_DGV \_ di MCI Cut \_</span><span class="sxs-lookup"><span data-stu-id="8af7b-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-122">Un rettangolo è incluso nel membro **RC** della struttura identificata da *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="8af7b-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="8af7b-123">Il rettangolo specifica la parte di ogni fotogramma da tagliare.</span><span class="sxs-lookup"><span data-stu-id="8af7b-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="8af7b-124">Se il flag viene omesso, \_ il taglio MCI taglia l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="8af7b-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_ \_ \_ flusso audio taglia DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="8af7b-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-126">Un numero di flusso audio è incluso nel membro **dwAudioStream** della struttura identificata da *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="8af7b-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="8af7b-127">Se si usa questo flag e si vuole anche tagliare il video, è necessario usare anche il \_ flag di flusso del video di MCI DGV \_ Cut \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8af7b-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="8af7b-128">Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono tagliati.</span><span class="sxs-lookup"><span data-stu-id="8af7b-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_ \_ \_ flusso video DGV di MCI Cut \_</span><span class="sxs-lookup"><span data-stu-id="8af7b-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-130">Un numero di flusso video è incluso nel membro **dwVideoStream** della struttura identificata da *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="8af7b-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="8af7b-131">Se si usa questo flag e si vuole anche tagliare audio, è necessario usare anche il \_ flag del \_ flusso audio DGV Cut MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8af7b-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="8af7b-132">Se non viene specificato alcun flag, i dati provenienti da tutti i flussi audio e video vengono tagliati.</span><span class="sxs-lookup"><span data-stu-id="8af7b-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ da</span><span class="sxs-lookup"><span data-stu-id="8af7b-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-134">Una posizione iniziale è inclusa nel membro **dwFrom** della struttura identificata da *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="8af7b-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="8af7b-135">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ flag di formato dell'ora del set \_ di MCI del comando [ \_ set di MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="8af7b-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="8af7b-136"><span id="MCI_TO"></span><span id="mci_to"></span>\_da MCI a</span><span class="sxs-lookup"><span data-stu-id="8af7b-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="8af7b-137">Una posizione finale è inclusa nel membro **dwTo** della struttura identificata da *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="8af7b-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="8af7b-138">Le unità assegnate ai valori di posizione vengono specificate con il \_ \_ \_ flag di formato dell'ora di set MCI del set di MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8af7b-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8af7b-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8af7b-139">Requirements</span></span>



| <span data-ttu-id="8af7b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8af7b-140">Requirement</span></span> | <span data-ttu-id="8af7b-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8af7b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af7b-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8af7b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8af7b-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8af7b-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8af7b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8af7b-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8af7b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8af7b-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8af7b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af7b-147"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8af7b-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af7b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8af7b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af7b-149">MCI</span><span class="sxs-lookup"><span data-stu-id="8af7b-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8af7b-150">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="8af7b-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


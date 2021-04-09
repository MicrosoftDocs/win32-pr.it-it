---
title: Comando MCI_STEP (mmsystem. h)
description: Il \_ comando del passaggio MCI segue il lettore di uno o più frame. I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Comando MCI_STEP Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118951"
---
# <a name="mci_step-command"></a><span data-ttu-id="a1dee-105">\_Comando del passaggio MCI</span><span class="sxs-lookup"><span data-stu-id="a1dee-105">MCI\_STEP command</span></span>

<span data-ttu-id="a1dee-106">Il \_ comando del passaggio MCI segue il lettore di uno o più frame.</span><span class="sxs-lookup"><span data-stu-id="a1dee-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="a1dee-107">I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="a1dee-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="a1dee-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a1dee-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="a1dee-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1dee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1dee-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a1dee-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="a1dee-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a1dee-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a1dee-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a1dee-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a1dee-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a1dee-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1dee-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span><span class="sxs-lookup"><span data-stu-id="a1dee-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dee-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="a1dee-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1dee-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1dee-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1dee-118">Return Value</span></span>

<span data-ttu-id="a1dee-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="a1dee-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1dee-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1dee-120">Remarks</span></span>

<span data-ttu-id="a1dee-121">Questo comando supporta i dispositivi che restituiscono **true** al \_ GETDEVCAPS MCI \_ con \_ il flag video del comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dee-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="a1dee-122">Con il tipo di dispositivo **digitalvideo** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1dee-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a1dee-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_ \_ frame passaggio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a1dee-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-124">Il membro **dwFrames** della struttura identificata da *lpStep* specifica il numero di frame da anticipare prima di visualizzare un'altra immagine.</span><span class="sxs-lookup"><span data-stu-id="a1dee-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="a1dee-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>DGV di MCI- \_ \_ passaggio \_ inverso</span><span class="sxs-lookup"><span data-stu-id="a1dee-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-126">Passaggi in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="a1dee-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="a1dee-127">Per i dispositivi digitali video, il parametro *lpStep* punta a una [**struttura \_ DGV \_ Step \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .</span><span class="sxs-lookup"><span data-stu-id="a1dee-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="a1dee-128">Con il tipo di dispositivo **VCR** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1dee-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a1dee-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_ \_ frame passaggio VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a1dee-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-130">Il membro **dwFrames** della struttura identificata da *lpStep* specifica il numero di frame da anticipare prima di visualizzare un'altra immagine.</span><span class="sxs-lookup"><span data-stu-id="a1dee-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="a1dee-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_ \_ passaggio \_ inverso del videoregistratore MCI</span><span class="sxs-lookup"><span data-stu-id="a1dee-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-132">Passaggi in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="a1dee-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="a1dee-133">Per i dispositivi VCR, il parametro *lpStep* punta a una struttura [**\_ \_ \_ parametri del passaggio VCR MCI**](mci-vcr-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dee-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="a1dee-134">Con il tipo di dispositivo **videodisco** vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1dee-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a1dee-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>frame di passaggio di MCI \_ VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="a1dee-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-136">Il membro **dwFrames** della struttura identificata da *lpStep* specifica il numero di frame da scorrere.</span><span class="sxs-lookup"><span data-stu-id="a1dee-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="a1dee-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>il \_ passaggio di MCI VD è \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="a1dee-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="a1dee-138">Passaggi in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="a1dee-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="a1dee-139">Per i dispositivi videodisco, il parametro *lpStep* punta a una struttura [**parametri del passaggio di MCI \_ VD \_ \_**](mci-vd-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dee-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1dee-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1dee-140">Requirements</span></span>



| <span data-ttu-id="a1dee-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1dee-141">Requirement</span></span> | <span data-ttu-id="a1dee-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a1dee-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1dee-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1dee-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a1dee-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1dee-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a1dee-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1dee-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a1dee-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1dee-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a1dee-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1dee-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1dee-148"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1dee-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1dee-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1dee-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1dee-150">MCI</span><span class="sxs-lookup"><span data-stu-id="a1dee-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a1dee-151">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="a1dee-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


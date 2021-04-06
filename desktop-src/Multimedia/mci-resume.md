---
title: Comando MCI_RESUME (mmsystem. h)
description: Il \_ comando MCI Resume causa il riavvio dell'operazione sospesa da parte di un dispositivo in pausa.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- Comando MCI_RESUME Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963878"
---
# <a name="mci_resume-command"></a><span data-ttu-id="e6ea1-104">\_Comando MCI Resume</span><span class="sxs-lookup"><span data-stu-id="e6ea1-104">MCI\_RESUME command</span></span>

<span data-ttu-id="e6ea1-105">Il \_ comando MCI Resume causa il riavvio dell'operazione sospesa da parte di un dispositivo in pausa.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="e6ea1-106">Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="e6ea1-107">Anche se i dispositivi CD audio, MIDI sequencer e videodisco riconoscono questo comando, i driver di dispositivo MCICDA, MCISEQ e MCIPIONR non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="e6ea1-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="e6ea1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6ea1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ea1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e6ea1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e6ea1-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="e6ea1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e6ea1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e6ea1-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="e6ea1-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="e6ea1-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e6ea1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6ea1-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span><span class="sxs-lookup"><span data-stu-id="e6ea1-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="e6ea1-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e6ea1-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="e6ea1-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ea1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6ea1-118">Return Value</span></span>

<span data-ttu-id="e6ea1-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6ea1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6ea1-120">Remarks</span></span>

<span data-ttu-id="e6ea1-121">Questo comando riprende la riproduzione e la registrazione senza modificare il set di posizioni della traccia corrente con [il \_ record](mci-record.md) [MCI \_ Play](mci-play.md) o MCI.</span><span class="sxs-lookup"><span data-stu-id="e6ea1-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ea1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6ea1-122">Requirements</span></span>



| <span data-ttu-id="e6ea1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ea1-123">Requirement</span></span> | <span data-ttu-id="e6ea1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e6ea1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ea1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6ea1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ea1-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6ea1-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e6ea1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6ea1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ea1-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6ea1-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6ea1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6ea1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6ea1-130"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6ea1-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ea1-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6ea1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ea1-132">MCI</span><span class="sxs-lookup"><span data-stu-id="e6ea1-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6ea1-133">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="e6ea1-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


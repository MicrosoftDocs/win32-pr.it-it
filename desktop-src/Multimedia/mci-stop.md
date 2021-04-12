---
title: Comando MCI_STOP (mmsystem. h)
description: Il \_ comando MCI stop arresta tutte le sequenze di riproduzione e di record, Scarica tutti i buffer di riproduzione e interrompe la visualizzazione delle immagini video. CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- Comando MCI_STOP Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400679"
---
# <a name="mci_stop-command"></a><span data-ttu-id="b99c9-105">\_Comando di arresto MCI</span><span class="sxs-lookup"><span data-stu-id="b99c9-105">MCI\_STOP command</span></span>

<span data-ttu-id="b99c9-106">Il \_ comando MCI stop arresta tutte le sequenze di riproduzione e di record, Scarica tutti i buffer di riproduzione e interrompe la visualizzazione delle immagini video.</span><span class="sxs-lookup"><span data-stu-id="b99c9-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="b99c9-107">CD audio, Digital-video, MIDI sequencer, videodisco, VCR e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="b99c9-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="b99c9-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b99c9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="b99c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b99c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b99c9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b99c9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b99c9-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="b99c9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b99c9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b99c9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b99c9-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b99c9-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="b99c9-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b99c9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b99c9-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span><span class="sxs-lookup"><span data-stu-id="b99c9-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="b99c9-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b99c9-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b99c9-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b99c9-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b99c9-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b99c9-118">Return Value</span></span>

<span data-ttu-id="b99c9-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="b99c9-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b99c9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b99c9-120">Remarks</span></span>

<span data-ttu-id="b99c9-121">La differenza tra i \_ comandi MCI stop e [MCI \_ pause](mci-pause.md) dipende dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b99c9-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="b99c9-122">Se possibile, \_ la sospensione MCI sospende l'operazione del dispositivo, ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b99c9-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="b99c9-123">Per il dispositivo audio CD, MCI \_ Stop Reimposta la posizione di rilevamento corrente su zero. al contrario, [MCI \_ pause](mci-pause.md) mantiene la posizione corrente, prevedendo che il dispositivo riprende la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b99c9-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99c9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b99c9-124">Requirements</span></span>



| <span data-ttu-id="b99c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b99c9-125">Requirement</span></span> | <span data-ttu-id="b99c9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b99c9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b99c9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b99c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b99c9-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b99c9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b99c9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b99c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b99c9-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b99c9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b99c9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b99c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b99c9-132"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b99c9-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b99c9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b99c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99c9-134">MCI</span><span class="sxs-lookup"><span data-stu-id="b99c9-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b99c9-135">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="b99c9-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


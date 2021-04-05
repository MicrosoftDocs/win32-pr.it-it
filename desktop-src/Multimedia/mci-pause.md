---
title: Comando MCI_PAUSE (mmsystem. h)
description: Il \_ comando di sospensione MCI sospende l'azione corrente. CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- Comando MCI_PAUSE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739823"
---
# <a name="mci_pause-command"></a><span data-ttu-id="efae3-105">\_Comando di sospensione MCI</span><span class="sxs-lookup"><span data-stu-id="efae3-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="efae3-106">Il \_ comando di sospensione MCI sospende l'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="efae3-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="efae3-107">CD audio, Digital-video, MIDI sequencer, VCR, videodisco e waveform-i dispositivi audio riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="efae3-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="efae3-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="efae3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="efae3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="efae3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efae3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="efae3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="efae3-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="efae3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="efae3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="efae3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="efae3-113">\_Notifica MCI, \_ attesa MCI o, per i dispositivi digitali video e VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="efae3-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="efae3-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="efae3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="efae3-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span><span class="sxs-lookup"><span data-stu-id="efae3-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="efae3-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="efae3-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="efae3-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efae3-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efae3-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efae3-118">Return Value</span></span>

<span data-ttu-id="efae3-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="efae3-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="efae3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="efae3-120">Remarks</span></span>

<span data-ttu-id="efae3-121">La differenza tra i comandi [MCI \_ Stop](mci-stop.md) e MCI \_ pause dipende dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efae3-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="efae3-122">Se possibile, \_ la sospensione MCI sospende l'operazione del dispositivo, ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="efae3-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="efae3-123">Con i driver MCICDA, MCISEQ e MCIPIONR, il comando MCI \_ pause funziona allo stesso modo del comando MCI \_ stop.</span><span class="sxs-lookup"><span data-stu-id="efae3-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="efae3-124">Per i dispositivi digitali video, il parametro *lpPause* punta a una struttura [**DGV di \_ \_ sospensione \_ parametri MCI**](/previous-versions//dd743395(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="efae3-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="efae3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efae3-125">Requirements</span></span>



| <span data-ttu-id="efae3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="efae3-126">Requirement</span></span> | <span data-ttu-id="efae3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="efae3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efae3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efae3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="efae3-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="efae3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="efae3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efae3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="efae3-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="efae3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="efae3-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efae3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="efae3-133"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efae3-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efae3-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efae3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efae3-135">MCI</span><span class="sxs-lookup"><span data-stu-id="efae3-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="efae3-136">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="efae3-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


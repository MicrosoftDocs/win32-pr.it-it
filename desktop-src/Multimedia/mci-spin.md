---
title: Comando MCI_SPIN (mmsystem. h)
description: Il \_ comando MCI spin avvia la rotazione del dispositivo verso l'alto o verso il basso. I dispositivi videodisco riconoscono questo comando.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- Comando MCI_SPIN Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400532"
---
# <a name="mci_spin-command"></a><span data-ttu-id="2caf5-105">\_Comando di rotazione MCI</span><span class="sxs-lookup"><span data-stu-id="2caf5-105">MCI\_SPIN command</span></span>

<span data-ttu-id="2caf5-106">Il \_ comando MCI spin avvia la rotazione del dispositivo verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="2caf5-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="2caf5-107">I dispositivi videodisco riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="2caf5-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="2caf5-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2caf5-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="2caf5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2caf5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2caf5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2caf5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2caf5-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="2caf5-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2caf5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2caf5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2caf5-113">\_Attesa notifica MCI o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2caf5-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="2caf5-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2caf5-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2caf5-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span><span class="sxs-lookup"><span data-stu-id="2caf5-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="2caf5-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2caf5-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="2caf5-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2caf5-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2caf5-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2caf5-118">Return Value</span></span>

<span data-ttu-id="2caf5-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="2caf5-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2caf5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2caf5-120">Remarks</span></span>

<span data-ttu-id="2caf5-121">I seguenti flag aggiuntivi si applicano ai dispositivi videodisco:</span><span class="sxs-lookup"><span data-stu-id="2caf5-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="2caf5-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>casella di riepilogo per MCI \_ VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="2caf5-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="2caf5-123">Arresta la rotazione del disco.</span><span class="sxs-lookup"><span data-stu-id="2caf5-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="2caf5-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>\_ \_ spin up MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="2caf5-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="2caf5-125">Avvia la rotazione del disco.</span><span class="sxs-lookup"><span data-stu-id="2caf5-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2caf5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2caf5-126">Requirements</span></span>



| <span data-ttu-id="2caf5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2caf5-127">Requirement</span></span> | <span data-ttu-id="2caf5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2caf5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2caf5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2caf5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2caf5-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2caf5-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2caf5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2caf5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2caf5-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2caf5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2caf5-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2caf5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2caf5-134"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2caf5-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2caf5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2caf5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2caf5-136">MCI</span><span class="sxs-lookup"><span data-stu-id="2caf5-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2caf5-137">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="2caf5-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


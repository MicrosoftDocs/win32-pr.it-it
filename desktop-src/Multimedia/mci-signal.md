---
title: Comando MCI_SIGNAL (mmsystem. h)
description: Il \_ comando MCI Signal imposta una posizione specificata nell'area di lavoro. I dispositivi digitali video riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Comando MCI_SIGNAL Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400533"
---
# <a name="mci_signal-command"></a><span data-ttu-id="dd8b2-106">\_Comando MCI Signal</span><span class="sxs-lookup"><span data-stu-id="dd8b2-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="dd8b2-107">Il \_ comando MCI Signal imposta una posizione specificata nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="dd8b2-108">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="dd8b2-109">MCIAVI supporta un solo segnale attivo alla volta.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="dd8b2-110">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="dd8b2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd8b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd8b2-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="dd8b2-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-113">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="dd8b2-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="dd8b2-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-115">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="dd8b2-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="dd8b2-116">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dd8b2-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd8b2-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span><span class="sxs-lookup"><span data-stu-id="dd8b2-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-118">Puntatore a una [**struttura \_ \_ \_ parametri del segnale DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .</span><span class="sxs-lookup"><span data-stu-id="dd8b2-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd8b2-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd8b2-119">Return Value</span></span>

<span data-ttu-id="dd8b2-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd8b2-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd8b2-121">Remarks</span></span>

<span data-ttu-id="dd8b2-122">La finestra il cui handle specificato nel membro **dwCallback** della struttura [**MCI \_ DGV \_ Signal \_ parametri**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) riceve il \_ messaggio MCISIGNAL mm.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="dd8b2-123">I flag seguenti si applicano ai dispositivi video digitali:</span><span class="sxs-lookup"><span data-stu-id="dd8b2-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="dd8b2-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_segnale DGV \_ MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="dd8b2-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-125">Una posizione del segnale è inclusa nel membro **dwPosition** della struttura identificata da *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="dd8b2-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_ \_ annullamento segnale DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="dd8b2-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-127">Rimuove la posizione del segnale specificata dal valore associato al \_ segnale DGV \_ MCI \_ USERVAL.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="dd8b2-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_segnale DGV \_ MCI \_ ogni</span><span class="sxs-lookup"><span data-stu-id="dd8b2-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-129">Il valore del periodo del segnale è incluso nel membro **dwPeriod** della struttura identificata da *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="dd8b2-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_posizione del \_ segnale \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="dd8b2-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-131">Il dispositivo invierà il valore di posizione con il messaggio di Windows invece del valore specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="dd8b2-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_ \_ USERVAL segnale DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="dd8b2-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="dd8b2-133">Un valore di dati è incluso nel membro **dwUserParm** della struttura identificata da *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="dd8b2-134">Il valore di dati associato a questa richiesta viene restituito con il messaggio di Windows.</span><span class="sxs-lookup"><span data-stu-id="dd8b2-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd8b2-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd8b2-135">Requirements</span></span>



| <span data-ttu-id="dd8b2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd8b2-136">Requirement</span></span> | <span data-ttu-id="dd8b2-137">Valore</span><span class="sxs-lookup"><span data-stu-id="dd8b2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8b2-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd8b2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dd8b2-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd8b2-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dd8b2-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd8b2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dd8b2-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd8b2-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dd8b2-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd8b2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd8b2-143"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd8b2-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd8b2-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd8b2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd8b2-145">MCI</span><span class="sxs-lookup"><span data-stu-id="dd8b2-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dd8b2-146">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="dd8b2-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


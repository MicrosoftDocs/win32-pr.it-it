---
title: Comando MCI_BREAK (mmsystem. h)
description: Il \_ comando MCI break imposta un tasto di pausa per un dispositivo MCI. MCI supporta direttamente questo comando anziché passarlo al dispositivo. Qualsiasi applicazione MCI può utilizzare questo comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Comando MCI_BREAK Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476240"
---
# <a name="mci_break-command"></a><span data-ttu-id="ef073-106">\_Comando di Interrompi MCI</span><span class="sxs-lookup"><span data-stu-id="ef073-106">MCI\_BREAK command</span></span>

<span data-ttu-id="ef073-107">Il \_ comando MCI break imposta un tasto di pausa per un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ef073-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="ef073-108">MCI supporta direttamente questo comando anziché passarlo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef073-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="ef073-109">Qualsiasi applicazione MCI può utilizzare questo comando.</span><span class="sxs-lookup"><span data-stu-id="ef073-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="ef073-110">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ef073-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="ef073-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef073-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef073-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ef073-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ef073-113">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="ef073-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ef073-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ef073-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ef073-115">\_Notifica MCI, \_ attesa MCI o, per i dispositivi VCR (Digital-video e videoregistratore), \_ test MCI.</span><span class="sxs-lookup"><span data-stu-id="ef073-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="ef073-116">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ef073-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef073-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span><span class="sxs-lookup"><span data-stu-id="ef073-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="ef073-118">Puntatore a una [**struttura \_ \_ parametri break MCI**](mci-break-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ef073-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef073-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef073-119">Return Value</span></span>

<span data-ttu-id="ef073-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ef073-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef073-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef073-121">Remarks</span></span>

<span data-ttu-id="ef073-122">Potrebbe essere necessario premere il tasto Break più volte per interrompere un'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="ef073-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="ef073-123">Quando si preme il tasto INTERR dopo che l'attesa di un dispositivo è stata annullata, è possibile inviare l'operazione</span><span class="sxs-lookup"><span data-stu-id="ef073-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="ef073-124">Se un'applicazione ha un'azione definita per il codice della chiave virtuale, può rispondere inavvertitamente all'interruzioni.</span><span class="sxs-lookup"><span data-stu-id="ef073-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="ef073-125">Ad esempio, un'applicazione che usa \_ l'annullamento VK per un tasto di scelta rapida può rispondere al tasto Ctrl + Break predefinito se viene premuto dopo l'annullamento di un'attesa.</span><span class="sxs-lookup"><span data-stu-id="ef073-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="ef073-126">I flag aggiuntivi seguenti si applicano a tutti i dispositivi:</span><span class="sxs-lookup"><span data-stu-id="ef073-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="ef073-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND Interrompi MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef073-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="ef073-128">Il membro **hwndBreak** della struttura identificata da *lpBreak* contiene un handle di finestra che deve essere la finestra corrente per abilitare il rilevamento delle interruzioni per quel dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ef073-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="ef073-129">Si tratta in genere della finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef073-129">This is usually the application's main window.</span></span> <span data-ttu-id="ef073-130">Se omesso, MCI non controlla l'handle della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="ef073-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="ef073-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_chiave di pausa MCI \_</span><span class="sxs-lookup"><span data-stu-id="ef073-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="ef073-132">Il membro **nVirtKey** della struttura identificata da *lpBreak* specifica il codice della chiave virtuale usato per la chiave Break.</span><span class="sxs-lookup"><span data-stu-id="ef073-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="ef073-133">Per impostazione predefinita, MCI assegna CTRL + INTERr come chiave di break.</span><span class="sxs-lookup"><span data-stu-id="ef073-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="ef073-134">Questo flag è obbligatorio se MCI \_ break \_ off non è specificato.</span><span class="sxs-lookup"><span data-stu-id="ef073-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="ef073-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>interruzione di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ef073-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="ef073-136">Disabilita qualsiasi chiave di break esistente per il dispositivo indicato.</span><span class="sxs-lookup"><span data-stu-id="ef073-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef073-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef073-137">Requirements</span></span>



| <span data-ttu-id="ef073-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef073-138">Requirement</span></span> | <span data-ttu-id="ef073-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ef073-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef073-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef073-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ef073-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef073-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ef073-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef073-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ef073-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef073-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ef073-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef073-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef073-145"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef073-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef073-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef073-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef073-147">MCI</span><span class="sxs-lookup"><span data-stu-id="ef073-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ef073-148">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="ef073-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


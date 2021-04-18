---
title: Signal (comando)
description: Il comando Signal identifica una posizione specificata nell'area di lavoro inviando all'applicazione un \_ messaggio MCISIGNAL mm. I dispositivi digitali video riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- comando segnale Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301824"
---
# <a name="signal-command"></a><span data-ttu-id="5f6cc-106">Signal (comando)</span><span class="sxs-lookup"><span data-stu-id="5f6cc-106">signal command</span></span>

<span data-ttu-id="5f6cc-107">Il comando Signal identifica una posizione specificata nell'area di lavoro inviando all'applicazione un messaggio [ \_ MCISIGNAL mm](mm-mcisignal.md) .</span><span class="sxs-lookup"><span data-stu-id="5f6cc-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="5f6cc-108">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="5f6cc-109">MCIAVI supporta un solo segnale attivo alla volta.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="5f6cc-110">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5f6cc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f6cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f6cc-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5f6cc-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5f6cc-113">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-113">Identifier of an MCI device.</span></span> <span data-ttu-id="5f6cc-114">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5f6cc-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span><span class="sxs-lookup"><span data-stu-id="5f6cc-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5f6cc-116">Uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-116">One of the following flags.</span></span>



| <span data-ttu-id="5f6cc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6cc-117">Value</span></span>            | <span data-ttu-id="5f6cc-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5f6cc-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6cc-119">alla posizione</span><span class="sxs-lookup"><span data-stu-id="5f6cc-119">at position</span></span>      | <span data-ttu-id="5f6cc-120">Specifica il frame per richiamare un segnale.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5f6cc-121">cancel</span><span class="sxs-lookup"><span data-stu-id="5f6cc-121">cancel</span></span>           | <span data-ttu-id="5f6cc-122">Rimuove i segnali dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-122">Removes signals from the workspace.</span></span> <span data-ttu-id="5f6cc-123">Un singolo segnale viene specificato tramite il flag "userValue".</span><span class="sxs-lookup"><span data-stu-id="5f6cc-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="5f6cc-124">Se il flag "userValue" non viene specificato con "Annulla", il dispositivo annulla tutti i segnali.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="5f6cc-125">Il flag "Cancel" non è compatibile con i flag "at", "Ever" e "Return position".</span><span class="sxs-lookup"><span data-stu-id="5f6cc-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5f6cc-126">ogni *intervallo*</span><span class="sxs-lookup"><span data-stu-id="5f6cc-126">every *interval*</span></span> | <span data-ttu-id="5f6cc-127">Specifica il periodo dei segnali.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-127">Specifies the period of the signals.</span></span> <span data-ttu-id="5f6cc-128">Il valore dell' *intervallo* è specificato nel formato dell'ora corrente. Se usato con la *posizione*"at", i segnali vengono posizionati in tutta l'area di lavoro con un segno di segnale posizionato alla *posizione*.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="5f6cc-129">Senza il flag "at", i segnali vengono posizionati nell'area di lavoro con un segnale nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="5f6cc-130">Se questo flag viene omesso, viene contrassegnata solo la posizione indicata dal flag "at".</span><span class="sxs-lookup"><span data-stu-id="5f6cc-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="5f6cc-131">Se il valore dell' *intervallo* è inferiore alla frequenza minima supportata da un dispositivo, utilizzerà il relativo valore minimo.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="5f6cc-132">posizione di ritorno</span><span class="sxs-lookup"><span data-stu-id="5f6cc-132">return position</span></span>  | <span data-ttu-id="5f6cc-133">Indica che il dispositivo deve inviare il valore di posizione anziché l'identificatore "userValue" nel messaggio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="5f6cc-134">L'identificatore "userValue" può comunque essere usato per annullare o ridefinire i contrassegni di segnale.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5f6cc-135">*ID* userValue</span><span class="sxs-lookup"><span data-stu-id="5f6cc-135">uservalue *id*</span></span>   | <span data-ttu-id="5f6cc-136">Specifica un identificatore restituito con il messaggio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="5f6cc-137">Questo identificatore funge da identificatore che può essere usato con altri comandi del **segnale** per fare riferimento a questa impostazione del **segnale** .</span><span class="sxs-lookup"><span data-stu-id="5f6cc-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="5f6cc-138">Se omesso, il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="5f6cc-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="5f6cc-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5f6cc-140">Può essere "Wait", "notify", "test" o una combinazione di questi.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="5f6cc-141">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5f6cc-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f6cc-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f6cc-142">Return Value</span></span>

<span data-ttu-id="5f6cc-143">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f6cc-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f6cc-144">Remarks</span></span>

<span data-ttu-id="5f6cc-145">L'handle della finestra utilizzato per la notifica dei messaggi di completamento del comando viene utilizzato anche per la segnalazione.</span><span class="sxs-lookup"><span data-stu-id="5f6cc-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f6cc-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f6cc-146">Requirements</span></span>



| <span data-ttu-id="5f6cc-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f6cc-147">Requirement</span></span> | <span data-ttu-id="5f6cc-148">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6cc-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5f6cc-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6cc-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5f6cc-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f6cc-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5f6cc-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6cc-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5f6cc-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f6cc-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5f6cc-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f6cc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6cc-154">MCI</span><span class="sxs-lookup"><span data-stu-id="5f6cc-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5f6cc-155">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="5f6cc-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="5f6cc-156">\_MCISIGNAL mm</span><span class="sxs-lookup"><span data-stu-id="5f6cc-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 


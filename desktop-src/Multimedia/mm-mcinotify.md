---
title: Messaggio MM_MCINOTIFY (mmsystem. h)
description: Il \_ messaggio mm MCINOTIFY notifica a un'applicazione che un dispositivo MCI ha completato un'operazione. I dispositivi MCI inviano questo messaggio solo quando \_ viene usato il flag di notifica MCI.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120458"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="7f4a5-105">\_Messaggio MCINOTIFY mm</span><span class="sxs-lookup"><span data-stu-id="7f4a5-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="7f4a5-106">Il messaggio **mm \_ MCINOTIFY** notifica a un'applicazione che un dispositivo MCI ha completato un'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="7f4a5-107">I dispositivi MCI inviano questo messaggio solo quando \_ viene usato il flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="7f4a5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f4a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f4a5-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="7f4a5-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7f4a5-110">Motivo della notifica.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-110">Reason for the notification.</span></span> <span data-ttu-id="7f4a5-111">Vengono definiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f4a5-111">The following values are defined:</span></span>



| <span data-ttu-id="7f4a5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4a5-112">Requirement</span></span> | <span data-ttu-id="7f4a5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7f4a5-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4a5-114">\_notifica MCI \_ interrotta</span><span class="sxs-lookup"><span data-stu-id="7f4a5-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="7f4a5-115">Il dispositivo ha ricevuto un comando che impedisce che le condizioni correnti per avviare la funzione di callback vengano soddisfatte.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="7f4a5-116">Se un nuovo comando interrompe il comando corrente e richiede anche la notifica, il dispositivo invia solo questo messaggio e non la \_ notifica MCI \_ sostituita</span><span class="sxs-lookup"><span data-stu-id="7f4a5-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="7f4a5-117">\_errore di notifica MCI \_</span><span class="sxs-lookup"><span data-stu-id="7f4a5-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="7f4a5-118">Si è verificato un errore del dispositivo durante l'esecuzione del comando da parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="7f4a5-119">\_notifica MCI \_ riuscita</span><span class="sxs-lookup"><span data-stu-id="7f4a5-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="7f4a5-120">Le condizioni che avviano la funzione di callback sono state soddisfatte.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="7f4a5-121">\_notifica MCI \_ sostituita</span><span class="sxs-lookup"><span data-stu-id="7f4a5-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="7f4a5-122">Il dispositivo ha ricevuto un altro comando con il flag "notify" impostato e le condizioni correnti per l'avvio della funzione di callback sono state sostituite.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="7f4a5-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span><span class="sxs-lookup"><span data-stu-id="7f4a5-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="7f4a5-124">Identificatore del dispositivo che avvia la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f4a5-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f4a5-125">Return Value</span></span>

<span data-ttu-id="7f4a5-126">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f4a5-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f4a5-127">Remarks</span></span>

<span data-ttu-id="7f4a5-128">Per ulteriori informazioni sul flag di \_ notifica MCI, vedere [il flag di notifica](the-notify-flag.md).</span><span class="sxs-lookup"><span data-stu-id="7f4a5-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="7f4a5-129">Un dispositivo restituisce il \_ flag MCI Notify \_ successful con **mm \_ MCINOTIFY** quando viene completata l'azione per un comando.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="7f4a5-130">Ad esempio, un dispositivo audio CD utilizza questo flag per la notifica del comando [**Play**](play.md) ( [**MCI \_ Play**](mci-play.md)) al termine della riproduzione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="7f4a5-131">Il comando **Play** ha esito positivo solo quando raggiunge la posizione finale specificata o raggiunge la fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="7f4a5-132">Analogamente, i comandi [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) e [**record**](record.md) ( [**MCI \_ record**](mci-record.md)) non restituiscono la \_ notifica MCI \_ riuscita fino a raggiungere la posizione finale specificata o raggiungere la fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="7f4a5-133">Un dispositivo restituisce il \_ \_ flag di notifica di MCI interrotto con **mm \_ MCINOTIFY** solo quando riceve un comando che impedisce che soddisfi le condizioni di notifica.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="7f4a5-134">Ad esempio, il comando [**Play**](play.md) non interrompe la notifica per un comando **Play** precedente, purché il nuovo comando non modifichi la direzione della riproduzione o modifichi la posizione finale.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="7f4a5-135">I comandi [**Seek**](seek.md) e [**record**](record.md) si comportano in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="7f4a5-136">MCI non invia inoltre notifiche MCI \_ \_ interrotte quando la riproduzione o la registrazione viene sospesa con il comando [**Sospendi**](pause.md) (pausa [**MCI \_**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="7f4a5-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="7f4a5-137">L'invio del comando [**Resume**](resume.md) ( [**MCI \_ Resume**](mci-resume.md)) consente loro di continuare a soddisfare le condizioni di callback.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="7f4a5-138">Quando l'applicazione richiede una notifica per un comando, controllare la restituzione dell'errore delle funzioni [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7f4a5-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="7f4a5-139">Se queste funzioni riscontrano un errore e restituiscono un valore diverso da zero, MCI non imposterà la notifica per il comando.</span><span class="sxs-lookup"><span data-stu-id="7f4a5-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f4a5-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f4a5-140">Requirements</span></span>



| <span data-ttu-id="7f4a5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4a5-141">Requirement</span></span> | <span data-ttu-id="7f4a5-142">Valore</span><span class="sxs-lookup"><span data-stu-id="7f4a5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4a5-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f4a5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4a5-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f4a5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7f4a5-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f4a5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4a5-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f4a5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7f4a5-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f4a5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4a5-148"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f4a5-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4a5-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f4a5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4a5-150">MCI</span><span class="sxs-lookup"><span data-stu-id="7f4a5-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7f4a5-151">Messaggi MCI</span><span class="sxs-lookup"><span data-stu-id="7f4a5-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="7f4a5-152">**pause**</span><span class="sxs-lookup"><span data-stu-id="7f4a5-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="7f4a5-153">**Play**</span><span class="sxs-lookup"><span data-stu-id="7f4a5-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="7f4a5-154">**record**</span><span class="sxs-lookup"><span data-stu-id="7f4a5-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="7f4a5-155">**riprendere**</span><span class="sxs-lookup"><span data-stu-id="7f4a5-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="7f4a5-156">**cercare**</span><span class="sxs-lookup"><span data-stu-id="7f4a5-156">**seek**</span></span>](seek.md)
</dt> </dl>

 


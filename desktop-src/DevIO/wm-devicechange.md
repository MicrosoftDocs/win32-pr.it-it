---
description: Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Messaggio WM_DEVICECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401413"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="586a1-103">\_Messaggio DEVICECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="586a1-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="586a1-104">Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.</span><span class="sxs-lookup"><span data-stu-id="586a1-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="586a1-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="586a1-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="586a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="586a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="586a1-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="586a1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="586a1-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="586a1-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="586a1-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="586a1-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="586a1-110">Identificatore **WM \_ DEVICECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="586a1-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="586a1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="586a1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="586a1-112">Evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="586a1-112">The event that has occurred.</span></span> <span data-ttu-id="586a1-113">Questo parametro può essere uno dei valori seguenti del file di intestazione DBT. h.</span><span class="sxs-lookup"><span data-stu-id="586a1-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="586a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="586a1-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="586a1-115">Significato</span><span class="sxs-lookup"><span data-stu-id="586a1-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="586a1-116"><dt>**[DBT \_](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="586a1-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="586a1-117">Una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="586a1-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="586a1-118"><dt>**[DBT \_](dbt-configchanged.md)**</dt> <dt>0x0018</dt> CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="586a1-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="586a1-119">La configurazione corrente è cambiata a causa di un ancoraggio o di Undock.</span><span class="sxs-lookup"><span data-stu-id="586a1-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="586a1-120"><dt>**[DBT \_](dbt-customevent.md)**</dt> <dt>0x8006</dt> CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="586a1-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="586a1-121">Si è verificato un evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="586a1-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="586a1-122"><dt>**[DBT \_](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="586a1-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="586a1-123">Un dispositivo o un elemento multimediale è stato inserito ed è ora disponibile.</span><span class="sxs-lookup"><span data-stu-id="586a1-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="586a1-124"><dt>**[DBT \_](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="586a1-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="586a1-125">Viene richiesta l'autorizzazione per rimuovere un dispositivo o un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="586a1-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="586a1-126">Qualsiasi applicazione può negare questa richiesta e annullare la rimozione.</span><span class="sxs-lookup"><span data-stu-id="586a1-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="586a1-127"><dt>**[DBT \_](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="586a1-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="586a1-128">Una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="586a1-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="586a1-129"><dt>**[DBT \_](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="586a1-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="586a1-130">Un dispositivo o un elemento multimediale è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="586a1-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="586a1-131"><dt>**[DBT \_](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="586a1-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="586a1-132">Un dispositivo o un elemento multimediale sta per essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="586a1-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="586a1-133">Non può essere negato.</span><span class="sxs-lookup"><span data-stu-id="586a1-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="586a1-134"><dt>**[DBT \_](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="586a1-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="586a1-135">Si è verificato un evento specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="586a1-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="586a1-136"><dt>**[DBT \_ DEVNODE \_ modificato](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="586a1-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="586a1-137">Un dispositivo è stato aggiunto o rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="586a1-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="586a1-138"><dt>**[DBT \_](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="586a1-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="586a1-139">Viene richiesta l'autorizzazione per modificare la configurazione corrente (dock o Undock).</span><span class="sxs-lookup"><span data-stu-id="586a1-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="586a1-140"><dt>**[DBT \_](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt> USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="586a1-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="586a1-141">Il significato di questo messaggio è definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="586a1-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="586a1-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="586a1-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="586a1-143">Puntatore a una struttura che contiene dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="586a1-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="586a1-144">Il formato dipende dal valore del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="586a1-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="586a1-145">Per ulteriori informazioni, vedere la documentazione relativa a ogni evento.</span><span class="sxs-lookup"><span data-stu-id="586a1-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="586a1-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="586a1-146">Return value</span></span>

<span data-ttu-id="586a1-147">Restituisce **true** per concedere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="586a1-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="586a1-148">Restituisce **la \_ query broadcast \_ Deny** per negare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="586a1-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="586a1-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="586a1-149">Remarks</span></span>

<span data-ttu-id="586a1-150">Per i dispositivi che offrono funzionalità controllabili dal software, ad esempio l'espulsione e il blocco, il sistema invia in genere un messaggio [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) per consentire alle applicazioni e ai driver di dispositivo di terminare l'uso del dispositivo normalmente.</span><span class="sxs-lookup"><span data-stu-id="586a1-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="586a1-151">Se il sistema rimuove forzatamente un dispositivo, è possibile che non invii un messaggio [ \_ DEVICEQUERYREMOVE di DBT](dbt-devicequeryremove.md) prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="586a1-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="586a1-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="586a1-152">Requirements</span></span>



| <span data-ttu-id="586a1-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="586a1-153">Requirement</span></span> | <span data-ttu-id="586a1-154">Valore</span><span class="sxs-lookup"><span data-stu-id="586a1-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586a1-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="586a1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="586a1-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="586a1-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="586a1-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="586a1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="586a1-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="586a1-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="586a1-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="586a1-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="586a1-160"><dt>Winuser. h (include Windows. h o dbt. h)</dt></span><span class="sxs-lookup"><span data-stu-id="586a1-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586a1-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="586a1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586a1-162">\_CONFIGCHANGECANCELED DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="586a1-163">\_CONFIGCHANGED DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="586a1-164">\_CUSTOMEVENT DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="586a1-165">\_DEVICEARRIVAL DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="586a1-166">\_DEVICEQUERYREMOVE DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="586a1-167">\_DEVICEQUERYREMOVEFAILED DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="586a1-168">\_DEVICEREMOVECOMPLETE DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="586a1-169">\_DEVICEREMOVEPENDING DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="586a1-170">\_DEVICETYPESPECIFIC DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="586a1-171">\_DEVNODE DBT \_ modificato</span><span class="sxs-lookup"><span data-stu-id="586a1-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="586a1-172">\_QUERYCHANGECONFIG DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="586a1-173">\_USERDEFINED DBT</span><span class="sxs-lookup"><span data-stu-id="586a1-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 


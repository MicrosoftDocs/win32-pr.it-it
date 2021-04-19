---
description: Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581503"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="e2125-103">Messaggio \_ DEVICECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="e2125-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="e2125-104">Notifica a un'applicazione una modifica alla configurazione hardware di un dispositivo o del computer.</span><span class="sxs-lookup"><span data-stu-id="e2125-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="e2125-105">Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2125-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="e2125-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2125-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2125-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="e2125-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e2125-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="e2125-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="e2125-109">*Umsg*</span><span class="sxs-lookup"><span data-stu-id="e2125-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e2125-110">Identificatore **\_ DEVICECHANGE WM.**</span><span class="sxs-lookup"><span data-stu-id="e2125-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e2125-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2125-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2125-112">Evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="e2125-112">The event that has occurred.</span></span> <span data-ttu-id="e2125-113">Questo parametro può essere uno dei valori seguenti del file di intestazione Dbt.h.</span><span class="sxs-lookup"><span data-stu-id="e2125-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="e2125-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e2125-114">Value</span></span> | <span data-ttu-id="e2125-115">Significato</span><span class="sxs-lookup"><span data-stu-id="e2125-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="e2125-116">**[DBT \_ DEVNODES \_ MODIFICATO](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="e2125-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="e2125-117">0x0007</span></span> | <span data-ttu-id="e2125-118">Un dispositivo è stato aggiunto o rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e2125-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="e2125-119">**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="e2125-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="e2125-120">0x0017</span></span> | <span data-ttu-id="e2125-121">È richiesta l'autorizzazione per modificare la configurazione corrente (ancora o disanco).</span><span class="sxs-lookup"><span data-stu-id="e2125-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="e2125-122">**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="e2125-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="e2125-123">0x0018</span></span> | <span data-ttu-id="e2125-124">La configurazione corrente è stata modificata a causa di un'ancoraggio o un disinseramento.</span><span class="sxs-lookup"><span data-stu-id="e2125-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="e2125-125">**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="e2125-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="e2125-126">0x0019</span></span> | <span data-ttu-id="e2125-127">Una richiesta di modifica della configurazione corrente (ancora o disanco) è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="e2125-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="e2125-128">**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="e2125-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="e2125-129">0x8000</span></span> | <span data-ttu-id="e2125-130">Un dispositivo o un elemento multimediale è stato inserito ed è ora disponibile.</span><span class="sxs-lookup"><span data-stu-id="e2125-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="e2125-131">**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="e2125-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="e2125-132">0x8001</span></span> | <span data-ttu-id="e2125-133">È richiesta l'autorizzazione per rimuovere un dispositivo o un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="e2125-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="e2125-134">Qualsiasi applicazione può rifiutare questa richiesta e annullare la rimozione.</span><span class="sxs-lookup"><span data-stu-id="e2125-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="e2125-135">**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="e2125-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="e2125-136">0x8002</span></span> | <span data-ttu-id="e2125-137">Una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="e2125-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="e2125-138">**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="e2125-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="e2125-139">0x8003</span></span> | <span data-ttu-id="e2125-140">Un dispositivo o un elemento multimediale sta per essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="e2125-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="e2125-141">Non può essere negato.</span><span class="sxs-lookup"><span data-stu-id="e2125-141">Cannot be denied.</span></span> |
| <span data-ttu-id="e2125-142">**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="e2125-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="e2125-143">0x8004</span></span> | <span data-ttu-id="e2125-144">Un dispositivo o un elemento multimediale è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="e2125-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="e2125-145">**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="e2125-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="e2125-146">0x8005</span></span> | <span data-ttu-id="e2125-147">Si è verificato un evento specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2125-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="e2125-148">**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="e2125-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="e2125-149">0x8006</span></span> | <span data-ttu-id="e2125-150">Si è verificato un evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e2125-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="e2125-151">**[DBT \_ USERDEFINED](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="e2125-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="e2125-152">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="e2125-152">0xFFFF</span></span> | <span data-ttu-id="e2125-153">Il significato di questo messaggio è definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e2125-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="e2125-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2125-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2125-155">Puntatore a una struttura che contiene dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e2125-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="e2125-156">Il formato dipende dal valore del *parametro wParam.*</span><span class="sxs-lookup"><span data-stu-id="e2125-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="e2125-157">Per altre informazioni, vedere la documentazione per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="e2125-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2125-158">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2125-158">Return value</span></span>

<span data-ttu-id="e2125-159">Restituire **TRUE per** concedere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e2125-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="e2125-160">Restituisce **BROADCAST \_ QUERY \_ DENY** per negare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e2125-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2125-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2125-161">Remarks</span></span>

<span data-ttu-id="e2125-162">Per i dispositivi che offrono funzionalità di controllo software, ad esempio l'espulsione e il blocco, il sistema in genere invia un messaggio [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) per consentire alle applicazioni e ai driver di dispositivo di terminare normalmente l'uso del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2125-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="e2125-163">Se il sistema rimuove forzatamente un dispositivo, potrebbe non inviare un [messaggio DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) prima di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e2125-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2125-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2125-164">Requirements</span></span>

| <span data-ttu-id="e2125-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2125-165">Requirement</span></span> | <span data-ttu-id="e2125-166">Valore</span><span class="sxs-lookup"><span data-stu-id="e2125-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2125-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2125-167">Minimum supported client</span></span> | <span data-ttu-id="e2125-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2125-168">Windows XP</span></span> |
| <span data-ttu-id="e2125-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2125-169">Minimum supported server</span></span> | <span data-ttu-id="e2125-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2125-170">Windows Server 2003</span></span>|
| <span data-ttu-id="e2125-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2125-171">Header</span></span> | <dl> <span data-ttu-id="e2125-172"><dt>Winuser.h (includere Windows.h o Dbt.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2125-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e2125-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2125-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2125-174">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="e2125-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="e2125-175">DBT \_ CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="e2125-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="e2125-176">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="e2125-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="e2125-177">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="e2125-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="e2125-178">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="e2125-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="e2125-179">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="e2125-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="e2125-180">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="e2125-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="e2125-181">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="e2125-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="e2125-182">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="e2125-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="e2125-183">DBT \_ DEVNODES \_ MODIFICATO</span><span class="sxs-lookup"><span data-stu-id="e2125-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="e2125-184">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="e2125-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="e2125-185">DBT \_ DEFINITO DALL'UTENTE</span><span class="sxs-lookup"><span data-stu-id="e2125-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

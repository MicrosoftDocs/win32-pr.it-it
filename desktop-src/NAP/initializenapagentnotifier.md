---
title: Funzione InitializeNapAgentNotifier (NapUtil. h)
description: Sottoscrive il processo chiamante per NapAgent le notifiche di modifica dello stato e la quarantena delle notifiche di modifica dello stato.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- NAP funzione InitializeNapAgentNotifier
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964003"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="8480b-104">InitializeNapAgentNotifier (funzione)</span><span class="sxs-lookup"><span data-stu-id="8480b-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="8480b-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8480b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8480b-106">La funzione **InitializeNapAgentNotifier** sottoscrive il processo chiamante per napagent le notifiche di modifica dello stato e la quarantena delle notifiche di modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="8480b-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="8480b-107">Queste notifiche vengono fornite dal servizio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="8480b-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8480b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8480b-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="8480b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8480b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8480b-110">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8480b-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8480b-111">Valore [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) che specifica il tipo di notifiche del servizio da ricevere.</span><span class="sxs-lookup"><span data-stu-id="8480b-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="8480b-112">*hNotifyEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8480b-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8480b-113">Handle di evento utilizzato per la notifica.</span><span class="sxs-lookup"><span data-stu-id="8480b-113">An event handle used for notification.</span></span> <span data-ttu-id="8480b-114">Il chiamante deve passare un handle aperto al parametro *hNotifyEvent* .</span><span class="sxs-lookup"><span data-stu-id="8480b-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="8480b-115">Il chiamante deve anche chiudere l'handle di evento quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="8480b-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8480b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8480b-116">Return value</span></span>



| <span data-ttu-id="8480b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8480b-117">Return code</span></span>                                                                                                | <span data-ttu-id="8480b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8480b-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8480b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8480b-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8480b-120">Inizializzazione completata.</span><span class="sxs-lookup"><span data-stu-id="8480b-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="8480b-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="8480b-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="8480b-122">Inizializzazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="8480b-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="8480b-123"><dt>**ERRORE \_ già \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="8480b-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="8480b-124">Il processo ha già sottoscritto le notifiche del servizio NapAgent del *tipo* specificato.</span><span class="sxs-lookup"><span data-stu-id="8480b-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="8480b-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8480b-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="8480b-126">È stato passato un argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="8480b-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="8480b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="8480b-127">Remarks</span></span>

<span data-ttu-id="8480b-128">Questa funzione non è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8480b-128">This function is not thread safe.</span></span>

<span data-ttu-id="8480b-129">Ogni processo che richiede una sottoscrizione per le notifiche del servizio NapAgent del *tipo* specificato deve chiamare **InitializeNapAgentNotifier** per sottoscrivere le notifiche.</span><span class="sxs-lookup"><span data-stu-id="8480b-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="8480b-130">Se un processo deve sottoscrivere più di un tipo di notifica, deve chiamare **InitializeNapAgentNotifier** una volta per ogni tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="8480b-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="8480b-131">Quando un processo non richiede ulteriori notifiche, il processo deve chiamare [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) per il *tipo* specificato.</span><span class="sxs-lookup"><span data-stu-id="8480b-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8480b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8480b-132">Requirements</span></span>



| <span data-ttu-id="8480b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8480b-133">Requirement</span></span> | <span data-ttu-id="8480b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8480b-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8480b-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8480b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8480b-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8480b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8480b-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8480b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8480b-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8480b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8480b-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8480b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8480b-140"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="8480b-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="8480b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8480b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8480b-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8480b-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8480b-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8480b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8480b-144">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="8480b-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 






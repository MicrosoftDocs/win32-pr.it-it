---
description: Sottoscrive le notifiche di modifica dello stato del servizio utilizzando una funzione di callback.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Funzione SubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316089"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="f6918-103">SubscribeServiceChangeNotifications (funzione)</span><span class="sxs-lookup"><span data-stu-id="f6918-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="f6918-104">Sottoscrive le notifiche di modifica dello stato del servizio utilizzando una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f6918-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6918-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6918-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="f6918-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6918-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6918-107">*hService* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6918-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6918-108">Handle per il servizio o un handle per Gestione controllo servizi (SCM) per monitorare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="f6918-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="f6918-109">Gli handle ai servizi vengono restituiti dalla funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) e [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e devono avere il diritto di accesso **\_ \_ stato query del servizio** .</span><span class="sxs-lookup"><span data-stu-id="f6918-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="f6918-110">Gli handle per Gestione controllo servizi vengono restituiti dalla funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) ed è necessario che il **\_ gestore SC \_ enumera \_** il diritto di accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="f6918-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="f6918-111">*eEventType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6918-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6918-112">Specifica il tipo di modifiche di stato da segnalare.</span><span class="sxs-lookup"><span data-stu-id="f6918-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="f6918-113">Questo parametro è impostato su uno dei valori specificati nel [**tipo di \_ evento \_ SC**](sc-event-type.md).</span><span class="sxs-lookup"><span data-stu-id="f6918-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="f6918-114">Il comportamento di questa funzione è diverso a seconda del tipo di evento, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f6918-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="f6918-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f6918-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="f6918-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f6918-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="f6918-117"><dt>**SC \_ \_ \_ Modifica database evento**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6918-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f6918-118">Un servizio è stato aggiunto o eliminato.</span><span class="sxs-lookup"><span data-stu-id="f6918-118">A service has been added or deleted.</span></span> <span data-ttu-id="f6918-119">Il parametro *hService* deve essere un handle per SCM.</span><span class="sxs-lookup"><span data-stu-id="f6918-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="f6918-120"><dt>**SC \_ \_ \_ Modifica proprietà evento**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6918-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f6918-121">Una o più proprietà del servizio sono state aggiornate.</span><span class="sxs-lookup"><span data-stu-id="f6918-121">One or more service properties have been updated.</span></span> <span data-ttu-id="f6918-122">Il parametro *hService* deve essere un handle per il servizio.</span><span class="sxs-lookup"><span data-stu-id="f6918-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="f6918-123"><dt>**SC \_ \_ \_ Modifica stato evento**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6918-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="f6918-124">Lo stato di un servizio è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f6918-124">The status of a service has changed.</span></span> <span data-ttu-id="f6918-125">Il parametro *hService* deve essere un handle per il servizio.</span><span class="sxs-lookup"><span data-stu-id="f6918-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="f6918-126">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6918-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6918-127">Specifica la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f6918-127">Specifies the callback function.</span></span> <span data-ttu-id="f6918-128">Il callback deve essere definito come avente un tipo **di \_ \_ callback di notifica SC**.</span><span class="sxs-lookup"><span data-stu-id="f6918-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="f6918-129">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f6918-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f6918-130">*pCallbackContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f6918-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6918-131">Puntatore che rappresenta il contesto per questo callback di notifica.</span><span class="sxs-lookup"><span data-stu-id="f6918-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="f6918-132">*pSubscription* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f6918-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6918-133">Restituisce un puntatore alla sottoscrizione risultante dalla registrazione del callback di notifica.</span><span class="sxs-lookup"><span data-stu-id="f6918-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="f6918-134">Il chiamante è responsabile della chiamata di [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) per interrompere la ricezione delle notifiche.</span><span class="sxs-lookup"><span data-stu-id="f6918-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6918-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6918-135">Return value</span></span>

<span data-ttu-id="f6918-136">Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="f6918-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="f6918-137">Se la funzione ha esito negativo, il valore restituito è uno dei [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6918-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6918-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6918-138">Remarks</span></span>

<span data-ttu-id="f6918-139">La funzione di callback viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="f6918-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="f6918-140">La funzione di callback riceve un puntatore al contesto fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="f6918-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="f6918-141">Il callback viene richiamato in seguito all'evento di modifica dello stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f6918-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="f6918-142">Quando viene richiamato, il callback viene fornito con una maschera di maschera dei valori del **servizio \_ Notify \_ \* xxx**\* che indica il tipo di modifica dello stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f6918-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="f6918-143">Quando il callback viene fornito con zero invece di un valore valido per il \*\*servizio \_ Notify \_ \* xxx\*\*\*, l'applicazione deve verificare cosa è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f6918-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="f6918-144">La funzione di callback non deve bloccare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f6918-144">The callback function must not block execution.</span></span> <span data-ttu-id="f6918-145">Se si prevede che l'esecuzione della funzione di callback abbia tempo, eseguire l'offload del lavoro eseguito nella funzione di callback in un thread separato tramite l'accodamento di un elemento di lavoro a un thread in un pool di thread.</span><span class="sxs-lookup"><span data-stu-id="f6918-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="f6918-146">Alcuni tipi di lavoro che possono rendere la funzione di callback possono richiedere tempo, ad esempio l'esecuzione di operazioni di I/O di file, l'attesa di un evento e la creazione di chiamate a procedure remote esterne.</span><span class="sxs-lookup"><span data-stu-id="f6918-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6918-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6918-147">Requirements</span></span>



| <span data-ttu-id="f6918-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6918-148">Requirement</span></span> | <span data-ttu-id="f6918-149">Valore</span><span class="sxs-lookup"><span data-stu-id="f6918-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6918-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6918-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f6918-151">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6918-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f6918-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6918-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f6918-153">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6918-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6918-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6918-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6918-155"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6918-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6918-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f6918-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6918-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6918-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6918-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6918-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6918-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="f6918-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="f6918-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="f6918-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="f6918-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="f6918-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="f6918-162">**UnsubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="f6918-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="f6918-163">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="f6918-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 


---
description: 'Altre informazioni su: funzione JetSetLS'
title: Funzione JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525555"
---
# <a name="jetsetls-function"></a><span data-ttu-id="08c9a-103">Funzione JetSetLS</span><span class="sxs-lookup"><span data-stu-id="08c9a-103">JetSetLS Function</span></span>


<span data-ttu-id="08c9a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="08c9a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="08c9a-105">Funzione JetSetLS</span><span class="sxs-lookup"><span data-stu-id="08c9a-105">JetSetLS Function</span></span>

<span data-ttu-id="08c9a-106">La funzione **JetSetLS** consente all'applicazione di associare un handle di contesto noto come archiviazione locale con un cursore o la tabella associata a tale cursore.</span><span class="sxs-lookup"><span data-stu-id="08c9a-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="08c9a-107">Questo handle di contesto può essere utilizzato dall'applicazione per archiviare dati ausiliari associati a un cursore o a una tabella.</span><span class="sxs-lookup"><span data-stu-id="08c9a-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="08c9a-108">In seguito, l'applicazione riceve una notifica tramite un callback di runtime quando è necessario rilasciare l'handle del contesto.</span><span class="sxs-lookup"><span data-stu-id="08c9a-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="08c9a-109">Ciò consente di associare lo stato allocato in modo dinamico a un cursore o a una tabella.</span><span class="sxs-lookup"><span data-stu-id="08c9a-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="08c9a-110">**Windows XP:**  **JetSetLS** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08c9a-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="08c9a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="08c9a-111">Parameters</span></span>

<span data-ttu-id="08c9a-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="08c9a-112">*sesid*</span></span>

<span data-ttu-id="08c9a-113">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="08c9a-113">The session to use for this call.</span></span>

<span data-ttu-id="08c9a-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="08c9a-114">*tableid*</span></span>

<span data-ttu-id="08c9a-115">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="08c9a-115">The cursor to use for this call.</span></span>

<span data-ttu-id="08c9a-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="08c9a-116">*ls*</span></span>

<span data-ttu-id="08c9a-117">Handle di contesto da associare al cursore o alla tabella.</span><span class="sxs-lookup"><span data-stu-id="08c9a-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="08c9a-118">Quando si specifica JET_bitLSReset, il valore effettivo di questo parametro viene ignorato e viene utilizzato JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="08c9a-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="08c9a-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="08c9a-119">*grbit*</span></span>

<span data-ttu-id="08c9a-120">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="08c9a-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08c9a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="08c9a-121">Value</span></span></p></th>
<th><p><span data-ttu-id="08c9a-122">Significato</span><span class="sxs-lookup"><span data-stu-id="08c9a-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="08c9a-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="08c9a-124">Questa opzione indica che l'handle di contesto deve essere associato al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="08c9a-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="08c9a-125">Se non viene specificato né JET_bitLSCursor né JET_bitLSTable, JET_bitLSCursor si presume.</span><span class="sxs-lookup"><span data-stu-id="08c9a-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="08c9a-126">Non è consentito usare questa opzione con JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="08c9a-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="08c9a-127">L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="08c9a-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="08c9a-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="08c9a-129">Questa opzione indica che l'handle del contesto specificato deve essere ignorato e che l'handle di contesto per l'oggetto scelto deve essere reimpostato su JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="08c9a-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="08c9a-130">È importante tenere presente che questa azione non comporterà la pulizia del valore precedente dell'handle di contesto per l'oggetto scelto da parte di un callback.</span><span class="sxs-lookup"><span data-stu-id="08c9a-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="08c9a-131">La pulizia corretta dell'handle di contesto precedente può essere eseguita usando <a href="gg269234(v=exchg.10).md">JetGetLS</a> con JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="08c9a-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="08c9a-132">Per ulteriori informazioni, vedere <a href="gg269234(v=exchg.10).md">JetGetLS</a> .</span><span class="sxs-lookup"><span data-stu-id="08c9a-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="08c9a-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="08c9a-134">Questa opzione indica che l'handle di contesto deve essere associato alla tabella associata al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="08c9a-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="08c9a-135">Non è consentito usare questa opzione con JET_bitLSCursor.</span><span class="sxs-lookup"><span data-stu-id="08c9a-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="08c9a-136">L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="08c9a-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="08c9a-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08c9a-137">Return Value</span></span>

<span data-ttu-id="08c9a-138">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="08c9a-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="08c9a-139">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="08c9a-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08c9a-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="08c9a-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="08c9a-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08c9a-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="08c9a-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="08c9a-143">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="08c9a-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="08c9a-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="08c9a-145">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="08c9a-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="08c9a-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="08c9a-147">Una delle opzioni richieste non è valida, è stata usata in modo errato o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="08c9a-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="08c9a-148">Questo problema può verificarsi per <strong>JetSetLS</strong> quando vengono specificati entrambi JET_bitLSCursor e JET_bitLSTable.</span><span class="sxs-lookup"><span data-stu-id="08c9a-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="08c9a-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="08c9a-150">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="08c9a-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="08c9a-151">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="08c9a-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="08c9a-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="08c9a-153">Impossibile associare l'handle del contesto specificato all'oggetto richiesto perché è già associato a un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="08c9a-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="08c9a-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="08c9a-155">Impossibile associare l'handle del contesto specificato all'oggetto richiesto perché il callback di runtime non è stato configurato per l'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="08c9a-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="08c9a-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="08c9a-157">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="08c9a-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="08c9a-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="08c9a-159">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="08c9a-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="08c9a-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="08c9a-161">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="08c9a-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="08c9a-162">In caso di esito positivo, l'handle di contesto specificato è stato associato correttamente all'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="08c9a-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="08c9a-163">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="08c9a-163">No change to the database state will occur.</span></span>

<span data-ttu-id="08c9a-164">In caso di errore, non sono state apportate modifiche allo stato dell'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="08c9a-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="08c9a-165">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="08c9a-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="08c9a-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="08c9a-166">Remarks</span></span>

<span data-ttu-id="08c9a-167">L'archiviazione locale per un cursore o una tabella deve essere visualizzata come cache volatile.</span><span class="sxs-lookup"><span data-stu-id="08c9a-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="08c9a-168">L'applicazione deve prima provare a recuperare l'handle del contesto usando [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="08c9a-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="08c9a-169">Se il valore non è impostato (ovvero è JET_LSNil), l'applicazione deve creare un nuovo contesto e caricarlo nella cache usando **JetSetLS**.</span><span class="sxs-lookup"><span data-stu-id="08c9a-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="08c9a-170">L'applicazione può ripulire la cache utilizzando una chiamata a [JetGetLS](./jetgetls-function.md) con JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="08c9a-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="08c9a-171">Se il motore di database elimina la cache, verrà generato un callback di runtime per concedere all'applicazione la possibilità di pulire tale contesto.</span><span class="sxs-lookup"><span data-stu-id="08c9a-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="08c9a-172">Il tipo di callback verrà JET_cbtypFreeCursorLS per un handle di contesto associato a un cursore e JET_cbtypFreeTableLS per un handle di contesto associato a una tabella.</span><span class="sxs-lookup"><span data-stu-id="08c9a-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="08c9a-173">In entrambi i casi, l'handle di contesto verrà passato come pvArg1.</span><span class="sxs-lookup"><span data-stu-id="08c9a-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="08c9a-174">Per ulteriori informazioni, vedere [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="08c9a-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="08c9a-175">Il callback di runtime deve essere configurato correttamente per l'istanza associata alla sessione specificata prima di poter usare l'archiviazione locale.</span><span class="sxs-lookup"><span data-stu-id="08c9a-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="08c9a-176">Questo callback può essere impostato usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramRuntimeCallback](./callback-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="08c9a-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="08c9a-177">Per ulteriori informazioni, vedere [JetSetSystemParameter](./jetsetsystemparameter-function.md) e [JET_paramRuntimeCallback](./callback-parameters.md) nei parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="08c9a-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="08c9a-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08c9a-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-179"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="08c9a-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="08c9a-180">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08c9a-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="08c9a-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="08c9a-182">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="08c9a-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-183"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="08c9a-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="08c9a-184">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="08c9a-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c9a-185"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="08c9a-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="08c9a-186">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="08c9a-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c9a-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="08c9a-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="08c9a-188">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="08c9a-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="08c9a-189">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="08c9a-189">See Also</span></span>

[<span data-ttu-id="08c9a-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="08c9a-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="08c9a-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="08c9a-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="08c9a-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="08c9a-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="08c9a-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="08c9a-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="08c9a-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="08c9a-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="08c9a-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="08c9a-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="08c9a-196">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="08c9a-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="08c9a-197">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="08c9a-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="08c9a-198">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="08c9a-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

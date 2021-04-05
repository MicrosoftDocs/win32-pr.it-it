---
description: 'Altre informazioni su: funzione JetDupSession'
title: JetDupSession (funzione)
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884197"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="23694-103">JetDupSession (funzione)</span><span class="sxs-lookup"><span data-stu-id="23694-103">JetDupSession Function</span></span>


<span data-ttu-id="23694-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="23694-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="23694-105">JetDupSession (funzione)</span><span class="sxs-lookup"><span data-stu-id="23694-105">JetDupSession Function</span></span>

<span data-ttu-id="23694-106">La funzione **JetDupSession** avvia una sessione e Inizializza e restituisce un handle di sessione ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="23694-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="23694-107">Le sessioni controllano l'accesso al database e vengono utilizzate per controllare l'ambito delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="23694-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="23694-108">La sessione può essere utilizzata per avviare, eseguire il commit o interrompere le transazioni.</span><span class="sxs-lookup"><span data-stu-id="23694-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="23694-109">La sessione viene inoltre utilizzata per il fissaggio, la creazione o l'apertura di un database.</span><span class="sxs-lookup"><span data-stu-id="23694-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="23694-110">La sessione viene utilizzata come contesto per tutte le operazioni DDL e DML.</span><span class="sxs-lookup"><span data-stu-id="23694-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="23694-111">Per aumentare la concorrenza e l'accesso parallelo al database, è possibile iniziare più sessioni.</span><span class="sxs-lookup"><span data-stu-id="23694-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="23694-112">**Nota** Questa API agirà in tutti i modi come un [JetBeginSession](./jetbeginsession-function.md) chiamato nell'istanza della sessione passata.</span><span class="sxs-lookup"><span data-stu-id="23694-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="23694-113">Questa funzione non è consigliata, [JetBeginSession](./jetbeginsession-function.md) è preferibile.</span><span class="sxs-lookup"><span data-stu-id="23694-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="23694-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="23694-114">Parameters</span></span>

<span data-ttu-id="23694-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="23694-115">*sesid*</span></span>

<span data-ttu-id="23694-116">Sessione da utilizzare come origine per la duplicazione o l'inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="23694-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="23694-117">*psesid*</span><span class="sxs-lookup"><span data-stu-id="23694-117">*psesid*</span></span>

<span data-ttu-id="23694-118">Un puntatore alla variabile che l'handle di sessione Inizializza per restituire correttamente.</span><span class="sxs-lookup"><span data-stu-id="23694-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="23694-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23694-119">Return Value</span></span>

<span data-ttu-id="23694-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="23694-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="23694-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="23694-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23694-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="23694-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="23694-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23694-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23694-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="23694-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="23694-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="23694-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23694-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="23694-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="23694-127">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="23694-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23694-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="23694-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="23694-129">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="23694-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="23694-130">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="23694-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23694-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="23694-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="23694-132">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="23694-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23694-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="23694-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="23694-134">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="23694-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23694-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="23694-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="23694-136">L'operazione non è riuscita perché non è stato possibile allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="23694-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23694-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="23694-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="23694-138">Il numero di sessioni consentite dal motore per l'avvio del client è limitato.</span><span class="sxs-lookup"><span data-stu-id="23694-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="23694-139">Questo valore può essere modificato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la costante <em>JET_paramMaxSessions</em> .</span><span class="sxs-lookup"><span data-stu-id="23694-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="23694-140">Il numero predefinito di sessioni è 16.</span><span class="sxs-lookup"><span data-stu-id="23694-140">The default number of sessions is 16.</span></span> <span data-ttu-id="23694-141">Per informazioni dettagliate sui <em>JET_paramMaxSessions</em>, vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a> .</span><span class="sxs-lookup"><span data-stu-id="23694-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23694-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="23694-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="23694-143">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="23694-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23694-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="23694-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="23694-145">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="23694-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="23694-146">In seguito all'esito positivo, l'handle di sessione viene inizializzato e può essere utilizzato per le operazioni di database.</span><span class="sxs-lookup"><span data-stu-id="23694-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="23694-147">In caso di errore, non sono disponibili sessioni o non è stato possibile inizializzare una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="23694-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="23694-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23694-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23694-149"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="23694-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="23694-150">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="23694-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23694-151"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="23694-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="23694-152">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="23694-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23694-153"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="23694-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="23694-154">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="23694-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23694-155"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="23694-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="23694-156">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="23694-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23694-157"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="23694-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="23694-158">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="23694-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="23694-159">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="23694-159">See Also</span></span>

[<span data-ttu-id="23694-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="23694-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="23694-161">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="23694-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="23694-162">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="23694-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="23694-163">JetStopService</span><span class="sxs-lookup"><span data-stu-id="23694-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="23694-164">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="23694-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

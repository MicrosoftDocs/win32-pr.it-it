---
description: 'Altre informazioni su: funzione JetSetSessionContext'
title: JetSetSessionContext (funzione)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307807"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="76168-103">JetSetSessionContext (funzione)</span><span class="sxs-lookup"><span data-stu-id="76168-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="76168-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="76168-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="76168-105">JetSetSessionContext (funzione)</span><span class="sxs-lookup"><span data-stu-id="76168-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="76168-106">La funzione **JetSetSessionContext** associa una sessione al thread corrente usando l'handle di contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="76168-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="76168-107">Questa associazione esegue l'override del requisito del motore predefinito che una transazione per una determinata sessione deve essere interamente eseguita sullo stesso thread.</span><span class="sxs-lookup"><span data-stu-id="76168-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="76168-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="76168-108">Parameters</span></span>

<span data-ttu-id="76168-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="76168-109">*sesid*</span></span>

<span data-ttu-id="76168-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="76168-110">The session to use for this call.</span></span>

<span data-ttu-id="76168-111">*ulContext*</span><span class="sxs-lookup"><span data-stu-id="76168-111">*ulContext*</span></span>

<span data-ttu-id="76168-112">Identificatore univoco a cui verrà associata la sessione.</span><span class="sxs-lookup"><span data-stu-id="76168-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="76168-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76168-113">Return Value</span></span>

<span data-ttu-id="76168-114">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="76168-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="76168-115">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="76168-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76168-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="76168-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="76168-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76168-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76168-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="76168-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="76168-119">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="76168-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76168-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="76168-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="76168-121">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="76168-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76168-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="76168-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="76168-123">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="76168-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="76168-124"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76168-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76168-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="76168-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="76168-126">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="76168-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="76168-127">Questo errore viene restituito da <strong>JetSetSessionContext</strong> nelle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="76168-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="76168-128"><em>ulContext</em> è null</span><span class="sxs-lookup"><span data-stu-id="76168-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="76168-129"><em>ulContext</em> è-1</span><span class="sxs-lookup"><span data-stu-id="76168-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76168-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="76168-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="76168-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="76168-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76168-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="76168-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="76168-133">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="76168-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76168-134">JET_errSessionContextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="76168-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="76168-135">Impossibile associare la sessione al thread corrente perché è già stata associata a un thread.</span><span class="sxs-lookup"><span data-stu-id="76168-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76168-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="76168-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="76168-137">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="76168-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="76168-138">Se questa funzione ha esito positivo, la sessione verrà associata al thread corrente.</span><span class="sxs-lookup"><span data-stu-id="76168-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="76168-139">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="76168-139">No change to the database state will occur.</span></span>

<span data-ttu-id="76168-140">Se questa funzione ha esito negativo, lo stato della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="76168-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="76168-141">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="76168-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="76168-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="76168-142">Remarks</span></span>

<span data-ttu-id="76168-143">Una sessione è in genere associata a un thread specifico per la durata di una transazione.</span><span class="sxs-lookup"><span data-stu-id="76168-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="76168-144">Questo comportamento è progettato per aiutare le applicazioni a rilevare ed evitare la condivisione concettualmente non consigliata di una singola sessione tra più thread.</span><span class="sxs-lookup"><span data-stu-id="76168-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="76168-145">In alcuni casi questo semplice controllo non funziona con l'architettura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76168-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="76168-146">Se, ad esempio, l'applicazione ospita oggetti lato server utilizzando un pool di thread e le transazioni si estendono su più chiamate server a un determinato oggetto, questa protezione potrebbe causare l'esito negativo di alcune chiamate con JET_errSessionSharingViolation anche se il modello di utilizzo è corretto.</span><span class="sxs-lookup"><span data-stu-id="76168-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="76168-147">Questa situazione è comune per i server oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="76168-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="76168-148">**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) risolvono questo problema rendendo il controllo della condivisione della sessione leggermente più flessibile.</span><span class="sxs-lookup"><span data-stu-id="76168-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="76168-149">Quando l'applicazione inizia a eseguire una serie di chiamate API ESE usando una determinata sessione, imposta prima di tutto il contesto della sessione su un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="76168-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="76168-150">Questa azione associa la sessione al thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="76168-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="76168-151">Nell'esempio specificato, questo contesto può essere l'indirizzo dell'oggetto che contiene l'handle della sessione JET.</span><span class="sxs-lookup"><span data-stu-id="76168-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="76168-152">Una volta effettuate le chiamate all'API ESE, l'applicazione Reimposta il contesto della sessione.</span><span class="sxs-lookup"><span data-stu-id="76168-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="76168-153">Questa azione annulla l'associazione della sessione dal thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="76168-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="76168-154">L'oggetto e la relativa sessione possono quindi essere utilizzati da un altro thread anche se la sessione dispone di una transazione attiva.</span><span class="sxs-lookup"><span data-stu-id="76168-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="76168-155">È importante notare che **JetSetSessionContext** deve essere chiamato prima di aprire una transazione nella sessione o l'associazione non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="76168-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="76168-156">**JetSetSessionContext** è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="76168-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="76168-157">Più thread possono provare a impostare un contesto di thread nella stessa sessione nello stesso momento e solo uno vincerà.</span><span class="sxs-lookup"><span data-stu-id="76168-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="76168-158">Questo fatto può essere utilizzato dall'applicazione come mezzo per allocare una sessione da un pool senza archiviare lo stato esterno sulla relativa allocazione.</span><span class="sxs-lookup"><span data-stu-id="76168-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="76168-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76168-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76168-160"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="76168-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="76168-161">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="76168-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76168-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="76168-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="76168-163">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="76168-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76168-164"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="76168-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="76168-165">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="76168-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76168-166"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="76168-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="76168-167">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="76168-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76168-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="76168-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="76168-169">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="76168-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="76168-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="76168-170">See Also</span></span>

[<span data-ttu-id="76168-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="76168-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="76168-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="76168-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="76168-173">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="76168-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="76168-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="76168-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="76168-175">JetStopService</span><span class="sxs-lookup"><span data-stu-id="76168-175">JetStopService</span></span>](./jetstopservice-function.md)

---
description: 'Altre informazioni su: funzione JetSetSessionParameter'
title: JetSetSessionParameter (funzione)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966545"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="db705-103">JetSetSessionParameter (funzione)</span><span class="sxs-lookup"><span data-stu-id="db705-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="db705-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="db705-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="db705-105">La funzione **JetSetSessionParameter** configura il motore di database.</span><span class="sxs-lookup"><span data-stu-id="db705-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="db705-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db705-106">Parameters</span></span>

<span data-ttu-id="db705-107">*sesid*</span><span class="sxs-lookup"><span data-stu-id="db705-107">*sesid*</span></span>

<span data-ttu-id="db705-108">Specifica la sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="db705-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="db705-109">Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="db705-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="db705-110">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="db705-110">*sesparamid*</span></span>

<span data-ttu-id="db705-111">ID del parametro della sessione da impostare.</span><span class="sxs-lookup"><span data-stu-id="db705-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="db705-112">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="db705-112">*pvParam*</span></span>

<span data-ttu-id="db705-113">Dati da impostare in questo parametro della sessione.</span><span class="sxs-lookup"><span data-stu-id="db705-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="db705-114">*cbParam*</span><span class="sxs-lookup"><span data-stu-id="db705-114">*cbParam*</span></span>

<span data-ttu-id="db705-115">Dimensione dei dati forniti.</span><span class="sxs-lookup"><span data-stu-id="db705-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="db705-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db705-116">Return value</span></span>

<span data-ttu-id="db705-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="db705-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="db705-118">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="db705-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db705-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="db705-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="db705-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db705-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db705-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="db705-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="db705-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="db705-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="db705-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="db705-124">L'istanza è stata inizializzata tramite una chiamata alla funzione <a href="gg294068(v=exchg.10).md">JetInit</a> e questa operazione non può essere eseguita di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="db705-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="db705-125">Questa situazione può verificarsi quando viene effettuato un tentativo di configurare un parametro di sistema dopo che una modifica nel valore del parametro non può più influire sullo stato del motore di database.</span><span class="sxs-lookup"><span data-stu-id="db705-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="db705-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="db705-127">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="db705-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="db705-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="db705-129">I parametri specificati per l'indice di tupla non sono validi.</span><span class="sxs-lookup"><span data-stu-id="db705-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="db705-130">Questo errore viene restituito solo quando il parametro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>o <em>JET_paramIndexTuplesToIndexMax</em> è impostato su un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="db705-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="db705-131">Per informazioni su questi parametri, vedere <a href="gg294119(v=exchg.10).md">parametri di indice</a>.</span><span class="sxs-lookup"><span data-stu-id="db705-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="db705-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="db705-133">Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="db705-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="db705-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="db705-135">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="db705-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="db705-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="db705-137">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="db705-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="db705-138">Questa situazione può verificarsi quando si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="db705-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="db705-139">L'ID parametro di sistema specificato non è valido o non è supportato.</span><span class="sxs-lookup"><span data-stu-id="db705-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="db705-140">È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con una stringa la cui lunghezza non era compresa nell'intervallo valido per il parametro.</span><span class="sxs-lookup"><span data-stu-id="db705-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="db705-141">È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della rappresentazione del percorso assoluto non rientra nell'intervallo valido per il parametro.</span><span class="sxs-lookup"><span data-stu-id="db705-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="db705-142">È stato effettuato un tentativo di impostare un parametro di sistema con valori integer con un numero intero non compreso nell'intervallo valido per il parametro.</span><span class="sxs-lookup"><span data-stu-id="db705-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="db705-143">È stato effettuato un tentativo di impostare JET_paramUnicodeIndexDefault con un puntatore <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> null, un LCID non valido o un set di flag <strong>LCMapString</strong> non supportato.</span><span class="sxs-lookup"><span data-stu-id="db705-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="db705-144">Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="db705-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="db705-145">È stato effettuato un tentativo di impostare un parametro di sistema dopo che è stata chiamata la funzione <a href="gg294068(v=exchg.10).md">JetInit</a> , il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</span><span class="sxs-lookup"><span data-stu-id="db705-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="db705-146">Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per il parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="db705-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="db705-147">Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per il parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="db705-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="db705-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="db705-149">Il percorso di file system specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="db705-149">The specified file system path was invalid.</span></span> <span data-ttu-id="db705-150">Questo errore può essere restituito da <strong>JetSetSessionParameter</strong> solo quando si impostano parametri di sistema che rappresentano file System percorsi.</span><span class="sxs-lookup"><span data-stu-id="db705-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="db705-151">Ad esempio, il parametro <em>JET_paramSystemPath</em> può restituire l'errore.</span><span class="sxs-lookup"><span data-stu-id="db705-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="db705-152">Per informazioni su questo parametro, vedere <a href="gg269235(v=exchg.10).md">parametri del log delle transazioni</a>.</span><span class="sxs-lookup"><span data-stu-id="db705-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="db705-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="db705-154">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="db705-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="db705-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="db705-156">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="db705-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="db705-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="db705-158">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="db705-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="db705-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="db705-160">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="db705-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="db705-161">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="db705-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="db705-162">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="db705-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="db705-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="db705-164">L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="db705-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="db705-165">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="db705-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="db705-166">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="db705-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db705-167">In seguito all'esito positivo, il parametro di sistema verrà impostato sul valore fornito.</span><span class="sxs-lookup"><span data-stu-id="db705-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="db705-168">In caso di errore, il valore del parametro di sistema rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="db705-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="db705-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db705-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db705-170"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="db705-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="db705-171">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="db705-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="db705-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="db705-173">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="db705-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-174"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="db705-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="db705-175">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="db705-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db705-176"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="db705-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="db705-177">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="db705-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db705-178"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="db705-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="db705-179">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="db705-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="db705-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db705-180">See also</span></span>

[<span data-ttu-id="db705-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="db705-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="db705-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="db705-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="db705-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="db705-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="db705-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="db705-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="db705-185">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="db705-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="db705-186">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="db705-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="db705-187">JetInit</span><span class="sxs-lookup"><span data-stu-id="db705-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="db705-188">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="db705-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

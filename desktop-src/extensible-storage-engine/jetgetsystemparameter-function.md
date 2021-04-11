---
description: 'Altre informazioni su: funzione JetGetSystemParameter'
title: JetGetSystemParameter (funzione)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233356"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="28023-103">JetGetSystemParameter (funzione)</span><span class="sxs-lookup"><span data-stu-id="28023-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="28023-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="28023-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="28023-105">JetGetSystemParameter (funzione)</span><span class="sxs-lookup"><span data-stu-id="28023-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="28023-106">La funzione **JetGetSystemParameter** legge le numerose impostazioni di configurazione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="28023-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="28023-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="28023-107">Parameters</span></span>

<span data-ttu-id="28023-108">*istanza*</span><span class="sxs-lookup"><span data-stu-id="28023-108">*instance*</span></span>

<span data-ttu-id="28023-109">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="28023-109">The instance to use for this call.</span></span>

<span data-ttu-id="28023-110">Per Windows 2000, questo parametro viene ignorato e deve essere sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="28023-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="28023-111">Per Windows XP e versioni successive, questo parametro è leggermente sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="28023-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="28023-112">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere **null** o può contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="28023-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="28023-113">In entrambi i casi, tutte le impostazioni dei parametri di sistema vengono lette da un'istanza.</span><span class="sxs-lookup"><span data-stu-id="28023-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="28023-114">Se il motore funziona in modalità a istanze diverse, questo parametro può essere **null** o un puntatore a un'istanza creata utilizzando [JetInit](./jetinit-function.md) o [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="28023-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="28023-115">Se questo parametro è **null** , viene letta l'impostazione del parametro di sistema globale (o default).</span><span class="sxs-lookup"><span data-stu-id="28023-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="28023-116">Quando questo parametro è un'istanza, viene letta l'impostazione del parametro di sistema per tale istanza.</span><span class="sxs-lookup"><span data-stu-id="28023-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="28023-117">*sesid*</span><span class="sxs-lookup"><span data-stu-id="28023-117">*sesid*</span></span>

<span data-ttu-id="28023-118">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="28023-118">The session to use for this call.</span></span>

<span data-ttu-id="28023-119">Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="28023-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="28023-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="28023-120">*paramid*</span></span>

<span data-ttu-id="28023-121">ID del parametro di sistema che verrà letto.</span><span class="sxs-lookup"><span data-stu-id="28023-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="28023-122">Per un elenco completo dei parametri di sistema e delle relative proprietà, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="28023-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="28023-123">*plParam*</span><span class="sxs-lookup"><span data-stu-id="28023-123">*plParam*</span></span>

<span data-ttu-id="28023-124">Buffer di output che riceve il valore del parametro di sistema selezionato se tale parametro di sistema è di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="28023-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="28023-125">*szParam*</span><span class="sxs-lookup"><span data-stu-id="28023-125">*szParam*</span></span>

<span data-ttu-id="28023-126">Buffer di output che riceve il valore del parametro di sistema selezionato se tale parametro di sistema è di tipo String.</span><span class="sxs-lookup"><span data-stu-id="28023-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="28023-127">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="28023-127">*cbMax*</span></span>

<span data-ttu-id="28023-128">Dimensione massima in byte del buffer di output della stringa.</span><span class="sxs-lookup"><span data-stu-id="28023-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="28023-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28023-129">Return Value</span></span>

<span data-ttu-id="28023-130">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="28023-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="28023-131">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="28023-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28023-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="28023-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="28023-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28023-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28023-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="28023-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="28023-135">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="28023-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="28023-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="28023-137">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="28023-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="28023-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="28023-139">Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="28023-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="28023-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="28023-141">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="28023-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="28023-142">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="28023-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="28023-144">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="28023-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="28023-145">Questo problema può verificarsi per <strong>JetGetSystemParameter</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="28023-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="28023-146">L'ID parametro di sistema specificato non è valido o non è supportato.</span><span class="sxs-lookup"><span data-stu-id="28023-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="28023-147">Per il parametro di sistema specificato è necessario fornire il buffer di output di tipo integer e il puntatore del buffer di output è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="28023-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="28023-148">Il parametro di sistema specificato richiede che venga fornito un buffer di output di stringa e che il puntatore del buffer di output sia <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="28023-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="28023-149"><strong>Windows Vista:  </strong> Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="28023-150">Il parametro di sistema specificato richiede che venga fornito un buffer di output di stringa e che la dimensione del buffer di output sia troppo piccola per accettare una stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="28023-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="28023-151"><strong>Windows Vista:  </strong> Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="28023-152">Impossibile leggere il parametro di sistema specificato perché è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="28023-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="28023-153">Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di lettura di un valore specifico dell'istanza per il parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="28023-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="28023-154">Questa operazione può essere eseguita solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="28023-155">Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di lettura del valore globale per il parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="28023-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="28023-156">Questa operazione può essere eseguita solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="28023-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="28023-158">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="28023-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="28023-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="28023-160">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="28023-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="28023-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="28023-162">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="28023-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="28023-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="28023-164">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="28023-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="28023-165">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="28023-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="28023-166">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="28023-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="28023-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="28023-168">L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="28023-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="28023-169">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="28023-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="28023-170">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="28023-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="28023-171"><strong>Windows Vista:  </strong> Questo errore verrà restituito solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="28023-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="28023-173">L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intera impostazione del parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="28023-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="28023-174">Il buffer di output è stato riempito con la maggior parte delle impostazioni del parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="28023-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="28023-175">Se il buffer di output è di almeno un carattere di lunghezza, la stringa in tale buffer di output sarà terminata con null.</span><span class="sxs-lookup"><span data-stu-id="28023-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="28023-176"><strong>Nota  </strong> Questo errore non viene restituito da tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="28023-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="28023-177">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="28023-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="28023-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="28023-179">L'operazione non è riuscita perché il buffer di output era troppo piccolo per ricevere l'intera impostazione del parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="28023-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="28023-180"><strong>Nota  </strong> Questo errore non viene restituito in alcuni casi per mantenere la compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="28023-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="28023-181">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="28023-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="28023-182"><strong>Windows Vista:  </strong> Questo errore verrà restituito solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="28023-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28023-183">In caso di esito positivo, il buffer di output appropriato per il parametro di sistema richiesto verrà impostato sul valore di tale parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="28023-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="28023-184">In caso di errore, lo stato dei buffer di output sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="28023-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="28023-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="28023-185">Remarks</span></span>

<span data-ttu-id="28023-186">Si è verificato un problema importante in questa API presente in tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="28023-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="28023-187">Se viene richiesto un parametro di sistema con un valore stringa e il buffer di output è troppo piccolo per ricevere l'intera impostazione del parametro di sistema, JET_wrnBufferTruncated non verrà restituito.</span><span class="sxs-lookup"><span data-stu-id="28023-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="28023-188">Viene invece restituito JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="28023-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="28023-189">Se la lunghezza della stringa restituita è uguale alla dimensione del buffer di output minore del carattere di terminazione **null** , il chiamante deve reagire come se JET_wrnBufferTruncated fosse stato restituito.</span><span class="sxs-lookup"><span data-stu-id="28023-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="28023-190">Se viene specificato un buffer di output di stringa di dimensioni zero, il chiamante deve reagire come se JET_errInvalidParameter fosse stato restituito.</span><span class="sxs-lookup"><span data-stu-id="28023-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="28023-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28023-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28023-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="28023-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="28023-193">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="28023-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="28023-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="28023-195">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="28023-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-196"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="28023-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="28023-197">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="28023-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-198"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="28023-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="28023-199">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="28023-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28023-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="28023-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="28023-201">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="28023-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28023-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="28023-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="28023-203">Implementato come <strong>JetGetSystemParameterW</strong> (Unicode) e <strong>JetGetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="28023-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="28023-204">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="28023-204">See Also</span></span>

[<span data-ttu-id="28023-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="28023-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="28023-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="28023-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="28023-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="28023-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="28023-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="28023-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="28023-209">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="28023-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="28023-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="28023-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="28023-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="28023-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="28023-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="28023-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="28023-213">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="28023-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)

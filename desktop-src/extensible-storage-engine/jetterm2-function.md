---
description: 'Altre informazioni su: funzione JetTerm2'
title: Funzione JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129718"
---
# <a name="jetterm2-function"></a><span data-ttu-id="5bac1-103">Funzione JetTerm2</span><span class="sxs-lookup"><span data-stu-id="5bac1-103">JetTerm2 Function</span></span>


<span data-ttu-id="5bac1-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5bac1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="5bac1-105">Funzione JetTerm2</span><span class="sxs-lookup"><span data-stu-id="5bac1-105">JetTerm2 Function</span></span>

<span data-ttu-id="5bac1-106">La funzione **JetTerm2** avvia l'arresto di un'istanza che è stata inizializzata da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="5bac1-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="5bac1-107">**JetTerm2** può anche eliminare un'istanza non inizializzata creata da [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="5bac1-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5bac1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bac1-108">Parameters</span></span>

<span data-ttu-id="5bac1-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="5bac1-109">*instance*</span></span>

<span data-ttu-id="5bac1-110">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5bac1-110">The instance to use for this call.</span></span>

<span data-ttu-id="5bac1-111">**Windows 2000:**  Questo parametro viene ignorato e deve essere sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="5bac1-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="5bac1-112">**Windows XP e versioni successive:**  Questo parametro è sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="5bac1-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="5bac1-113">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro potrebbe essere **null** o potrebbe contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="5bac1-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="5bac1-114">Se il motore funziona in modalità a istanze diverse, questo parametro deve essere un puntatore a un'istanza creata con [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="5bac1-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="5bac1-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5bac1-115">*grbit*</span></span>

<span data-ttu-id="5bac1-116">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5bac1-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bac1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5bac1-117">Value</span></span></p></th>
<th><p><span data-ttu-id="5bac1-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5bac1-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="5bac1-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="5bac1-120">Richiede che l'istanza venga arrestata in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="5bac1-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="5bac1-121">Eventuali operazioni di pulizia facoltative normalmente eseguite in background in fase di esecuzione vengono completate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5bac1-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="5bac1-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="5bac1-123">Richiede che l'istanza venga arrestata nel minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="5bac1-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="5bac1-124">Qualsiasi lavoro facoltativo che normalmente verrebbe eseguito in background in fase di esecuzione viene abbandonato.</span><span class="sxs-lookup"><span data-stu-id="5bac1-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="5bac1-125"><strong>Nota</strong>  Questa opzione può causare una perdita di spazio temporanea o permanente nel database.</span><span class="sxs-lookup"><span data-stu-id="5bac1-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="5bac1-126">Questo spazio perso può sempre essere recuperato tramite una deframmentazione non in linea del database.</span><span class="sxs-lookup"><span data-stu-id="5bac1-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="5bac1-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="5bac1-128">Richiede che l'istanza venga arrestata anche se è attualmente in corso un backup.</span><span class="sxs-lookup"><span data-stu-id="5bac1-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="5bac1-129">In genere, un backup in sospeso provocherebbe un errore di <a href="gg269298(v=exchg.10).md">JetTerm</a> con JET_errBackupInProgress.</span><span class="sxs-lookup"><span data-stu-id="5bac1-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="5bac1-130">Se questo parametro non è presente, il relativo valore si presume che sia JET_bitTermAbrupt.</span><span class="sxs-lookup"><span data-stu-id="5bac1-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="5bac1-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="5bac1-132">Richiede che l'istanza venga arrestata con tutti i database collegati rimasti in uno stato modificato.</span><span class="sxs-lookup"><span data-stu-id="5bac1-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="5bac1-133">Windows 7: JET_bitTermDirty è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5bac1-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5bac1-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bac1-134">Return Value</span></span>

<span data-ttu-id="5bac1-135">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5bac1-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5bac1-136">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5bac1-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bac1-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5bac1-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="5bac1-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bac1-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5bac1-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5bac1-140">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5bac1-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="5bac1-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="5bac1-142">Non è possibile completare l'operazione perché è in corso un'operazione di backup sull'istanza.</span><span class="sxs-lookup"><span data-stu-id="5bac1-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5bac1-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5bac1-144">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5bac1-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="5bac1-145">Questo errore viene restituito da <a href="gg269298(v=exchg.10).md">JetTerm</a> quando il motore è in modalità a istanze diverse e quando <em>pinstance</em> fa riferimento a un'istanza non valida.</span><span class="sxs-lookup"><span data-stu-id="5bac1-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="5bac1-146"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5bac1-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5bac1-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5bac1-148">Non è possibile completare l'operazione perché l'istanza non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="5bac1-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5bac1-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5bac1-150">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5bac1-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5bac1-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5bac1-152">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza.</span><span class="sxs-lookup"><span data-stu-id="5bac1-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="5bac1-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="5bac1-154">Impossibile arrestare l'istanza perché attualmente sono presenti sessioni con transazioni attive per l'istanza specificata.</span><span class="sxs-lookup"><span data-stu-id="5bac1-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="5bac1-155">Questo errore si verifica solo se viene utilizzata la JET_bitTermComplete.</span><span class="sxs-lookup"><span data-stu-id="5bac1-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5bac1-156">Se questa funzione ha esito positivo, l'istanza specificata verrà arrestata.</span><span class="sxs-lookup"><span data-stu-id="5bac1-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="5bac1-157">L'handle dell'istanza verrà inoltre chiuso e reso non disponibile a qualsiasi API che accetta un handle di istanza.</span><span class="sxs-lookup"><span data-stu-id="5bac1-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="5bac1-158">Verranno chiusi anche tutti gli altri oggetti associati all'istanza, ad esempio le sessioni.</span><span class="sxs-lookup"><span data-stu-id="5bac1-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="5bac1-159">Lo stato del file del checkpoint, dei file di log delle transazioni e dei file di database collegati all'istanza verrà modificato durante il processo di arresto.</span><span class="sxs-lookup"><span data-stu-id="5bac1-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="5bac1-160">Se questa funzione ha esito negativo a causa di un errore di utilizzo, l'istanza rimane in uno stato inizializzato e non vengono apportate modifiche.</span><span class="sxs-lookup"><span data-stu-id="5bac1-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="5bac1-161">In caso contrario, l'istanza viene ancora arrestata come indicato per il caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5bac1-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="5bac1-162">La differenza consiste nel fatto che l'istanza dovrà eseguire il ripristino di arresto anomalo del sistema alla successiva inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="5bac1-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="5bac1-163">Il motore tenterà di scaricare quanti più dati possibile per ridurre al minimo la quantità di ripristino richiesta.</span><span class="sxs-lookup"><span data-stu-id="5bac1-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="5bac1-164">A livello concettuale, questo errore di [JetTerm](./jetterm-function.md) non è diverso da un arresto anomalo del processo.</span><span class="sxs-lookup"><span data-stu-id="5bac1-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5bac1-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bac1-165">Remarks</span></span>

<span data-ttu-id="5bac1-166">Vedere [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="5bac1-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5bac1-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bac1-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5bac1-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5bac1-169">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5bac1-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5bac1-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5bac1-171">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5bac1-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-172"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5bac1-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5bac1-173">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5bac1-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bac1-174"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5bac1-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5bac1-175">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5bac1-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5bac1-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5bac1-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5bac1-177">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5bac1-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5bac1-178">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5bac1-178">See Also</span></span>

[<span data-ttu-id="5bac1-179">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="5bac1-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="5bac1-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="5bac1-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="5bac1-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5bac1-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5bac1-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5bac1-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5bac1-183">JetInit</span><span class="sxs-lookup"><span data-stu-id="5bac1-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="5bac1-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5bac1-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5bac1-185">JetTerm</span><span class="sxs-lookup"><span data-stu-id="5bac1-185">JetTerm</span></span>](./jetterm-function.md)

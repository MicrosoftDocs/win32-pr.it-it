---
description: 'Altre informazioni su: funzione JetTerm'
title: Funzione JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306210"
---
# <a name="jetterm-function"></a><span data-ttu-id="75d21-103">Funzione JetTerm</span><span class="sxs-lookup"><span data-stu-id="75d21-103">JetTerm Function</span></span>


<span data-ttu-id="75d21-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="75d21-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="75d21-105">Funzione JetTerm</span><span class="sxs-lookup"><span data-stu-id="75d21-105">JetTerm Function</span></span>

<span data-ttu-id="75d21-106">La funzione **JetTerm** avvia l'arresto di un'istanza che è stata inizializzata da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="75d21-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="75d21-107">**JetTerm** può essere utilizzato anche per eliminare un'istanza non inizializzata creata da [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="75d21-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="75d21-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75d21-108">Parameters</span></span>

<span data-ttu-id="75d21-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="75d21-109">*instance*</span></span>

<span data-ttu-id="75d21-110">Specifica l'istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="75d21-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="75d21-111">**Windows 2000:**  Questo parametro viene ignorato e deve essere sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="75d21-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="75d21-112">**Windows XP e versioni successive:**  Questo parametro è sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="75d21-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="75d21-113">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro potrebbe essere **null** o potrebbe contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="75d21-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="75d21-114">Se il motore funziona in modalità a istanze diverse, questo parametro deve essere un puntatore a un'istanza creata con [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="75d21-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="75d21-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75d21-115">Return Value</span></span>

<span data-ttu-id="75d21-116">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="75d21-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="75d21-117">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="75d21-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75d21-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="75d21-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="75d21-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75d21-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75d21-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="75d21-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="75d21-121">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="75d21-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d21-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="75d21-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="75d21-123">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi parametri ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="75d21-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="75d21-124">Questo errore viene restituito da <strong>JetTerm</strong> quando il motore è in modalità a istanze diverse e quando <em>pinstance</em> fa riferimento a un'istanza non valida.</span><span class="sxs-lookup"><span data-stu-id="75d21-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="75d21-125"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75d21-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d21-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="75d21-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="75d21-127">Non è possibile completare l'operazione perché l'istanza non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="75d21-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d21-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="75d21-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="75d21-129">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="75d21-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d21-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="75d21-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="75d21-131">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza.</span><span class="sxs-lookup"><span data-stu-id="75d21-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d21-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="75d21-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="75d21-133">Non è possibile completare l'operazione perché è in corso un'operazione di backup sull'istanza.</span><span class="sxs-lookup"><span data-stu-id="75d21-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d21-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="75d21-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="75d21-135">Impossibile arrestare l'istanza perché attualmente sono presenti sessioni con transazioni attive per l'istanza specificata.</span><span class="sxs-lookup"><span data-stu-id="75d21-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="75d21-136">Questo errore si verifica solo se viene utilizzata la JET_bitTermComplete.</span><span class="sxs-lookup"><span data-stu-id="75d21-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75d21-137">Se questa funzione ha esito positivo, l'istanza specificata verrà arrestata.</span><span class="sxs-lookup"><span data-stu-id="75d21-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="75d21-138">L'handle dell'istanza verrà inoltre chiuso e reso non disponibile a qualsiasi API che accetta un handle di istanza.</span><span class="sxs-lookup"><span data-stu-id="75d21-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="75d21-139">Verranno chiusi anche tutti gli altri oggetti associati all'istanza, ad esempio le sessioni.</span><span class="sxs-lookup"><span data-stu-id="75d21-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="75d21-140">Lo stato del file del checkpoint, dei file di log delle transazioni e dei file di database collegati all'istanza verrà modificato durante il processo di arresto.</span><span class="sxs-lookup"><span data-stu-id="75d21-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="75d21-141">Se questa funzione ha esito negativo a causa di un errore di utilizzo, l'istanza rimane in uno stato inizializzato e non vengono apportate modifiche.</span><span class="sxs-lookup"><span data-stu-id="75d21-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="75d21-142">In caso contrario, l'istanza viene ancora arrestata in base al caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="75d21-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="75d21-143">La differenza consiste nel fatto che l'istanza dovrà eseguire il ripristino di arresto anomalo del sistema alla successiva inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="75d21-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="75d21-144">Il motore tenterà di scaricare quanti più dati possibile per ridurre al minimo la quantità di ripristino richiesta.</span><span class="sxs-lookup"><span data-stu-id="75d21-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="75d21-145">A livello concettuale, questo errore di **JetTerm** non è diverso da un arresto anomalo del processo.</span><span class="sxs-lookup"><span data-stu-id="75d21-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="75d21-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="75d21-146">Remarks</span></span>

<span data-ttu-id="75d21-147">Se il processo host di un'istanza viene chiuso per qualsiasi motivo prima che **JetTerm** venga chiamato correttamente su tale istanza, l'istanza viene considerata in stato arrestato in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="75d21-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="75d21-148">Il ripristino dell'arresto anomalo si verificherà al successivo tentativo di inizializzare l'istanza.</span><span class="sxs-lookup"><span data-stu-id="75d21-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="75d21-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75d21-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75d21-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="75d21-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="75d21-151">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="75d21-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d21-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="75d21-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="75d21-153">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="75d21-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d21-154"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="75d21-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="75d21-155">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="75d21-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75d21-156"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="75d21-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="75d21-157">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="75d21-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75d21-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="75d21-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="75d21-159">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="75d21-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="75d21-160">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="75d21-160">See Also</span></span>

[<span data-ttu-id="75d21-161">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="75d21-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="75d21-162">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="75d21-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="75d21-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="75d21-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="75d21-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="75d21-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="75d21-165">JetInit</span><span class="sxs-lookup"><span data-stu-id="75d21-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="75d21-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="75d21-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="75d21-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="75d21-167">JetTerm2</span></span>](./jetterm2-function.md)

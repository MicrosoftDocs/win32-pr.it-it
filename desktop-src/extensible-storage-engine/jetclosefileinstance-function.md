---
description: 'Altre informazioni su: funzione JetCloseFileInstance'
title: JetCloseFileInstance (funzione)
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524967"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="b144c-103">JetCloseFileInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="b144c-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="b144c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b144c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="b144c-105">JetCloseFileInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="b144c-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="b144c-106">La funzione **JetCloseFileInstance** chiude un file aperto con [JetOpenFileInstance](./jetopenfileinstance-function.md) dopo l'estrazione dei dati da tale file con [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="b144c-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="b144c-107">**Windows XP: JetCloseFileInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b144c-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="b144c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b144c-108">Parameters</span></span>

<span data-ttu-id="b144c-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="b144c-109">*instance*</span></span>

<span data-ttu-id="b144c-110">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b144c-110">The instance to use for this call.</span></span>

<span data-ttu-id="b144c-111">Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="b144c-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="b144c-112">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="b144c-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="b144c-113">Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="b144c-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="b144c-114">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="b144c-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="b144c-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="b144c-115">*hfFile*</span></span>

<span data-ttu-id="b144c-116">Handle del file da leggere.</span><span class="sxs-lookup"><span data-stu-id="b144c-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="b144c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b144c-117">Return Value</span></span>

<span data-ttu-id="b144c-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b144c-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b144c-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b144c-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b144c-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b144c-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="b144c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b144c-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b144c-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b144c-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b144c-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b144c-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b144c-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b144c-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b144c-125">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="b144c-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b144c-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b144c-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b144c-127">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="b144c-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b144c-128">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b144c-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b144c-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b144c-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b144c-130">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b144c-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="b144c-131">Questo problema può verificarsi per <strong>JetCloseFileInstance</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="b144c-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="b144c-132">L'handle dell'istanza specificato non è valido (Windows XP e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="b144c-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="b144c-133">L'handle di file specificato non è valido</span><span class="sxs-lookup"><span data-stu-id="b144c-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b144c-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="b144c-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="b144c-135">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="b144c-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b144c-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b144c-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b144c-137">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="b144c-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b144c-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b144c-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b144c-139">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="b144c-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b144c-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="b144c-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="b144c-141">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="b144c-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b144c-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b144c-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b144c-143">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="b144c-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b144c-144">In seguito all'esito positivo, l'handle di file viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="b144c-144">On success, the file handle is closed.</span></span> <span data-ttu-id="b144c-145">Se un file di database è stato chiuso, il file di patch del database associato (se presente) viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="b144c-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="b144c-146">In caso di errore, non si verifica alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="b144c-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b144c-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="b144c-147">Remarks</span></span>

<span data-ttu-id="b144c-148">Attualmente, il motore di database supporta un solo file aperto tramite [JetOpenFileInstance](./jetopenfileinstance-function.md) alla volta.</span><span class="sxs-lookup"><span data-stu-id="b144c-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="b144c-149">Se un handle di file viene aperto utilizzando [JetOpenFileInstance](./jetopenfileinstance-function.md) , è necessario chiuderlo utilizzando **JetCloseFileInstance** prima di poter aprire un altro file.</span><span class="sxs-lookup"><span data-stu-id="b144c-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b144c-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b144c-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b144c-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b144c-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b144c-152">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b144c-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b144c-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b144c-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b144c-154">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b144c-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b144c-155"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b144c-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b144c-156">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b144c-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b144c-157"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b144c-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b144c-158">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b144c-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b144c-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b144c-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b144c-160">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b144c-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b144c-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b144c-161">See Also</span></span>

[<span data-ttu-id="b144c-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b144c-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b144c-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="b144c-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="b144c-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b144c-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b144c-165">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="b144c-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="b144c-166">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="b144c-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="b144c-167">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="b144c-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)

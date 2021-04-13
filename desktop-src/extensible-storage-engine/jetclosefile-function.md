---
description: 'Altre informazioni su: funzione JetCloseFile'
title: JetCloseFile (funzione)
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401589"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="5b8f5-103">JetCloseFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b8f5-103">JetCloseFile Function</span></span>


<span data-ttu-id="5b8f5-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5b8f5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="5b8f5-105">JetCloseFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b8f5-105">JetCloseFile Function</span></span>

<span data-ttu-id="5b8f5-106">La funzione **JetCloseFile** chiude un file aperto con [JetOpenFile](./jetopenfile-function.md) dopo l'estrazione dei dati da tale file con [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="5b8f5-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="5b8f5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b8f5-107">Parameters</span></span>

<span data-ttu-id="5b8f5-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="5b8f5-108">*hfFile*</span></span>

<span data-ttu-id="5b8f5-109">Handle del file da leggere.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="5b8f5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b8f5-110">Return Value</span></span>

<span data-ttu-id="5b8f5-111">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5b8f5-112">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5b8f5-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b8f5-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5b8f5-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="5b8f5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b8f5-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5b8f5-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-116">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b8f5-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5b8f5-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-118">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5b8f5-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-120">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5b8f5-121">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b8f5-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5b8f5-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-123">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="5b8f5-124">Questo problema può verificarsi per <strong>JetCloseFile</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="5b8f5-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="5b8f5-125">L'handle dell'istanza specificato non è valido (Windows XP e versioni successive),</span><span class="sxs-lookup"><span data-stu-id="5b8f5-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="5b8f5-126">L'handle di file specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="5b8f5-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-128">L'operazione non è riuscita perché non è in corso alcun backup esterno.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b8f5-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5b8f5-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-130">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5b8f5-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-132">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b8f5-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="5b8f5-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-134">L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5b8f5-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5b8f5-136">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5b8f5-137">In seguito all'esito positivo, l'handle di file viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-137">On success, the file handle is closed.</span></span> <span data-ttu-id="5b8f5-138">Se un file di database è stato chiuso, il file di patch del database associato (se presente) viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="5b8f5-139">In caso di errore, non si verifica alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5b8f5-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b8f5-140">Remarks</span></span>

<span data-ttu-id="5b8f5-141">Attualmente, il motore di database supporta un solo file aperto tramite [JetOpenFile](./jetopenfile-function.md) alla volta.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="5b8f5-142">Se un handle di file viene aperto utilizzando [JetOpenFile](./jetopenfile-function.md) , è necessario chiuderlo utilizzando **JetCloseFile** prima di poter aprire un altro file.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5b8f5-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b8f5-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-144"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5b8f5-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5b8f5-145">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b8f5-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5b8f5-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5b8f5-147">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-148"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5b8f5-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5b8f5-149">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b8f5-150"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5b8f5-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5b8f5-151">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b8f5-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5b8f5-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5b8f5-153">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5b8f5-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5b8f5-154">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5b8f5-154">See Also</span></span>

[<span data-ttu-id="5b8f5-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5b8f5-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5b8f5-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5b8f5-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5b8f5-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="5b8f5-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="5b8f5-158">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="5b8f5-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="5b8f5-159">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="5b8f5-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="5b8f5-160">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5b8f5-160">JetStopService</span></span>](./jetstopservice-function.md)

---
description: 'Altre informazioni su: funzione JetOSSnapshotPrepare'
title: Funzione JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315613"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="e4e1a-103">Funzione JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="e4e1a-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="e4e1a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e4e1a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="e4e1a-105">Funzione JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="e4e1a-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="e4e1a-106">La funzione **JetOSSnapshotPrepare** avvia i preparativi per una sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="e4e1a-107">Una sessione snapshot è un breve intervallo di tempo in cui il motore non rilascia alcun disco IOs su disco, in modo che il motore possa partecipare a una sessione di snapshot del volume (se basata su uno snapshot writer).</span><span class="sxs-lookup"><span data-stu-id="e4e1a-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="e4e1a-108">**Windows XP:**  **JetOSSnapshotPrepare** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e4e1a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4e1a-109">Parameters</span></span>

<span data-ttu-id="e4e1a-110">*psnapId*</span><span class="sxs-lookup"><span data-stu-id="e4e1a-110">*psnapId*</span></span>

<span data-ttu-id="e4e1a-111">Identificatore della sessione snapshot da avviare.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="e4e1a-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e4e1a-112">*grbit*</span></span>

<span data-ttu-id="e4e1a-113">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-113">The options for this call.</span></span> <span data-ttu-id="e4e1a-114">Questo parametro può avere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4e1a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e4e1a-115">Value</span></span></p></th>
<th><p><span data-ttu-id="e4e1a-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e4e1a-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-117">0</span><span class="sxs-lookup"><span data-stu-id="e4e1a-117">0</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-118">Snapshot normale.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4e1a-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="e4e1a-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-120">Verranno effettuati solo i file di log.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="e4e1a-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-122">Uno snapshot di copia (normale o incrementale) senza troncamento del log.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4e1a-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="e4e1a-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-124">La sessione snapshot si verifica dopo <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> e richiede una chiamata di funzione <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</span><span class="sxs-lookup"><span data-stu-id="e4e1a-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="e4e1a-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-126">Nessuna istanza verrà preparata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="e4e1a-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e4e1a-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4e1a-128">Return Value</span></span>

<span data-ttu-id="e4e1a-129">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e4e1a-130">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e1a-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4e1a-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e4e1a-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="e4e1a-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4e1a-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e4e1a-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-134">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4e1a-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e4e1a-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-136">Il puntatore di ID snapshot è NULL o il parametro <em>grbit</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="e4e1a-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="e4e1a-138">Una sessione snapshot è già in corso e l'operazione non può avere più di una sessione snapshot in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e4e1a-139">Se questa funzione ha esito positivo, sarà possibile avviare una sessione snapshot in qualsiasi momento con la fase di blocco IO.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="e4e1a-140">L'identificatore per la sessione verrà restituito e deve essere utilizzato nelle chiamate successive per la sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="e4e1a-141">Le istanze in esecuzione del motore verranno ora considerate parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="e4e1a-142">**Windows Vista:**  Per specificare un subset diverso di istanze, è possibile chiamare [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e1a-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="e4e1a-143">La normale chiamata di sequenza API è: **JetOSSnapshotPrepare**, seguita facoltativamente da una o più chiamate a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)e quindi da [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="e4e1a-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="e4e1a-144">Una volta avviato il blocco, è possibile terminarlo utilizzando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="e4e1a-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="e4e1a-145">In qualsiasi momento dopo la preparazione, la sessione snapshot può essere terminata improvvisamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="e4e1a-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="e4e1a-146">Se JET_bitContinueAfterThaw viene specificato dopo [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), la sessione snapshot rimarrà (anche se verrà ripresa l'i/O).</span><span class="sxs-lookup"><span data-stu-id="e4e1a-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="e4e1a-147">In questo modo verrà abilitata una verifica dello snapshot e, se necessario, verrà abilitato il troncamento del log tramite [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) e verrà richiesta una chiamata a [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span><span class="sxs-lookup"><span data-stu-id="e4e1a-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="e4e1a-148">Se questa funzione ha esito negativo, non viene apportata alcuna modifica allo stato del motore.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e4e1a-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4e1a-149">Remarks</span></span>

<span data-ttu-id="e4e1a-150">Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e4e1a-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4e1a-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e4e1a-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e4e1a-153">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4e1a-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e4e1a-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e4e1a-155">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-156"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e4e1a-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e4e1a-157">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4e1a-158"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="e4e1a-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e4e1a-159">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4e1a-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e4e1a-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e4e1a-161">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e4e1a-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e4e1a-162">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e4e1a-162">See Also</span></span>

[<span data-ttu-id="e4e1a-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e4e1a-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e4e1a-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="e4e1a-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="e4e1a-165">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="e4e1a-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="e4e1a-166">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="e4e1a-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="e4e1a-167">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="e4e1a-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="e4e1a-168">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="e4e1a-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="e4e1a-169">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="e4e1a-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="e4e1a-170">JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="e4e1a-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)

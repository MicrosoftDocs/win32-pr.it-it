---
description: 'Altre informazioni su: funzione JetOSSnapshotFreeze'
title: Funzione JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232739"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="f63c7-103">Funzione JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="f63c7-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="f63c7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f63c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="f63c7-105">Funzione JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="f63c7-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="f63c7-106">La funzione **JetOSSnapshotFreeze** avvia uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="f63c7-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="f63c7-107">Durante l'esecuzione dello snapshot, non è possibile eseguire alcuna attività Write-to-disk da parte del motore.</span><span class="sxs-lookup"><span data-stu-id="f63c7-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="f63c7-108">**Windows XP:**  **JetOSSnapshotFreeze** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f63c7-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f63c7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f63c7-109">Parameters</span></span>

<span data-ttu-id="f63c7-110">*snapId*</span><span class="sxs-lookup"><span data-stu-id="f63c7-110">*snapId*</span></span>

<span data-ttu-id="f63c7-111">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="f63c7-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="f63c7-112">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="f63c7-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="f63c7-113">Numero di istanze attualmente in esecuzione nel motore che fanno parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="f63c7-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="f63c7-114">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="f63c7-114">*paInstanceInfo*</span></span>

<span data-ttu-id="f63c7-115">Matrice di strutture, una per ogni istanza in esecuzione che fa parte della sessione snapshot, che descrive l'istanza e i database che ne fanno parte.</span><span class="sxs-lookup"><span data-stu-id="f63c7-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="f63c7-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f63c7-116">*grbit*</span></span>

<span data-ttu-id="f63c7-117">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="f63c7-117">The options for this call.</span></span> <span data-ttu-id="f63c7-118">Questo parametro è riservato per utilizzi futuri e l'unico valore valido supportato è 0.</span><span class="sxs-lookup"><span data-stu-id="f63c7-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="f63c7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f63c7-119">Return Value</span></span>

<span data-ttu-id="f63c7-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f63c7-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f63c7-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f63c7-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f63c7-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f63c7-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="f63c7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f63c7-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f63c7-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f63c7-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f63c7-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63c7-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f63c7-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f63c7-127">I puntatori forniti per i parametri di output sono NULL, la sessione snapshot non è valida o il parametro <em>grbit</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="f63c7-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="f63c7-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="f63c7-129">La sessione snapshot non è nello stato appropriato per avviare un blocco (ad esempio, un blocco precedente non è riuscito in questa sessione).</span><span class="sxs-lookup"><span data-stu-id="f63c7-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63c7-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="f63c7-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="f63c7-131">Il motore non si trova in uno stato in cui può essere eseguito uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="f63c7-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="f63c7-132">Uno o più backup di streaming sono già in corso o una o più istanze passano attraverso i passaggi di ripristino o terminano.</span><span class="sxs-lookup"><span data-stu-id="f63c7-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="f63c7-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="f63c7-134">Identificatore per la sessione snapshot non valido.</span><span class="sxs-lookup"><span data-stu-id="f63c7-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63c7-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f63c7-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f63c7-136">La funzione non è riuscita a causa di una condizione di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f63c7-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="f63c7-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="f63c7-138">La funzione non è riuscita perché non è stato possibile avviare un nuovo thread che esegue il blocco.</span><span class="sxs-lookup"><span data-stu-id="f63c7-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f63c7-139">Se questa funzione ha esito positivo, non verranno eseguiti IOs di scrittura per i file di database o per i file di log che fanno parte di istanze bloccate.</span><span class="sxs-lookup"><span data-stu-id="f63c7-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="f63c7-140">Inoltre, le informazioni sull'istanza verranno compilate correttamente e devono essere liberate in un secondo momento chiamando [JetFreeBuffer](./jetfreebuffer-function.md) con il puntatore alla matrice di informazioni sull'istanza restituita.</span><span class="sxs-lookup"><span data-stu-id="f63c7-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="f63c7-141">Se questa funzione ha esito negativo, il motore continuerà a funzionare normalmente con l'IOs che si verifica come di consueto.</span><span class="sxs-lookup"><span data-stu-id="f63c7-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="f63c7-142">Non è necessario chiamare [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) se il blocco non riesce.</span><span class="sxs-lookup"><span data-stu-id="f63c7-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="f63c7-143">Inoltre, le informazioni sull'istanza non verranno compilate, quindi non è necessario liberare questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="f63c7-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f63c7-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="f63c7-144">Remarks</span></span>

<span data-ttu-id="f63c7-145">Durante il periodo di blocco, non verranno rilasciati IOs di scrittura nei database collegati o nei log delle transazioni, anche se potrebbe essere stata eseguita la scrittura di IOs nei database temporanei o nei file di streaming.</span><span class="sxs-lookup"><span data-stu-id="f63c7-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="f63c7-146">Lo stato in cui si troveranno i database e i file di log durante il blocco, ovvero lo stato in cui si trovano i file in un'immagine di snapshot del volume, sarà tale da consentire un ripristino normale se tali file vengono ripristinati in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="f63c7-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="f63c7-147">Poiché non sono presenti operazioni di scrittura durante il periodo di blocco, le normali chiamate API nel motore potrebbero essere bloccate per tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="f63c7-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="f63c7-148">L'applicazione client deve essere in grado di gestire le chiamate API che potrebbero richiedere più tempo del normale se si verifica un blocco.</span><span class="sxs-lookup"><span data-stu-id="f63c7-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="f63c7-149">A causa dei possibili effetti descritti in precedenza, si verifica un timeout interno dopo il quale la sessione snapshot arresterà la fase di blocco anche se non sono state chiamate le API che hanno eseguito lo sblocco o l'interruzione.</span><span class="sxs-lookup"><span data-stu-id="f63c7-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="f63c7-150">Il valore del timeout può essere modificato usando il [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f63c7-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="f63c7-151">Si noti che l'intervallo di blocco tipico è compreso nell'intervallo di 10 secondi con il timeout predefinito in un punto intorno a 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="f63c7-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f63c7-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f63c7-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f63c7-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f63c7-154">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f63c7-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63c7-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f63c7-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f63c7-156">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f63c7-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-157"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f63c7-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f63c7-158">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f63c7-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63c7-159"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f63c7-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f63c7-160">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f63c7-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f63c7-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f63c7-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f63c7-162">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f63c7-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f63c7-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f63c7-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f63c7-164">Implementato come <strong>JetOSSnapshotFreezeW</strong> (Unicode) e <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f63c7-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f63c7-165">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f63c7-165">See Also</span></span>

[<span data-ttu-id="f63c7-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f63c7-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f63c7-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="f63c7-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="f63c7-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="f63c7-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="f63c7-169">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="f63c7-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="f63c7-170">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="f63c7-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="f63c7-171">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="f63c7-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="f63c7-172">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="f63c7-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

---
description: 'Altre informazioni su: funzione JetInit'
title: Funzione JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356214"
---
# <a name="jetinit-function"></a><span data-ttu-id="0ab77-103">Funzione JetInit</span><span class="sxs-lookup"><span data-stu-id="0ab77-103">JetInit Function</span></span>


<span data-ttu-id="0ab77-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0ab77-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="0ab77-105">Funzione JetInit</span><span class="sxs-lookup"><span data-stu-id="0ab77-105">JetInit Function</span></span>

<span data-ttu-id="0ab77-106">La funzione **JetInit** inserisce il motore di database in uno stato in cui può supportare l'utilizzo di file di database da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab77-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="0ab77-107">Il motore deve essere già configurato correttamente per l'inizializzazione tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0ab77-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="0ab77-108">Il ripristino dell'arresto anomalo del database viene eseguito automaticamente nell'ambito del processo di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="0ab77-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="0ab77-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ab77-109">Parameters</span></span>

<span data-ttu-id="0ab77-110">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="0ab77-110">*pinstance*</span></span>

<span data-ttu-id="0ab77-111">Istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="0ab77-111">The instance to use for this call.</span></span>

<span data-ttu-id="0ab77-112">Per Windows 2000, questo parametro viene ignorato e deve essere sempre NULL.</span><span class="sxs-lookup"><span data-stu-id="0ab77-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="0ab77-113">Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore.</span><span class="sxs-lookup"><span data-stu-id="0ab77-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="0ab77-114">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL o può essere impostato su un buffer di output valido che restituirà l'handle dell'istanza globale creato come effetto collaterale dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="0ab77-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="0ab77-115">Questo buffer di output deve essere impostato su NULL o JET_instanceNil.</span><span class="sxs-lookup"><span data-stu-id="0ab77-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="0ab77-116">Questo handle di istanza può quindi essere passato a qualsiasi altra funzione che usa un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="0ab77-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="0ab77-117">Se il motore funziona in modalità a istanze diverse, questo parametro deve essere impostato su un buffer di input valido che contiene l'handle dell'istanza restituito dall'istanza della funzione [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzata.</span><span class="sxs-lookup"><span data-stu-id="0ab77-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="0ab77-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ab77-118">Remarks</span></span>

<span data-ttu-id="0ab77-119">Un'istanza deve essere inizializzata con una chiamata a **JetInit** prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0ab77-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="0ab77-120">Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="0ab77-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="0ab77-121">Un'istanza è l'unità di recupero per il motore di database.</span><span class="sxs-lookup"><span data-stu-id="0ab77-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="0ab77-122">Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database.</span><span class="sxs-lookup"><span data-stu-id="0ab77-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="0ab77-123">Questi file includono il file del checkpoint e i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="0ab77-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="0ab77-124">Il numero massimo di istanze che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxInstances](./resource-parameters.md), che può essere configurato tramite una chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0ab77-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="0ab77-125">Quando il motore di database viene inizializzato per la prima volta, **JetInit** creerà un set iniziale di file per supportare tale istanza.</span><span class="sxs-lookup"><span data-stu-id="0ab77-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="0ab77-126">Questi file includono un file del checkpoint (denominato \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un set di file di log delle transazioni riservati, denominato RES1. LOG e RES2. LOG), un file di log delle transazioni iniziale, denominato \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) e un file di database temporaneo (denominato in base a [JET_paramTempPath](./temporary-database-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="0ab77-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="0ab77-127">Se [JET_paramRecovery](./transaction-log-parameters.md) è impostato su "off", il file del checkpoint e i file di log non verranno creati.</span><span class="sxs-lookup"><span data-stu-id="0ab77-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="0ab77-128">Se [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) è impostato su zero, il file di database temporaneo non verrà creato.</span><span class="sxs-lookup"><span data-stu-id="0ab77-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="0ab77-129">Questi file rappresentano l'impronta sul disco di un'istanza e devono essere gestiti con cautela.</span><span class="sxs-lookup"><span data-stu-id="0ab77-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="0ab77-130">Se questi file sono danneggiati singolarmente o rispetto a un altro, i dati archiviati nei database associati all'istanza potrebbero andare persi.</span><span class="sxs-lookup"><span data-stu-id="0ab77-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="0ab77-131">Quando il motore di database viene inizializzato con un set di file di log delle transazioni esistente, questi file vengono controllati per verificare se l'incarnazione precedente dell'istanza è stata danneggiata.</span><span class="sxs-lookup"><span data-stu-id="0ab77-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="0ab77-132">Se viene rilevato un arresto anomalo, il ripristino dell'arresto anomalo verrà eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0ab77-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="0ab77-133">Questo processo ricostruirà i database collegati all'istanza durante la precedente incarnazione del motore e salverà le modifiche nei file di database.</span><span class="sxs-lookup"><span data-stu-id="0ab77-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="0ab77-134">Il risultato sarà costituito da database coerenti con le transazioni.</span><span class="sxs-lookup"><span data-stu-id="0ab77-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="0ab77-135">Questo processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre sui database è elevato.</span><span class="sxs-lookup"><span data-stu-id="0ab77-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="0ab77-136">A causa del fatto che **JetInit** esegue il ripristino dell'arresto anomalo del sistema, è possibile che venga restituito quasi qualsiasi errore del motore di database in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="0ab77-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="0ab77-137">In pratica, la maggior parte degli errori riscontrati nella distribuzione rientrano in due categorie: il danneggiamento dei dati e la gestione degli errori del file.</span><span class="sxs-lookup"><span data-stu-id="0ab77-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="0ab77-138">Il danneggiamento dei dati si manifesterà più spesso negli errori seguenti o simili:</span><span class="sxs-lookup"><span data-stu-id="0ab77-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="0ab77-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="0ab77-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="0ab77-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="0ab77-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="0ab77-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="0ab77-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="0ab77-142">Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati.</span><span class="sxs-lookup"><span data-stu-id="0ab77-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="0ab77-143">La gestione non automatica dei file si manifesterà più spesso negli errori seguenti o simili:</span><span class="sxs-lookup"><span data-stu-id="0ab77-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="0ab77-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="0ab77-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="0ab77-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="0ab77-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="0ab77-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0ab77-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="0ab77-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="0ab77-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="0ab77-148">Se il ripristino viene eseguito in un set di log, per cui non sono presenti tutti i database (che restituiscono l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, è possibile utilizzare il JET_ bitReplayIgnoreMissingDB per continuare il ripristino dei database disponibili.</span><span class="sxs-lookup"><span data-stu-id="0ab77-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="0ab77-149">Questi errori possono essere evitati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab77-149">These errors are preventable by the application.</span></span> <span data-ttu-id="0ab77-150">L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0ab77-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="0ab77-151">Se l'applicazione desidera eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="0ab77-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="0ab77-152">Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.</span><span class="sxs-lookup"><span data-stu-id="0ab77-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="0ab77-153">La funzione **JetInit** si comporta in modo diverso rispetto ai file di database collegati all'istanza tra Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0ab77-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="0ab77-154">**Windows 2000:**  In Windows 2000, qualsiasi database collegato all'istanza durante un'incarnazione precedente di tale istanza rimane collegato all'istanza dopo che **JetInit** è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0ab77-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="0ab77-155">Non è necessario chiamare [JetAttachDatabase](./jetattachdatabase-function.md) dopo **JetInit** per garantire l'accesso al database in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0ab77-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="0ab77-156">Se la funzione [JetAttachDatabase](./jetattachdatabase-function.md) viene chiamata dopo la funzione **JetInit** , verrà restituito il JET_wrnDatabaseAttached avviso.</span><span class="sxs-lookup"><span data-stu-id="0ab77-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="0ab77-157">Questo avviso indica che l'allegato del database è stato mantenuto e può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="0ab77-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="0ab77-158">**Windows XP:**  In Windows XP e versioni successive, tutti i database vengono scollegati automaticamente dall'istanza di da **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="0ab77-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="0ab77-159">Ciò significa che [JetAttachDatabase](./jetattachdatabase-function.md) deve sempre essere chiamato dopo **JetInit** in questo caso.</span><span class="sxs-lookup"><span data-stu-id="0ab77-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="0ab77-160">Qualsiasi applicazione scritta per l'esecuzione in Windows 2000 e nelle versioni successive deve sempre chiamare [JetAttachDatabase](./jetattachdatabase-function.md) dopo **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="0ab77-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="0ab77-161">Se l'applicazione viene eseguita in Windows 2000, è necessario che venga visualizzata JET_wrnDatabaseAttached in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="0ab77-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="0ab77-162">Per ulteriori informazioni, vedere [JetAttachDatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0ab77-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0ab77-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ab77-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ab77-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0ab77-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0ab77-165">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0ab77-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ab77-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0ab77-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0ab77-167">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0ab77-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ab77-168"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="0ab77-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0ab77-169">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="0ab77-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ab77-170"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="0ab77-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0ab77-171">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0ab77-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ab77-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0ab77-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0ab77-173">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0ab77-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0ab77-174">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0ab77-174">See Also</span></span>

[<span data-ttu-id="0ab77-175">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="0ab77-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0ab77-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0ab77-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0ab77-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0ab77-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0ab77-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0ab77-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0ab77-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="0ab77-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="0ab77-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="0ab77-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="0ab77-181">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="0ab77-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="0ab77-182">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0ab77-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0ab77-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="0ab77-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="0ab77-184">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0ab77-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)

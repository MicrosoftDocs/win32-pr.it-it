---
description: 'Altre informazioni su: funzione JetCreateInstance'
title: Funzione JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319186"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="6af99-103">Funzione JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="6af99-103">JetCreateInstance Function</span></span>


<span data-ttu-id="6af99-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6af99-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="6af99-105">Funzione JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="6af99-105">JetCreateInstance Function</span></span>

<span data-ttu-id="6af99-106">La funzione **JetCreateInstance** alloca una nuova istanza del motore di database per l'utilizzo in un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="6af99-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="6af99-107">**Windows XP: JetCreateInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6af99-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="6af99-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6af99-108">Parameters</span></span>

<span data-ttu-id="6af99-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="6af99-109">*pinstance*</span></span>

<span data-ttu-id="6af99-110">Buffer di output che riceve l'istanza appena creata.</span><span class="sxs-lookup"><span data-stu-id="6af99-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="6af99-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="6af99-111">*szInstanceName*</span></span>

<span data-ttu-id="6af99-112">Identificatore di stringa univoco per l'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="6af99-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="6af99-113">Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.</span><span class="sxs-lookup"><span data-stu-id="6af99-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="6af99-114">**Nota** Un valore NULL viene considerato come un identificatore di stringa valido per un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="6af99-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="6af99-115">Solo un'istanza può avere un identificatore di stringa NULL.</span><span class="sxs-lookup"><span data-stu-id="6af99-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="6af99-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6af99-116">Return Value</span></span>

<span data-ttu-id="6af99-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="6af99-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6af99-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="6af99-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6af99-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6af99-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="6af99-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6af99-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6af99-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6af99-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6af99-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="6af99-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af99-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="6af99-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="6af99-124">Il nome dell'istanza specificato è già in uso per questo processo.</span><span class="sxs-lookup"><span data-stu-id="6af99-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6af99-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6af99-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6af99-126">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="6af99-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="6af99-127">Questo problema può verificarsi per <strong>JetCreateInstance</strong> quando <em>pinstance</em> è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="6af99-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af99-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6af99-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="6af99-129">L'operazione non è riuscita perché non può essere usata quando il motore di database funziona in modalità a istanza singola (modalità di compatibilità di Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="6af99-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6af99-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="6af99-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="6af99-131">Impossibile creare una nuova istanza. è stato raggiunto il numero massimo di istanze.</span><span class="sxs-lookup"><span data-stu-id="6af99-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="6af99-132">Il numero massimo di istanze supportate viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="6af99-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6af99-133">In caso di esito positivo, verrà allocata una nuova istanza e verrà restituito l'identificatore per esso.</span><span class="sxs-lookup"><span data-stu-id="6af99-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="6af99-134">A questo punto, tutti i parametri di sistema per l'istanza avranno i valori dei parametri di sistema predefiniti globali.</span><span class="sxs-lookup"><span data-stu-id="6af99-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="6af99-135">Una volta allocata, un'istanza deve essere terminata e/o liberata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="6af99-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="6af99-136">In caso di errore, verrà restituito un errore che rappresenta la fonte di errore e non verrà allocata alcuna istanza.</span><span class="sxs-lookup"><span data-stu-id="6af99-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6af99-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="6af99-137">Remarks</span></span>

<span data-ttu-id="6af99-138">Un'istanza deve essere inizializzata con una chiamata a [JetInit](./jetinit-function.md) prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="6af99-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="6af99-139">Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="6af99-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="6af99-140">Il numero massimo di istanze che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxInstances](./resource-parameters.md), che può essere configurato tramite una chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="6af99-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="6af99-141">Un'istanza è l'unità di recupero per il motore di database.</span><span class="sxs-lookup"><span data-stu-id="6af99-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="6af99-142">Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database.</span><span class="sxs-lookup"><span data-stu-id="6af99-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="6af99-143">Questi file includono il file del checkpoint e i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="6af99-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="6af99-144">Se la funzione ha esito positivo, il motore di database verrà automaticamente modificato in modalità a istanze diverse come effetto collaterale di questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="6af99-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="6af99-145">Se l'applicazione desidera consentire una sola istanza del processo, [JetInit](./jetinit-function.md) deve essere usato per avviare il motore di database in modalità di compatibilità con Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6af99-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="6af99-146">Se presente, il *szDisplayName* verrà usato per identificare l'istanza in posizioni come il registro eventi o verso altri chiamanti come le applicazioni di backup (tramite funzioni come [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="6af99-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="6af99-147">Se il nome visualizzato non viene specificato, verrà usato il *szInstanceName* univoco, se presente, in caso contrario verrà restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="6af99-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="6af99-148">Se per il motore non è stata impostata la modalità in esecuzione, dopo questa chiamata verrà impostata la modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="6af99-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="6af99-149">La sequenza di avvio tipica per un processo che potenzialmente esegue più istanze Jet è la seguente:</span><span class="sxs-lookup"><span data-stu-id="6af99-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="6af99-150">Una chiamata a [JetCreateInstance2](./jetcreateinstance2-function.md) che consente di allocare e assegnare un nome all'istanza.</span><span class="sxs-lookup"><span data-stu-id="6af99-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="6af99-151">Più chiamate a [JetSetSystemParameter](./jetsetsystemparameter-function.md) per tale istanza per impostare parametri di sistema diversi.</span><span class="sxs-lookup"><span data-stu-id="6af99-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="6af99-152">Si noti che alcuni parametri di sistema devono essere univoci per ogni istanza, ad esempio [JET_paramSystemPath](./transaction-log-parameters.md) o [JET_paramLogFilePath](./transaction-log-parameters.md), quindi è molto probabile che sia necessario impostare ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="6af99-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="6af99-153">Avviare l'istanza utilizzando [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="6af99-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="6af99-154">Per terminare e/o liberare un'istanza, è necessario usare [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6af99-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="6af99-155">Se questa è la prima istanza da avviare, verranno eseguiti alcuni passaggi aggiuntivi durante la chiamata per eseguire l'inizializzazione e la configurazione di base del sistema.</span><span class="sxs-lookup"><span data-stu-id="6af99-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="6af99-156">Alcuni di questi passaggi potrebbero causare errori specifici che iniziano con JET_errOutOfMemory, ma anche altri. vedere gli errori precedenti.</span><span class="sxs-lookup"><span data-stu-id="6af99-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="6af99-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6af99-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6af99-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6af99-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6af99-159">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6af99-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af99-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6af99-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6af99-161">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6af99-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6af99-162"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="6af99-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6af99-163">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="6af99-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af99-164"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="6af99-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6af99-165">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6af99-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6af99-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6af99-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6af99-167">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6af99-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6af99-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6af99-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6af99-169">Implementato come <strong>JetCreateInstanceW</strong> (Unicode) e <strong>JetCreateInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6af99-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6af99-170">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6af99-170">See Also</span></span>

[<span data-ttu-id="6af99-171">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="6af99-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="6af99-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6af99-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6af99-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6af99-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6af99-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="6af99-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="6af99-175">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="6af99-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="6af99-176">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="6af99-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="6af99-177">JetInit</span><span class="sxs-lookup"><span data-stu-id="6af99-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="6af99-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="6af99-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="6af99-179">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="6af99-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="6af99-180">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6af99-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6af99-181">JetTerm</span><span class="sxs-lookup"><span data-stu-id="6af99-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="6af99-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="6af99-182">JetTerm2</span></span>](./jetterm2-function.md)

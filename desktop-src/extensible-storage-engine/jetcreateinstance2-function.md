---
description: 'Altre informazioni su: funzione JetCreateInstance2'
title: Funzione JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af31e7e66d92cf7ebbc238ac54a9b331e6dc5362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315624"
---
# <a name="jetcreateinstance2-function"></a><span data-ttu-id="0b2e7-103">Funzione JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="0b2e7-103">JetCreateInstance2 Function</span></span>


<span data-ttu-id="0b2e7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0b2e7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance2-function"></a><span data-ttu-id="0b2e7-105">Funzione JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="0b2e7-105">JetCreateInstance2 Function</span></span>

<span data-ttu-id="0b2e7-106">La funzione **JetCreateInstance2** viene utilizzata per allocare una nuova istanza del motore di database per l'utilizzo in un unico processo, con un nome visualizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-106">The **JetCreateInstance2** function is used to allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="0b2e7-107">**Windows XP:**  **JetCreateInstance2** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-107">**Windows XP:**  **JetCreateInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="0b2e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b2e7-108">Parameters</span></span>

<span data-ttu-id="0b2e7-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="0b2e7-109">*pinstance*</span></span>

<span data-ttu-id="0b2e7-110">Buffer di output che riceverà l'istanza appena creata.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-110">The output buffer that will receive the newly created instance.</span></span>

<span data-ttu-id="0b2e7-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="0b2e7-111">*szInstanceName*</span></span>

<span data-ttu-id="0b2e7-112">Specifica un identificatore di stringa univoco per l'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-112">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="0b2e7-113">Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="0b2e7-114">**Nota** Un valore NULL viene considerato come un identificatore di stringa valido per un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="0b2e7-115">Solo un'istanza può avere un identificatore di stringa NULL.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-115">Only one instance may have a NULL string identifier.</span></span>

<span data-ttu-id="0b2e7-116">*szDisplayName*</span><span class="sxs-lookup"><span data-stu-id="0b2e7-116">*szDisplayName*</span></span>

<span data-ttu-id="0b2e7-117">Nome visualizzato per l'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-117">A display name for the instance to be created.</span></span> <span data-ttu-id="0b2e7-118">Se questo parametro non è presente, il relativo valore viene considerato NULL.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-118">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="0b2e7-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0b2e7-119">*grbit*</span></span>

<span data-ttu-id="0b2e7-120">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-120">Reserved for future use.</span></span> <span data-ttu-id="0b2e7-121">Se questo parametro non è presente, il relativo valore si presume che sia zero.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-121">When this parameter is not present, its value is presumed to be zero.</span></span>

### <a name="return-value"></a><span data-ttu-id="0b2e7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b2e7-122">Return Value</span></span>

<span data-ttu-id="0b2e7-123">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0b2e7-124">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2e7-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b2e7-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0b2e7-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="0b2e7-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b2e7-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b2e7-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0b2e7-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0b2e7-128">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b2e7-129">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="0b2e7-129">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="0b2e7-130">Il nome dell'istanza specificato è già in uso per questo processo.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-130">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b2e7-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0b2e7-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0b2e7-132">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="0b2e7-133">Questo problema può verificarsi per <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> quando <em>pinstance</em> è null.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-133">This can happen for <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> when <em>pinstance</em> is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b2e7-134">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="0b2e7-134">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="0b2e7-135">L'operazione non è riuscita perché non può essere usata quando il motore di database funziona in modalità a istanza singola (modalità di compatibilità di Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-135">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b2e7-136">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="0b2e7-136">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="0b2e7-137">Impossibile creare una nuova istanza. è stato raggiunto il numero massimo di istanze.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-137">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="0b2e7-138">Il numero massimo di istanze supportate viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-138">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b2e7-139">In caso di esito positivo, verrà allocata una nuova istanza e verrà restituito l'identificatore per esso.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-139">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="0b2e7-140">A questo punto, tutti i parametri di sistema per l'istanza avranno i valori dei parametri di sistema predefiniti globali.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-140">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="0b2e7-141">Una volta allocata, un'istanza deve essere terminata e/o liberata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-141">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="0b2e7-142">In caso di errore, verrà restituito un errore che rappresenta la fonte di errore e non verrà allocata alcuna istanza.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-142">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0b2e7-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b2e7-143">Remarks</span></span>

<span data-ttu-id="0b2e7-144">Un'istanza deve essere inizializzata con una chiamata a [JetInit](./jetinit-function.md) prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-144">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="0b2e7-145">Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="0b2e7-146">Il numero massimo di istanze che è possibile creare in qualsiasi momento è controllato da *JET_paramMaxInstances*, che può essere configurato tramite una chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-146">The maximum number of instances that may be created at any one time is controlled by *JET_paramMaxInstances*, which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="0b2e7-147">Un'istanza è l'unità di recupero per il motore di database.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-147">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="0b2e7-148">Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-148">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="0b2e7-149">Questi file includono il file del checkpoint e i file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-149">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="0b2e7-150">Se la funzione ha esito positivo, il motore di database verrà automaticamente modificato in modalità a istanze diverse come effetto collaterale di questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-150">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="0b2e7-151">Se l'applicazione desidera consentire una sola istanza del processo, [JetInit](./jetinit-function.md) deve essere usato per avviare il motore di database in modalità di compatibilità con Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-151">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="0b2e7-152">Se presente, il parametro *szDisplayName* verrà usato per identificare l'istanza in posizioni come il registro eventi o verso altri chiamanti come le applicazioni di backup (tramite funzioni come [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-152">If present, the *szDisplayName* parameter will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="0b2e7-153">Se il nome visualizzato non viene specificato, verrà usato il parametro *szInstanceName* univoco, se presente. in caso contrario, verrà restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-153">If the display name is not provided, the unique *szInstanceName* parameter will be used instead, if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="0b2e7-154">Se per il motore non è stata impostata la modalità in esecuzione, dopo questa chiamata verrà impostata la modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-154">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="0b2e7-155">La sequenza di avvio tipica per un processo che potenzialmente esegue più istanze Jet è la seguente:</span><span class="sxs-lookup"><span data-stu-id="0b2e7-155">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="0b2e7-156">Una chiamata a **JetCreateInstance2** che consente di allocare e assegnare un nome all'istanza.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-156">A call to **JetCreateInstance2** which will allocate and name the instance.</span></span>

  - <span data-ttu-id="0b2e7-157">Più chiamate a [JetSetSystemParameter](./jetsetsystemparameter-function.md) per tale istanza per impostare parametri di sistema diversi.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-157">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="0b2e7-158">Si noti che alcuni parametri di sistema devono essere univoci per ogni istanza, ad esempio *JET_paramSystemPath* o *JET_paramLogFilePath*, in modo molto probabile, ognuno di questi deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-158">Note that some system parameters need to be unique for each instance (like *JET_paramSystemPath* or *JET_paramLogFilePath*) so most likely, each of these will need to be set.</span></span>

  - <span data-ttu-id="0b2e7-159">Avviare l'istanza utilizzando [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-159">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="0b2e7-160">Per terminare e/o liberare un'istanza, utilizzare [JetTerm](./jetterm-function.md) o [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-160">In order to terminate and/or free an instance, use [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="0b2e7-161">Se questa è la prima istanza da avviare, verranno eseguiti alcuni passaggi aggiuntivi durante la chiamata per eseguire l'inizializzazione e la configurazione di base del sistema.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-161">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="0b2e7-162">Alcuni di questi passaggi potrebbero causare errori specifici che iniziano con JET_errOutOfMemory ma anche altri. per ulteriori informazioni, vedere valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-162">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see Return Values for more information).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0b2e7-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b2e7-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b2e7-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0b2e7-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0b2e7-165">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b2e7-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0b2e7-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0b2e7-167">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b2e7-168"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="0b2e7-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0b2e7-169">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b2e7-170"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="0b2e7-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0b2e7-171">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b2e7-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0b2e7-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0b2e7-173">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0b2e7-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b2e7-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0b2e7-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0b2e7-175">Implementato come <strong>JetCreateInstance2W</strong> (Unicode) e <strong>JetCreateInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0b2e7-175">Implemented as <strong>JetCreateInstance2W</strong> (Unicode) and <strong>JetCreateInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0b2e7-176">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0b2e7-176">See Also</span></span>

[<span data-ttu-id="0b2e7-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0b2e7-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0b2e7-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0b2e7-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0b2e7-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0b2e7-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0b2e7-180">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="0b2e7-180">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="0b2e7-181">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="0b2e7-181">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="0b2e7-182">JetInit</span><span class="sxs-lookup"><span data-stu-id="0b2e7-182">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="0b2e7-183">JetInit2</span><span class="sxs-lookup"><span data-stu-id="0b2e7-183">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="0b2e7-184">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="0b2e7-184">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="0b2e7-185">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0b2e7-185">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="0b2e7-186">JetTerm</span><span class="sxs-lookup"><span data-stu-id="0b2e7-186">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="0b2e7-187">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="0b2e7-187">JetTerm2</span></span>](./jetterm2-function.md)

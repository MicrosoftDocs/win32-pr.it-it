---
description: 'Altre informazioni su: funzione JetStopServiceInstance2'
title: JetStopServiceInstance2 (funzione)
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752279"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="e1374-103">JetStopServiceInstance2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="e1374-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="e1374-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e1374-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="e1374-105">La funzione **JetStopServiceInstance2** prepara un'istanza prima della sospensione e prepara un'istanza dopo Resume.</span><span class="sxs-lookup"><span data-stu-id="e1374-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="e1374-106">Suspend e Resume sono stati di esecuzione del modello di ciclo di vita delle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e1374-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="e1374-107">La funzione **JetStopServiceInstance2** è stata introdotta in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e1374-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="e1374-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1374-108">Parameters</span></span>

<span data-ttu-id="e1374-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="e1374-109">*instance*</span></span>

<span data-ttu-id="e1374-110">Istanza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1374-110">The target instance.</span></span> <span data-ttu-id="e1374-111">Il tipo di dati **JET_INSTANCE** è un handle per l'istanza del database da usare per una chiamata all'API Jet.</span><span class="sxs-lookup"><span data-stu-id="e1374-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="e1374-112">Questo handle viene ottenuto quando si crea un'istanza del database chiamando le funzioni [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e1374-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="e1374-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e1374-113">*grbit*</span></span>

<span data-ttu-id="e1374-114">Gruppo di bit che specifica uno o più valori elencati e definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e1374-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1374-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e1374-115">Value</span></span></p></th>
<th><p><span data-ttu-id="e1374-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1374-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1374-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="e1374-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="e1374-118">Arresta tutti i servizi Extensible Storage Engine (ESE) per l'istanza di specificata.</span><span class="sxs-lookup"><span data-stu-id="e1374-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1374-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="e1374-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="e1374-120">Arresta le attività di manutenzione in background specificate dal client riavviabili (ad esempio, B + deframmentazione albero).</span><span class="sxs-lookup"><span data-stu-id="e1374-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1374-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="e1374-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="e1374-122">Quiesces tutte le cache Dirty sul disco.</span><span class="sxs-lookup"><span data-stu-id="e1374-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="e1374-123">Questo valore è asincrono e può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="e1374-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1374-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="e1374-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="e1374-125">Riprende le operazioni StopService rilasciate in precedenza; ovvero riavvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="e1374-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="e1374-126">Questo valore può essere combinato con il parametro <em>grbits</em> per riprendere servizi specifici o con JET_bitStopServiceAll per riprendere tutti i servizi precedentemente arrestati.</span><span class="sxs-lookup"><span data-stu-id="e1374-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="e1374-127">Questo bit può essere utilizzato solo per riprendere StopServiceBackgroundUserTasks e JET_bitStopServiceQuiesceCaches.</span><span class="sxs-lookup"><span data-stu-id="e1374-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="e1374-128">Se in precedenza è stato chiamato con JET_bitStopServiceAll, un tentativo di usare JET_bitStopServiceResume avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e1374-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="e1374-129">Se il secondo passaggio di ripresa non viene chiamato, le prestazioni dell'applicazione risulteranno ridotte.</span><span class="sxs-lookup"><span data-stu-id="e1374-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="e1374-130">In questa situazione il checkpoint viene mantenuto a zero.</span><span class="sxs-lookup"><span data-stu-id="e1374-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e1374-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1374-131">Return value</span></span>

<span data-ttu-id="e1374-132">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="e1374-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="e1374-133">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="e1374-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1374-134">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e1374-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="e1374-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1374-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1374-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e1374-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e1374-137">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e1374-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e1374-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1374-138">Remarks</span></span>

<span data-ttu-id="e1374-139">Questa funzione consente a un'applicazione JET di spostare la cache del database in uno stato pulito o quasi pulito (con l'I/O del sistema operativo), in modo che se l'applicazione venisse terminata, il ripristino sarebbe stato rapido.</span><span class="sxs-lookup"><span data-stu-id="e1374-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="e1374-140">Questo approccio è preferibile rispetto alla chiusura di JET chiamando le funzioni [JetTerm](./jetterm-function.md) o [JetDetachDatabase](./jetdetachdatabase-function.md) , in modo che, in uno scenario più comune, l'applicazione sia semplicemente sospesa e in seguito l'applicazione disponga dell'intera cache ed è pronta per iniziare il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="e1374-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="e1374-141">Se questa funzione ha esito positivo, prepara la cache del database per una sospensione imminente.</span><span class="sxs-lookup"><span data-stu-id="e1374-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="e1374-142">Questa funzione Accoda il lavoro a un thread di lavoro in background e ritorna immediatamente al chiamante.</span><span class="sxs-lookup"><span data-stu-id="e1374-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="e1374-143">La funzione deve essere chiamata in base al VisibilityNotice PLM anziché chiamare dal gestore dell'evento di sospensione dell'applicazione per assicurarsi che JET abbia il tempo di scaricamento dei buffer dirty prima che PLM sospenda/termina il processo.</span><span class="sxs-lookup"><span data-stu-id="e1374-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="e1374-144">Internamente, JET attiva una distribuzione immediata della manutenzione del checkpoint dopo la modifica della configurazione (aggiornamento del checkpoint o questo nuovo bit di cache mettere in stato).</span><span class="sxs-lookup"><span data-stu-id="e1374-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="e1374-145">Per ulteriori informazioni sugli eventi VisibilityNotice, vedere [classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span><span class="sxs-lookup"><span data-stu-id="e1374-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="e1374-146">Questa funzione deve essere chiamata due volte.</span><span class="sxs-lookup"><span data-stu-id="e1374-146">This function must be called twice.</span></span> <span data-ttu-id="e1374-147">Viene chiamato dopo che l'applicazione riceve l'avviso di sospensione dal sistema operativo, ma prima che l'applicazione sia stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="e1374-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="e1374-148">Viene quindi chiamato nuovamente dopo che il sistema operativo riprende l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e1374-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="e1374-149">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e1374-149">For example:</span></span>

<span data-ttu-id="e1374-150">Quando viene chiamato per sospendere: JET_ERR JET_API JetStopServiceInstance2 (istanza, JET_bitStopServiceQuiesceCaches);</span><span class="sxs-lookup"><span data-stu-id="e1374-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="e1374-151">Quando viene ripreso: JET_ERR JET_API JetStopServiceInstance2 (istanza, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);</span><span class="sxs-lookup"><span data-stu-id="e1374-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="e1374-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1374-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1374-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e1374-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e1374-154">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e1374-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1374-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e1374-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e1374-156">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e1374-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1374-157"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e1374-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e1374-158">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e1374-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1374-159"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="e1374-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e1374-160">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e1374-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1374-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e1374-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e1374-162">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e1374-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e1374-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1374-163">See also</span></span>

[<span data-ttu-id="e1374-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e1374-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e1374-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e1374-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e1374-166">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="e1374-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="e1374-167">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="e1374-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="e1374-168">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="e1374-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="e1374-169">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="e1374-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="e1374-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="e1374-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="e1374-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e1374-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e1374-172">JetTerm</span><span class="sxs-lookup"><span data-stu-id="e1374-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="e1374-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="e1374-173">JetTerm2</span></span>](./jetterm2-function.md)

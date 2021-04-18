---
description: 'Altre informazioni su: funzione JetGetThreadStats'
title: JetGetThreadStats (funzione)
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305737"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="c5eac-103">JetGetThreadStats (funzione)</span><span class="sxs-lookup"><span data-stu-id="c5eac-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="c5eac-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c5eac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="c5eac-105">JetGetThreadStats (funzione)</span><span class="sxs-lookup"><span data-stu-id="c5eac-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="c5eac-106">La funzione **JetGetThreadStats** recupera le informazioni sulle prestazioni dal motore di database per il thread corrente.</span><span class="sxs-lookup"><span data-stu-id="c5eac-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="c5eac-107">È possibile utilizzare più chiamate per raccogliere statistiche che riflettono l'attività del motore di database in questo thread tra le chiamate.</span><span class="sxs-lookup"><span data-stu-id="c5eac-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="c5eac-108">**Windows Vista:**  **JetGetThreadStats** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5eac-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="c5eac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5eac-109">Parameters</span></span>

<span data-ttu-id="c5eac-110">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="c5eac-110">*pvResult*</span></span>

<span data-ttu-id="c5eac-111">Buffer di output che riceve i dati delle statistiche del thread.</span><span class="sxs-lookup"><span data-stu-id="c5eac-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="c5eac-112">Il buffer contiene una struttura di [JET_THREADSTATS](./jet-threadstats-structure.md) dopo una chiamata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="c5eac-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="c5eac-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="c5eac-113">*cbMax*</span></span>

<span data-ttu-id="c5eac-114">Dimensione massima in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="c5eac-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="c5eac-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5eac-115">Return Value</span></span>

<span data-ttu-id="c5eac-116">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c5eac-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c5eac-117">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c5eac-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5eac-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c5eac-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c5eac-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5eac-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5eac-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c5eac-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c5eac-121">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c5eac-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5eac-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c5eac-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="c5eac-123">L'operazione non è riuscita perché il buffer di output specificato è troppo piccolo per contenere i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="c5eac-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="c5eac-124">La funzione <strong>JetGetThreadStats</strong> restituirà questo errore quando il buffer di output è troppo piccolo per contenere la versione più piccola della struttura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> supportata dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="c5eac-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5eac-125">In seguito all'esito positivo, il buffer di output conterrà una struttura [JET_THREADSTATS](./jet-threadstats-structure.md) contenente le statistiche del motore di database per il thread corrente.</span><span class="sxs-lookup"><span data-stu-id="c5eac-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="c5eac-126">In caso di errore, lo stato del buffer di output non è definito.</span><span class="sxs-lookup"><span data-stu-id="c5eac-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c5eac-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5eac-127">Remarks</span></span>

<span data-ttu-id="c5eac-128">Le informazioni fornite da due chiamate consecutive di questa API sono destinate a essere usate per calcolare i costi di qualsiasi altra operazione del motore di database nel thread corrente.</span><span class="sxs-lookup"><span data-stu-id="c5eac-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="c5eac-129">In genere, questa operazione viene eseguita eseguendo prima e dopo la lettura delle statistiche e sottraendo il conteggio after dal conteggio before per ottenere il conteggio netto delle operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="c5eac-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="c5eac-130">Ad esempio, un'applicazione può chiamare **JetGetThreadStats** una volta per ottenere una lettura iniziale delle statistiche per il thread corrente.</span><span class="sxs-lookup"><span data-stu-id="c5eac-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="c5eac-131">Potrebbe quindi chiamare la funzione [JetMove](./jetmove-function.md) con il parametro *cRow* impostato su JET_MoveNext per passare alla voce di indice successiva in un indice.</span><span class="sxs-lookup"><span data-stu-id="c5eac-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="c5eac-132">Potrebbe quindi chiamare di nuovo **JetGetThreadStats** per ottenere un'altra lettura delle statistiche del thread.</span><span class="sxs-lookup"><span data-stu-id="c5eac-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="c5eac-133">Potrebbe quindi sottrarre il contatore cPageReferenced dalla seconda lettura dalla prima.</span><span class="sxs-lookup"><span data-stu-id="c5eac-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="c5eac-134">Il risultato è il numero di pagine di database a cui il motore di database fa riferimento per eseguire l'operazione [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c5eac-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="c5eac-135">Le statistiche per ogni thread vengono accumulate per la durata di tale thread.</span><span class="sxs-lookup"><span data-stu-id="c5eac-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="c5eac-136">Le statistiche vengono reimpostate se la DLL del motore di database viene scaricata dal processo host.</span><span class="sxs-lookup"><span data-stu-id="c5eac-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="c5eac-137">La struttura di [JET_THREADSTATS](./jet-threadstats-structure.md) verrà probabilmente espansa in futuro per contenere più statistiche.</span><span class="sxs-lookup"><span data-stu-id="c5eac-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="c5eac-138">Le nuove statistiche verranno aggiunte alla fine della struttura e potranno essere recuperate con una dimensione del buffer di output maggiore.</span><span class="sxs-lookup"><span data-stu-id="c5eac-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="c5eac-139">La presenza di statistiche aggiuntive può essere dedotta da un valore cbStruct più grande.</span><span class="sxs-lookup"><span data-stu-id="c5eac-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c5eac-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5eac-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5eac-141"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c5eac-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5eac-142">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5eac-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5eac-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c5eac-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5eac-144">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c5eac-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5eac-145"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c5eac-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5eac-146">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c5eac-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5eac-147"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c5eac-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c5eac-148">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c5eac-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5eac-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c5eac-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c5eac-150">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c5eac-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c5eac-151">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c5eac-151">See Also</span></span>

[<span data-ttu-id="c5eac-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c5eac-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c5eac-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="c5eac-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="c5eac-154">JetMove</span><span class="sxs-lookup"><span data-stu-id="c5eac-154">JetMove</span></span>](./jetmove-function.md)

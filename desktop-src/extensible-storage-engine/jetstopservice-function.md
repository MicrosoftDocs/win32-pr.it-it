---
description: 'Altre informazioni su: funzione JetStopService'
title: Funzione JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307806"
---
# <a name="jetstopservice-function"></a><span data-ttu-id="25dd7-103">Funzione JetStopService</span><span class="sxs-lookup"><span data-stu-id="25dd7-103">JetStopService Function</span></span>


<span data-ttu-id="25dd7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25dd7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopservice-function"></a><span data-ttu-id="25dd7-105">Funzione JetStopService</span><span class="sxs-lookup"><span data-stu-id="25dd7-105">JetStopService Function</span></span>

<span data-ttu-id="25dd7-106">La funzione **JetStopService** prepara un'istanza per la chiusura.</span><span class="sxs-lookup"><span data-stu-id="25dd7-106">The **JetStopService** function prepares an instance for termination.</span></span>

<span data-ttu-id="25dd7-107">**JetStopService** è la chiamata legacy quando è consentita una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="25dd7-107">**JetStopService** is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="25dd7-108">In questo caso, l'unica istanza attiva è quella preparata per la terminazione.</span><span class="sxs-lookup"><span data-stu-id="25dd7-108">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a><span data-ttu-id="25dd7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="25dd7-109">Parameters</span></span>

<span data-ttu-id="25dd7-110">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="25dd7-110">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="25dd7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25dd7-111">Return Value</span></span>

<span data-ttu-id="25dd7-112">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="25dd7-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="25dd7-113">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="25dd7-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25dd7-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="25dd7-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="25dd7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25dd7-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25dd7-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="25dd7-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="25dd7-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="25dd7-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25dd7-118">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="25dd7-118">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="25dd7-119">Non è chiaro quale istanza preparare per la terminazione quando si usa <strong>JetStopService</strong> con più modalità di istanza.</span><span class="sxs-lookup"><span data-stu-id="25dd7-119">It is not clear which instance to prepare for termination when using <strong>JetStopService</strong> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="25dd7-120"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25dd7-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25dd7-121">Se questa funzione ha esito positivo, viene preparata per una terminazione futura.</span><span class="sxs-lookup"><span data-stu-id="25dd7-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="25dd7-122">I passaggi necessari per preparare la chiusura includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="25dd7-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="25dd7-123">Arrestare la deframmentazione in linea se è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="25dd7-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="25dd7-124">Avviare una pulizia dell'archivio versioni.</span><span class="sxs-lookup"><span data-stu-id="25dd7-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="25dd7-125">Per ridurre la profondità del checkpoint, iniziare a scaricare le pagine dirty in Gestione buffer.</span><span class="sxs-lookup"><span data-stu-id="25dd7-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="25dd7-126">Evitare chiamate future alla maggior parte delle funzioni per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="25dd7-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="25dd7-127">Se questa funzione ha esito negativo, non verrà eseguita alcuna procedura per preparare la terminazione di un'istanza, quindi non si verificherà alcuna modifica allo stato dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="25dd7-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="25dd7-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="25dd7-128">Remarks</span></span>

<span data-ttu-id="25dd7-129">Questa funzione riduce il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non termina l'istanza.</span><span class="sxs-lookup"><span data-stu-id="25dd7-129">This function reduces the work the instance will have to do when terminated, but will not terminate the instance.</span></span> <span data-ttu-id="25dd7-130">Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria per l'uso di.</span><span class="sxs-lookup"><span data-stu-id="25dd7-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="25dd7-131">Si noti che la quantità di lavoro svolto in preparazione era minore in Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25dd7-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="25dd7-132">Quando la funzione ha esito positivo, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="25dd7-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="25dd7-133">Le funzioni ancora consentite dopo questa chiamata sono: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="25dd7-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="25dd7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25dd7-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25dd7-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="25dd7-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="25dd7-136">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="25dd7-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25dd7-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="25dd7-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="25dd7-138">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="25dd7-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25dd7-139"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="25dd7-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="25dd7-140">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="25dd7-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25dd7-141"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="25dd7-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="25dd7-142">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="25dd7-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25dd7-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="25dd7-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="25dd7-144">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="25dd7-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="25dd7-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="25dd7-145">See Also</span></span>

[<span data-ttu-id="25dd7-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="25dd7-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="25dd7-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="25dd7-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="25dd7-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="25dd7-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="25dd7-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="25dd7-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="25dd7-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="25dd7-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="25dd7-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="25dd7-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="25dd7-152">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="25dd7-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="25dd7-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="25dd7-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="25dd7-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="25dd7-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="25dd7-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="25dd7-155">JetTerm2</span></span>](./jetterm2-function.md)

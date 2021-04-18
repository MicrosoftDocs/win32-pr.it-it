---
description: 'Altre informazioni su: funzione JetResetTableSequential'
title: JetResetTableSequential (funzione)
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313096"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="c569b-103">JetResetTableSequential (funzione)</span><span class="sxs-lookup"><span data-stu-id="c569b-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="c569b-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c569b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="c569b-105">JetResetTableSequential (funzione)</span><span class="sxs-lookup"><span data-stu-id="c569b-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="c569b-106">La funzione **JetResetTableSequential** notifica al motore di database che l'applicazione non sta più analizzando l'intero indice corrente contenente un cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="c569b-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="c569b-107">Questa chiamata inverte una notifica inviata da [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="c569b-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="c569b-108">**Windows XP:**   **JetResetTableSequential** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c569b-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c569b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c569b-109">Parameters</span></span>

<span data-ttu-id="c569b-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c569b-110">*sesid*</span></span>

<span data-ttu-id="c569b-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c569b-111">The session to use for this call.</span></span>

<span data-ttu-id="c569b-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c569b-112">*tableid*</span></span>

<span data-ttu-id="c569b-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="c569b-113">The cursor to use for this call.</span></span>

<span data-ttu-id="c569b-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c569b-114">*grbit*</span></span>

<span data-ttu-id="c569b-115">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="c569b-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="c569b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c569b-116">Return Value</span></span>

<span data-ttu-id="c569b-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c569b-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c569b-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c569b-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c569b-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c569b-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="c569b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c569b-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c569b-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c569b-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c569b-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c569b-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c569b-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c569b-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c569b-124">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c569b-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c569b-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c569b-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c569b-126">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="c569b-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c569b-127">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c569b-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c569b-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c569b-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c569b-129">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c569b-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c569b-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c569b-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c569b-131">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c569b-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c569b-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c569b-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c569b-133">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="c569b-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c569b-134">In seguito all'esito positivo, l'indice corrente del cursore non è più ottimizzato per un'analisi sequenziale dell'intero indice.</span><span class="sxs-lookup"><span data-stu-id="c569b-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="c569b-135">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="c569b-135">No change to the database state will occur.</span></span>

<span data-ttu-id="c569b-136">In caso di errore, non si verificherà alcuna modifica alla configurazione del cursore.</span><span class="sxs-lookup"><span data-stu-id="c569b-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="c569b-137">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="c569b-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c569b-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="c569b-138">Remarks</span></span>

<span data-ttu-id="c569b-139">È possibile eseguire questa chiamata su un cursore che non è stato configurato in precedenza da una chiamata a [JetSetTableSequential](./jetsettablesequential-function.md).</span><span class="sxs-lookup"><span data-stu-id="c569b-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c569b-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c569b-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c569b-141"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c569b-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c569b-142">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c569b-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c569b-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c569b-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c569b-144">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c569b-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c569b-145"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c569b-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c569b-146">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c569b-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c569b-147"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c569b-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c569b-148">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c569b-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c569b-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c569b-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c569b-150">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c569b-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c569b-151">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c569b-151">See Also</span></span>

[<span data-ttu-id="c569b-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c569b-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c569b-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c569b-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c569b-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c569b-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c569b-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c569b-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c569b-156">JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="c569b-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="c569b-157">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c569b-157">JetStopService</span></span>](./jetstopservice-function.md)

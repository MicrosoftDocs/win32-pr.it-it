---
description: 'Altre informazioni su: funzione JetUnregisterCallback'
title: JetUnregisterCallback (funzione)
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401634"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="fbcf2-103">JetUnregisterCallback (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbcf2-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="fbcf2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fbcf2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="fbcf2-105">JetUnregisterCallback (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbcf2-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="fbcf2-106">La funzione **JetUnregisterCallback** consente all'applicazione di configurare il motore di database per arrestare l'invio di notifiche all'applicazione come richiesto in precedenza tramite [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbcf2-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="fbcf2-107">**Windows XP:**  **JetUnregisterCallback** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="fbcf2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbcf2-108">Parameters</span></span>

<span data-ttu-id="fbcf2-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fbcf2-109">*sesid*</span></span>

<span data-ttu-id="fbcf2-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-110">The session to use for this call.</span></span>

<span data-ttu-id="fbcf2-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="fbcf2-111">*tableid*</span></span>

<span data-ttu-id="fbcf2-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-112">The cursor to use for this call.</span></span>

<span data-ttu-id="fbcf2-113">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="fbcf2-113">*cbtyp*</span></span>

<span data-ttu-id="fbcf2-114">Maschera di maschera costituita dai motivi di callback che l'applicazione non desidera più ricevere notifiche.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="fbcf2-115">Per creare questa maschera di maschera, è sufficiente o combinare i motivi di callback validi dall'enumerazione [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcf2-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="fbcf2-116">*hCallbackId*</span><span class="sxs-lookup"><span data-stu-id="fbcf2-116">*hCallbackId*</span></span>

<span data-ttu-id="fbcf2-117">Handle del callback registrato restituito da [JetRegisterCallback](./jetregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="fbcf2-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="fbcf2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbcf2-118">Return Value</span></span>

<span data-ttu-id="fbcf2-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fbcf2-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcf2-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbcf2-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fbcf2-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="fbcf2-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbcf2-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fbcf2-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbcf2-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fbcf2-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-126">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fbcf2-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-128">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="fbcf2-129"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbcf2-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fbcf2-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-131">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fbcf2-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-133">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbcf2-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fbcf2-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-135">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="fbcf2-136"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fbcf2-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fbcf2-138">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fbcf2-139">Se questa funzione ha esito positivo, verrà annullata la registrazione del callback specificato per i motivi di callback indicati con la tabella associata al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="fbcf2-140">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-140">No change to the database state will occur.</span></span>

<span data-ttu-id="fbcf2-141">Se questa funzione ha esito negativo, non verrà annullata la registrazione del callback specificato.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="fbcf2-142">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fbcf2-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbcf2-143">Remarks</span></span>

<span data-ttu-id="fbcf2-144">La maschera di maschera specificata deve corrispondere esattamente alla maschera di maschera specificata durante la registrazione del callback.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="fbcf2-145">Il motore di database attualmente non supporta la rimozione di un subset di queste notifiche e non restituisce un errore quando si tenta di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fbcf2-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbcf2-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fbcf2-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fbcf2-148">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbcf2-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fbcf2-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fbcf2-150">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-151"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="fbcf2-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fbcf2-152">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbcf2-153"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="fbcf2-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fbcf2-154">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbcf2-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fbcf2-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fbcf2-156">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fbcf2-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fbcf2-157">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fbcf2-157">See Also</span></span>

[<span data-ttu-id="fbcf2-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="fbcf2-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="fbcf2-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fbcf2-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fbcf2-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="fbcf2-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="fbcf2-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fbcf2-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fbcf2-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fbcf2-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fbcf2-163">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="fbcf2-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="fbcf2-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="fbcf2-164">JetStopService</span></span>](./jetstopservice-function.md)

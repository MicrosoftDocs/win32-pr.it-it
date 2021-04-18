---
description: 'Altre informazioni su: funzione JetRegisterCallback'
title: Funzione JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306823"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="5cd64-103">Funzione JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="5cd64-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="5cd64-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5cd64-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="5cd64-105">Funzione JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="5cd64-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="5cd64-106">La funzione **JetRegisterCallback** consente all'applicazione di configurare il motore di database per inviare notifiche all'applicazione per eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="5cd64-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="5cd64-107">Queste notifiche sono associate a una tabella specifica e rimangono attive solo fino a quando l'istanza contenente la tabella non viene arrestata utilizzando [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="5cd64-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="5cd64-108">**Windows XP: JetRegisterCallback** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5cd64-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="5cd64-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cd64-109">Parameters</span></span>

<span data-ttu-id="5cd64-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5cd64-110">*sesid*</span></span>

<span data-ttu-id="5cd64-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5cd64-111">The session to use for this call.</span></span>

<span data-ttu-id="5cd64-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5cd64-112">*tableid*</span></span>

<span data-ttu-id="5cd64-113">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="5cd64-113">The cursor to use for this call.</span></span>

<span data-ttu-id="5cd64-114">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="5cd64-114">*cbtyp*</span></span>

<span data-ttu-id="5cd64-115">Maschera di bit costituita dai motivi di callback per i quali l'applicazione desidera ricevere le notifiche.</span><span class="sxs-lookup"><span data-stu-id="5cd64-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="5cd64-116">Per creare questa maschera di bit, è sufficiente o combinare i motivi di callback validi dall'enumerazione [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="5cd64-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="5cd64-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="5cd64-117">*pCallback*</span></span>

<span data-ttu-id="5cd64-118">Puntatore a funzione per la funzione di callback per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5cd64-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="5cd64-119">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="5cd64-119">*pvContext*</span></span>

<span data-ttu-id="5cd64-120">Specifica un puntatore di contesto che verrà assegnato alla funzione di callback per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5cd64-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="5cd64-121">*phCallbackId*</span><span class="sxs-lookup"><span data-stu-id="5cd64-121">*phCallbackId*</span></span>

<span data-ttu-id="5cd64-122">Restituisce un handle che può essere utilizzato in un secondo momento per annullare la registrazione della funzione di callback specificata utilizzando [JetUnregisterCallback](./jetunregistercallback-function.md).</span><span class="sxs-lookup"><span data-stu-id="5cd64-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="5cd64-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cd64-123">Return Value</span></span>

<span data-ttu-id="5cd64-124">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5cd64-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5cd64-125">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5cd64-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cd64-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5cd64-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="5cd64-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cd64-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5cd64-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5cd64-129">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5cd64-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cd64-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5cd64-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5cd64-131">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5cd64-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5cd64-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5cd64-133">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="5cd64-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="5cd64-134">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5cd64-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cd64-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5cd64-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5cd64-136">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="5cd64-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="5cd64-137">Questo errore viene restituito da <strong>JetRegisterCallback</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="5cd64-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="5cd64-138"><em>cbtyp</em> è zero,</span><span class="sxs-lookup"><span data-stu-id="5cd64-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="5cd64-139"><em>pCallback</em> è null.</span><span class="sxs-lookup"><span data-stu-id="5cd64-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="5cd64-140"><em>phCallbackId</em> è null.</span><span class="sxs-lookup"><span data-stu-id="5cd64-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5cd64-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5cd64-142">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="5cd64-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cd64-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5cd64-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cd64-144">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="5cd64-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5cd64-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5cd64-146">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="5cd64-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="5cd64-147">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5cd64-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cd64-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5cd64-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cd64-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="5cd64-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cd64-150">In seguito all'esito positivo, il callback specificato verrà registrato per i motivi di callback specificati con la tabella associata al cursore specificato.</span><span class="sxs-lookup"><span data-stu-id="5cd64-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="5cd64-151">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="5cd64-151">No change to the database state will occur.</span></span>

<span data-ttu-id="5cd64-152">In caso di errore, il callback non verrà registrato.</span><span class="sxs-lookup"><span data-stu-id="5cd64-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="5cd64-153">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="5cd64-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5cd64-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cd64-154">Remarks</span></span>

<span data-ttu-id="5cd64-155">Questo metodo consente all'applicazione di associare callback volatili a una tabella in un database.</span><span class="sxs-lookup"><span data-stu-id="5cd64-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="5cd64-156">Se l'applicazione vuole associare callback salvati in modo permanente a una tabella nel database, deve passare il callback a [JET_TABLECREATE](./jet-tablecreate-structure.md) usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="5cd64-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5cd64-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cd64-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5cd64-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5cd64-159">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5cd64-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cd64-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5cd64-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5cd64-161">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5cd64-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-162"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5cd64-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5cd64-163">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5cd64-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cd64-164"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5cd64-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5cd64-165">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5cd64-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cd64-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5cd64-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5cd64-167">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5cd64-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5cd64-168">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5cd64-168">See Also</span></span>

[<span data-ttu-id="5cd64-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="5cd64-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="5cd64-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="5cd64-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="5cd64-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5cd64-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5cd64-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="5cd64-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="5cd64-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5cd64-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5cd64-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5cd64-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5cd64-175">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="5cd64-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="5cd64-176">JetTerm</span><span class="sxs-lookup"><span data-stu-id="5cd64-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="5cd64-177">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="5cd64-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

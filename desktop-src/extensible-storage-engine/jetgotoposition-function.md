---
description: 'Altre informazioni su: funzione JetGotoPosition'
title: JetGotoPosition (funzione)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749719"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="3c609-103">JetGotoPosition (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c609-103">JetGotoPosition Function</span></span>


<span data-ttu-id="3c609-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3c609-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="3c609-105">JetGotoPosition (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c609-105">JetGotoPosition Function</span></span>

<span data-ttu-id="3c609-106">La funzione **JetGotoPosition** sposta un cursore in una nuova posizione che rappresenta una frazione della strada attraverso l'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="3c609-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="3c609-107">La frazione è approssimativamente uguale alla seguente:</span><span class="sxs-lookup"><span data-stu-id="3c609-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="3c609-108">precpos- \> centriesLT/precpos- \> centriesTotal</span><span class="sxs-lookup"><span data-stu-id="3c609-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="3c609-109">Questa operazione viene eseguita in risposta all'input della casella di scorrimento dell'utente che viene ricevuto quando l'utente tenta di visualizzare i dati che iniziano in parte tramite un set di dati.</span><span class="sxs-lookup"><span data-stu-id="3c609-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="3c609-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c609-110">Parameters</span></span>

<span data-ttu-id="3c609-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3c609-111">*sesid*</span></span>

<span data-ttu-id="3c609-112">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="3c609-112">The session to use for this call.</span></span>

<span data-ttu-id="3c609-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3c609-113">*tableid*</span></span>

<span data-ttu-id="3c609-114">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="3c609-114">The cursor to use for this call.</span></span>

<span data-ttu-id="3c609-115">*precpos*</span><span class="sxs-lookup"><span data-stu-id="3c609-115">*precpos*</span></span>

<span data-ttu-id="3c609-116">Descrizione della frazione da utilizzare per posizionare il cursore nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="3c609-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="3c609-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c609-117">Return Value</span></span>

<span data-ttu-id="3c609-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3c609-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3c609-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3c609-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c609-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3c609-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="3c609-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c609-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c609-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3c609-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3c609-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3c609-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c609-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3c609-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3c609-125">Non è stato possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="3c609-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c609-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3c609-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3c609-127">Non è stato possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="3c609-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3c609-128"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3c609-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c609-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3c609-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3c609-130">Il &gt; valore di precpos-cbStruct specificato non è una dimensione valida per la struttura <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> o precpos- &gt; centriesLT è maggiore di precpos- &gt; centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="3c609-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c609-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3c609-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3c609-132">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="3c609-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c609-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="3c609-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="3c609-134">Questo errore verrà restituito se l'indice è vuoto.</span><span class="sxs-lookup"><span data-stu-id="3c609-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c609-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3c609-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3c609-136">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="3c609-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c609-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3c609-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3c609-138">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="3c609-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="3c609-139"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3c609-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c609-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3c609-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3c609-141">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="3c609-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c609-142">Se questa funzione ha esito positivo, il cursore viene spostato in un record corrente che rappresenta una frazione della strada attraverso l'indice in cui la frazione è precpos- \> centriesLT divisa per precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="3c609-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="3c609-143">Se questa funzione ha esito negativo, la posizione del cursore viene lasciata invariata.</span><span class="sxs-lookup"><span data-stu-id="3c609-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3c609-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c609-144">Remarks</span></span>

<span data-ttu-id="3c609-145">Questa operazione sposta il cursore nella tabella in una posizione nel punto approssimativo seguente: precpos- \> centriesLT diviso per precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="3c609-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="3c609-146">Quando si verificano continuamente aggiornamenti sulla tabella, le chiamate successive con lo stesso [JET_RECPOS](./jet-recpos-structure.md) possono spostare il cursore in posizioni diverse nell'indice, sia prima che dopo la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="3c609-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="3c609-147">L'isolamento transazionale non si applica al posizionamento tramite [JET_RECPOS](./jet-recpos-structure.md) perché dipende dalle proprietà fisiche dell'indice che non sono isolate dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="3c609-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="3c609-148">[JET_RECPOS](./jet-recpos-structure.md) non deve essere usato per descrivere un record all'interno di una tabella o per riposizionare un record vicino a un record esistente.</span><span class="sxs-lookup"><span data-stu-id="3c609-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="3c609-149">Al contrario, i segnalibri per un record esistente devono essere recuperati dopo un **JetGotoPosition** iniziale e quindi usati per riposizionare lo stesso record.</span><span class="sxs-lookup"><span data-stu-id="3c609-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3c609-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c609-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c609-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3c609-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3c609-152">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3c609-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c609-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3c609-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3c609-154">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3c609-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c609-155"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3c609-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3c609-156">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3c609-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c609-157"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3c609-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3c609-158">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3c609-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c609-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3c609-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3c609-160">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3c609-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3c609-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c609-161">See Also</span></span>

[<span data-ttu-id="3c609-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3c609-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="3c609-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3c609-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3c609-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3c609-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3c609-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3c609-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3c609-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="3c609-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="3c609-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="3c609-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

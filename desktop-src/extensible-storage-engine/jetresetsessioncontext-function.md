---
description: 'Altre informazioni su: funzione JetResetSessionContext'
title: JetResetSessionContext (funzione)
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231798"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="cc332-103">JetResetSessionContext (funzione)</span><span class="sxs-lookup"><span data-stu-id="cc332-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="cc332-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc332-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="cc332-105">JetResetSessionContext (funzione)</span><span class="sxs-lookup"><span data-stu-id="cc332-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="cc332-106">La funzione **JetResetSessionContext** Annulla l'associazione di una sessione dal thread corrente.</span><span class="sxs-lookup"><span data-stu-id="cc332-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="cc332-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc332-107">Parameters</span></span>

<span data-ttu-id="cc332-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cc332-108">*sesid*</span></span>

<span data-ttu-id="cc332-109">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="cc332-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="cc332-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc332-110">Return Value</span></span>

<span data-ttu-id="cc332-111">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="cc332-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cc332-112">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="cc332-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc332-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cc332-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="cc332-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc332-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc332-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cc332-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cc332-116">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="cc332-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc332-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cc332-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cc332-118">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="cc332-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="cc332-119">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc332-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc332-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cc332-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cc332-121">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="cc332-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc332-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cc332-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc332-123">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="cc332-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc332-124">JET_errSessionContextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="cc332-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="cc332-125">Impossibile dissociare la sessione dal thread corrente perché è associata a un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="cc332-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc332-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cc332-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc332-127">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="cc332-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc332-128">In seguito all'esito positivo, la sessione verrà dissociata dal thread corrente.</span><span class="sxs-lookup"><span data-stu-id="cc332-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="cc332-129">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="cc332-129">No change to the database state will occur.</span></span>

<span data-ttu-id="cc332-130">In caso di errore, lo stato della sessione rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="cc332-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="cc332-131">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="cc332-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc332-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc332-132">Remarks</span></span>

<span data-ttu-id="cc332-133">**JetResetSessionContext** deve essere chiamato sullo stesso thread che ha chiamato [JetSetSessionContext](./jetsetsessioncontext-function.md) per una determinata sessione.</span><span class="sxs-lookup"><span data-stu-id="cc332-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc332-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc332-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc332-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cc332-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc332-136">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cc332-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc332-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cc332-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc332-138">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cc332-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc332-139"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="cc332-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc332-140">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc332-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc332-141"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="cc332-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cc332-142">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cc332-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc332-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cc332-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cc332-144">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cc332-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc332-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cc332-145">See Also</span></span>

[<span data-ttu-id="cc332-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="cc332-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="cc332-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc332-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc332-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cc332-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cc332-149">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="cc332-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)

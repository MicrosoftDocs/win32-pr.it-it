---
description: 'Altre informazioni su: funzione JetOSSnapshotPrepareInstance'
title: JetOSSnapshotPrepareInstance (funzione)
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104402040"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="b4b86-103">JetOSSnapshotPrepareInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4b86-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="b4b86-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b4b86-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="b4b86-105">JetOSSnapshotPrepareInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4b86-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="b4b86-106">La funzione **JetOSSnapshotPrepareInstance** seleziona un'istanza specifica che deve far parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="b4b86-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="b4b86-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4b86-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="b4b86-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4b86-108">Parameters</span></span>

<span data-ttu-id="b4b86-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="b4b86-109">*snapId*</span></span>

<span data-ttu-id="b4b86-110">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="b4b86-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="b4b86-111">*istanza*</span><span class="sxs-lookup"><span data-stu-id="b4b86-111">*instance*</span></span>

<span data-ttu-id="b4b86-112">Istanza di che verrà utilizzata per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="b4b86-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="b4b86-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b4b86-113">*grbit*</span></span>

<span data-ttu-id="b4b86-114">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b4b86-114">The options for this call.</span></span> <span data-ttu-id="b4b86-115">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="b4b86-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="b4b86-116">L'unico valore valido è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b4b86-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="b4b86-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4b86-117">Return Value</span></span>

<span data-ttu-id="b4b86-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b4b86-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b4b86-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b4b86-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4b86-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b4b86-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="b4b86-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4b86-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4b86-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b4b86-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b4b86-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b4b86-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b86-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b4b86-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b4b86-125">Il puntatore di ID snapshot è <strong>null</strong> o il parametro <em>grbit</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="b4b86-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b86-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="b4b86-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="b4b86-127">Una sessione snapshot è già in corso.</span><span class="sxs-lookup"><span data-stu-id="b4b86-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b86-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="b4b86-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="b4b86-129">Identificatore per la sessione snapshot non valido.</span><span class="sxs-lookup"><span data-stu-id="b4b86-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4b86-130">Se questa funzione ha esito positivo, l'istanza specificata sarà parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="b4b86-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="b4b86-131">Se questa funzione ha esito negativo, non viene apportata alcuna modifica allo stato del motore.</span><span class="sxs-lookup"><span data-stu-id="b4b86-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b4b86-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4b86-132">Remarks</span></span>

<span data-ttu-id="b4b86-133">La normale chiamata di sequenza API è: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), seguita facoltativamente da una o più chiamate a **JetOSSnapshotPrepareInstance** e quindi da [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4b86-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="b4b86-134">Una volta avviato il blocco, è possibile terminarlo utilizzando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4b86-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="b4b86-135">In qualsiasi momento dopo la preparazione, la sessione snapshot può essere terminata improvvisamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4b86-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="b4b86-136">Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="b4b86-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="b4b86-137">Se **JetOSSnapshotPrepareInstance** non viene chiamato tra l'inizio della sessione ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e il momento di blocco ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), tutte le istanze in esecuzione nel motore verranno bloccate e diventeranno parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="b4b86-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="b4b86-138">Questo problema si verifica per due motivi:</span><span class="sxs-lookup"><span data-stu-id="b4b86-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="b4b86-139">Semplifica il codice per gli utenti che desiderano tutte le istanze.</span><span class="sxs-lookup"><span data-stu-id="b4b86-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="b4b86-140">Consente la compatibilità con le versioni precedenti per i chiamanti delle API snapshot.</span><span class="sxs-lookup"><span data-stu-id="b4b86-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b4b86-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4b86-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4b86-142"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b4b86-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b86-143">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4b86-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b86-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b4b86-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b86-145">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b4b86-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b86-146"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b4b86-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b86-147">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b4b86-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4b86-148"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b4b86-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b86-149">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b4b86-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4b86-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b4b86-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b4b86-151">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b4b86-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b4b86-152">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b4b86-152">See Also</span></span>

[<span data-ttu-id="b4b86-153">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="b4b86-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="b4b86-154">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="b4b86-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="b4b86-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b4b86-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b4b86-156">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="b4b86-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="b4b86-157">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="b4b86-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="b4b86-158">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="b4b86-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="b4b86-159">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="b4b86-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="b4b86-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="b4b86-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

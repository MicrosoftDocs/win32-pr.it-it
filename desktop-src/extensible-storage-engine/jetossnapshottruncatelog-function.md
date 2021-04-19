---
description: 'Altre informazioni su: funzione JetOSSnapshotTruncateLog'
title: JetOSSnapshotTruncateLog (funzione)
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316451"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="e314c-103">JetOSSnapshotTruncateLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="e314c-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="e314c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e314c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="e314c-105">JetOSSnapshotTruncateLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="e314c-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="e314c-106">La funzione **JetOSSnapshotTruncateLog** consente il troncamento del log per tutte le istanze che fanno parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="e314c-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="e314c-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e314c-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e314c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e314c-108">Parameters</span></span>

<span data-ttu-id="e314c-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="e314c-109">*snapId*</span></span>

<span data-ttu-id="e314c-110">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="e314c-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="e314c-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e314c-111">*grbit*</span></span>

<span data-ttu-id="e314c-112">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="e314c-112">The options for this call.</span></span> <span data-ttu-id="e314c-113">Questo parametro può avere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e314c-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e314c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e314c-114">Value</span></span></p></th>
<th><p><span data-ttu-id="e314c-115">Significato</span><span class="sxs-lookup"><span data-stu-id="e314c-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e314c-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="e314c-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="e314c-117">Tutti i database sono collegati, quindi il motore di archiviazione può calcolare ed eseguire il troncamento del log.</span><span class="sxs-lookup"><span data-stu-id="e314c-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e314c-118">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="e314c-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="e314c-119">Non si verificherà alcun troncamento.</span><span class="sxs-lookup"><span data-stu-id="e314c-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e314c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e314c-120">Return Value</span></span>

<span data-ttu-id="e314c-121">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="e314c-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e314c-122">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="e314c-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e314c-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e314c-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="e314c-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e314c-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e314c-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e314c-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e314c-126">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e314c-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e314c-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="e314c-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="e314c-128">Il parametro <em>grbit</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="e314c-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e314c-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="e314c-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="e314c-130">La sessione snapshot non è nello stato in cui può verificarsi un troncamento.</span><span class="sxs-lookup"><span data-stu-id="e314c-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="e314c-131">Le cause possibili sono:</span><span class="sxs-lookup"><span data-stu-id="e314c-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="e314c-132">la chiamata viene eseguita dopo il timeout della sessione snapshot</span><span class="sxs-lookup"><span data-stu-id="e314c-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="e314c-133">la sessione è stata specificata come snapshot di copia</span><span class="sxs-lookup"><span data-stu-id="e314c-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e314c-134">In caso di esito positivo, i file di log per una o tutte le istanze della sessione snapshot verranno troncati, se possibile.</span><span class="sxs-lookup"><span data-stu-id="e314c-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e314c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="e314c-135">Remarks</span></span>

<span data-ttu-id="e314c-136">Questa funzione deve essere chiamata solo se lo snapshot è stato creato con l'opzione JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="e314c-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="e314c-137">In caso contrario, la sessione snapshot verrà terminata dopo la chiamata a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e314c-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e314c-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e314c-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e314c-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e314c-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e314c-140">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e314c-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e314c-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e314c-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e314c-142">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e314c-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e314c-143"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e314c-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e314c-144">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e314c-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e314c-145"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="e314c-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e314c-146">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e314c-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e314c-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e314c-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e314c-148">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e314c-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e314c-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e314c-149">See Also</span></span>

[<span data-ttu-id="e314c-150">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="e314c-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="e314c-151">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="e314c-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="e314c-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e314c-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e314c-153">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="e314c-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="e314c-154">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="e314c-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="e314c-155">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="e314c-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="e314c-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="e314c-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

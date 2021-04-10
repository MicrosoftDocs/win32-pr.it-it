---
description: 'Altre informazioni su: funzione JetOSSnapshotTruncateLogInstance'
title: JetOSSnapshotTruncateLogInstance (funzione)
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749703"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="3588f-103">JetOSSnapshotTruncateLogInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="3588f-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="3588f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3588f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="3588f-105">JetOSSnapshotTruncateLogInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="3588f-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="3588f-106">La funzione **JetOSSnapshotTruncateLogInstance** tronca il log per un'istanza specificata durante una sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="3588f-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="3588f-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3588f-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="3588f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3588f-108">Parameters</span></span>

<span data-ttu-id="3588f-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="3588f-109">*snapId*</span></span>

<span data-ttu-id="3588f-110">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="3588f-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="3588f-111">*istanza*</span><span class="sxs-lookup"><span data-stu-id="3588f-111">*instance*</span></span>

<span data-ttu-id="3588f-112">Istanza di che verrà utilizzata per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="3588f-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="3588f-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3588f-113">*grbit*</span></span>

<span data-ttu-id="3588f-114">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="3588f-114">The options for this call.</span></span> <span data-ttu-id="3588f-115">Questo parametro può avere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3588f-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="3588f-116">*grbit* può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3588f-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3588f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3588f-117">Value</span></span></p></th>
<th><p><span data-ttu-id="3588f-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3588f-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3588f-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="3588f-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="3588f-120">Tutti i database sono collegati, quindi il motore di archiviazione può calcolare ed eseguire il troncamento del log.</span><span class="sxs-lookup"><span data-stu-id="3588f-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3588f-121">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="3588f-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="3588f-122">Non si verificherà alcun troncamento.</span><span class="sxs-lookup"><span data-stu-id="3588f-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3588f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3588f-123">Return Value</span></span>

<span data-ttu-id="3588f-124">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3588f-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3588f-125">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3588f-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3588f-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3588f-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="3588f-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3588f-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3588f-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3588f-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3588f-129">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3588f-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3588f-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="3588f-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="3588f-131">Il parametro <em>grbit</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="3588f-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3588f-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="3588f-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="3588f-133">La sessione snapshot non è nello stato in cui può verificarsi un troncamento.</span><span class="sxs-lookup"><span data-stu-id="3588f-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="3588f-134">Le cause possibili sono:</span><span class="sxs-lookup"><span data-stu-id="3588f-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3588f-135">La chiamata viene completata dopo il timeout della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="3588f-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="3588f-136">La sessione è stata specificata come snapshot di copia.</span><span class="sxs-lookup"><span data-stu-id="3588f-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3588f-137">Se questa funzione ha esito positivo, i file di log per una o tutte le istanze che fanno parte della sessione snapshot verranno troncati, se possibile.</span><span class="sxs-lookup"><span data-stu-id="3588f-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3588f-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="3588f-138">Remarks</span></span>

<span data-ttu-id="3588f-139">Questa funzione deve essere chiamata solo se lo snapshot è stato creato con l'opzione JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="3588f-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="3588f-140">In caso contrario, la sessione snapshot termina dopo la chiamata a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="3588f-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="3588f-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3588f-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3588f-142"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3588f-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3588f-143">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3588f-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3588f-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3588f-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3588f-145">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3588f-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3588f-146"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3588f-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3588f-147">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3588f-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3588f-148"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3588f-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3588f-149">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3588f-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3588f-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3588f-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3588f-151">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3588f-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3588f-152">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3588f-152">See Also</span></span>

[<span data-ttu-id="3588f-153">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="3588f-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="3588f-154">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="3588f-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="3588f-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3588f-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3588f-156">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="3588f-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="3588f-157">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="3588f-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="3588f-158">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="3588f-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="3588f-159">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="3588f-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

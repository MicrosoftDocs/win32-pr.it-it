---
description: 'Altre informazioni su: funzione JetOSSnapshotEnd'
title: JetOSSnapshotEnd (funzione)
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128170"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="1d564-103">JetOSSnapshotEnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="1d564-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="1d564-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d564-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="1d564-105">JetOSSnapshotEnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="1d564-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="1d564-106">La funzione **JetOSSnapshotEnd** notifica al motore che la sessione snapshot è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1d564-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="1d564-107">**Windows Vista:**  **JetOSSnapshotEnd** è stato introdotto in Windows Vista:.</span><span class="sxs-lookup"><span data-stu-id="1d564-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="1d564-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d564-108">Parameters</span></span>

<span data-ttu-id="1d564-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="1d564-109">*snapId*</span></span>

<span data-ttu-id="1d564-110">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="1d564-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="1d564-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1d564-111">*grbit*</span></span>

<span data-ttu-id="1d564-112">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1d564-112">The options for this call.</span></span> <span data-ttu-id="1d564-113">Questo parametro può avere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d564-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d564-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1d564-114">Value</span></span></p></th>
<th><p><span data-ttu-id="1d564-115">Significato</span><span class="sxs-lookup"><span data-stu-id="1d564-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d564-116">0</span><span class="sxs-lookup"><span data-stu-id="1d564-116">0</span></span></p></td>
<td><p><span data-ttu-id="1d564-117">Fine corretta della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="1d564-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d564-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="1d564-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="1d564-119">La sessione snapshot è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="1d564-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1d564-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d564-120">Return Value</span></span>

<span data-ttu-id="1d564-121">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="1d564-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1d564-122">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1d564-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d564-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1d564-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="1d564-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d564-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d564-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1d564-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1d564-126">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="1d564-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d564-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="1d564-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="1d564-128">Una delle opzioni richieste non è valida, viene usata in modo errato o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="1d564-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d564-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="1d564-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="1d564-130">Una sessione snapshot è già in corso.</span><span class="sxs-lookup"><span data-stu-id="1d564-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="1d564-131">ma questa operazione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="1d564-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d564-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="1d564-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="1d564-133">Identificatore per la sessione snapshot non valido.</span><span class="sxs-lookup"><span data-stu-id="1d564-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d564-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="1d564-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="1d564-135">Il timeout della sessione snapshot è stato interno prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="1d564-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="1d564-136">Di conseguenza, le operazioni di i/o restituite al normale prima che questa chiamata venisse eseguita.</span><span class="sxs-lookup"><span data-stu-id="1d564-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d564-137">Se questa funzione ha esito positivo, verrà completata una sessione snapshot e verrà ripreso il normale comportamento del motore.</span><span class="sxs-lookup"><span data-stu-id="1d564-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="1d564-138">Una nuova sessione snapshot può essere avviata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="1d564-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="1d564-139">Se questa funzione ha esito negativo, il codice restituito JET_errOSSnapshotTimeOut restituisce e la sessione snapshot corrente termina, ma il blocco di IOs durante il periodo dello snapshot non è stato rispettato internamente.</span><span class="sxs-lookup"><span data-stu-id="1d564-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="1d564-140">Per tutti gli altri errori lo stato della sessione snapshot non verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="1d564-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1d564-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d564-141">Remarks</span></span>

<span data-ttu-id="1d564-142">Questa funzione viene chiamata solo se [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) è stato chiamato con JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="1d564-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="1d564-143">Per eseguire la verifica dello snapshot e il troncamento del log, è necessario completare la sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="1d564-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="1d564-144">Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="1d564-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1d564-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d564-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d564-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1d564-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d564-147">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d564-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d564-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1d564-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d564-149">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1d564-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d564-150"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1d564-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d564-151">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1d564-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d564-152"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1d564-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1d564-153">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1d564-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d564-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1d564-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1d564-155">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1d564-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1d564-156">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1d564-156">See Also</span></span>

[<span data-ttu-id="1d564-157">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="1d564-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="1d564-158">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="1d564-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="1d564-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1d564-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1d564-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="1d564-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

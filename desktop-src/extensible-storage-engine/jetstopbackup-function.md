---
description: 'Altre informazioni su: funzione JetStopBackup'
title: JetStopBackup (funzione)
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323797"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="f0708-103">JetStopBackup (funzione)</span><span class="sxs-lookup"><span data-stu-id="f0708-103">JetStopBackup Function</span></span>


<span data-ttu-id="f0708-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f0708-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="f0708-105">JetStopBackup (funzione)</span><span class="sxs-lookup"><span data-stu-id="f0708-105">JetStopBackup Function</span></span>

<span data-ttu-id="f0708-106">La funzione **JetStopBackup** impedisce a tutte le attività correlate al backup di flusso di continuare su un'istanza in esecuzione specifica, chiudendo in tal modo il backup di flusso in modo prevedibile.</span><span class="sxs-lookup"><span data-stu-id="f0708-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="f0708-107">**Windows XP:**  Questa funzione è stata introdotta in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0708-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="f0708-108">[JetStopService](./jetstopservice-function.md) è la chiamata legacy quando è consentita una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="f0708-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="f0708-109">In questo caso, l'unica istanza attiva è quella preparata per la terminazione.</span><span class="sxs-lookup"><span data-stu-id="f0708-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="f0708-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0708-110">Parameters</span></span>

<span data-ttu-id="f0708-111">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="f0708-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="f0708-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0708-112">Return Value</span></span>

<span data-ttu-id="f0708-113">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f0708-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f0708-114">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f0708-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0708-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f0708-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="f0708-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0708-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0708-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f0708-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f0708-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f0708-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0708-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f0708-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f0708-120">Non è chiaro quale istanza preparare per la terminazione quando si usa <a href="gg269240(v=exchg.10).md">JetStopService</a> con più modalità di istanza.</span><span class="sxs-lookup"><span data-stu-id="f0708-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="f0708-121"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0708-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f0708-122">Se questa funzione ha esito positivo, l'istanza di avrà esito negativo per le nuove API di backup di flusso.</span><span class="sxs-lookup"><span data-stu-id="f0708-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="f0708-123">Se questa funzione ha esito negativo, non verrà eseguito alcun passaggio per preparare la terminazione del backup nell'istanza e non si verificherà alcuna modifica allo stato dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f0708-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f0708-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0708-124">Remarks</span></span>

<span data-ttu-id="f0708-125">Il backup viene in genere attivato da un evento esterno al meccanismo di processo e tramite questa API, l'applicazione ESENT stessa effettuerà altre chiamate alle API di backup di flusso per avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f0708-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="f0708-126">La maggior parte delle API di backup di flusso inizierà a non riuscire con JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="f0708-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="f0708-127">Di conseguenza, lo stato di avanzamento del backup di flusso, ad esempio [JetReadFileInstance](./jetreadfileinstance-function.md), restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="f0708-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="f0708-128">Verranno comunque consentite le operazioni di backup che fanno parte della terminazione del backup, ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0708-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f0708-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0708-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0708-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f0708-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f0708-131">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f0708-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0708-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f0708-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f0708-133">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f0708-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0708-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f0708-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f0708-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f0708-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0708-136"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f0708-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f0708-137">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f0708-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0708-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f0708-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f0708-139">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f0708-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f0708-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f0708-140">See Also</span></span>

[<span data-ttu-id="f0708-141">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="f0708-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="f0708-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f0708-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f0708-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f0708-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f0708-144">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="f0708-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="f0708-145">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f0708-145">JetStopService</span></span>](./jetstopservice-function.md)

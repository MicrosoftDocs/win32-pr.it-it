---
description: 'Altre informazioni su: funzione JetStopBackupInstance'
title: JetStopBackupInstance (funzione)
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128631"
---
# <a name="jetstopbackupinstance-function"></a><span data-ttu-id="7c672-103">JetStopBackupInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="7c672-103">JetStopBackupInstance Function</span></span>


<span data-ttu-id="7c672-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7c672-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackupinstance-function"></a><span data-ttu-id="7c672-105">JetStopBackupInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="7c672-105">JetStopBackupInstance Function</span></span>

<span data-ttu-id="7c672-106">La funzione **JetStopBackupInstance** impedisce che l'attività correlata al backup di flusso continui su un'istanza in esecuzione specifica, chiudendo in tal modo il backup del flusso in modo prevedibile.</span><span class="sxs-lookup"><span data-stu-id="7c672-106">The **JetStopBackupInstance** function prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="7c672-107">**Windows XP:**  **JetStopBackupInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c672-107">**Windows XP:**  **JetStopBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="7c672-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c672-108">Parameters</span></span>

<span data-ttu-id="7c672-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="7c672-109">*instance*</span></span>

<span data-ttu-id="7c672-110">Identifica l'istanza in esecuzione da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="7c672-110">Identifies the running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="7c672-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c672-111">Return Value</span></span>

<span data-ttu-id="7c672-112">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="7c672-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7c672-113">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="7c672-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c672-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7c672-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="7c672-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c672-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c672-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7c672-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7c672-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="7c672-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c672-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7c672-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7c672-119">Il valore del parametro di istanza specificato non è valido (non è un'istanza attualmente in esecuzione).</span><span class="sxs-lookup"><span data-stu-id="7c672-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="7c672-120"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c672-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c672-121">Se questa funzione ha esito positivo, l'istanza specificata non riuscirà a eseguire alcuna nuova API di backup di flusso.</span><span class="sxs-lookup"><span data-stu-id="7c672-121">If this function succeeds, the instance that was specified will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="7c672-122">Se questa funzione ha esito negativo, non verrà eseguito alcun passaggio per preparare la terminazione del backup nell'istanza e non si verificherà alcuna modifica allo stato dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7c672-122">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7c672-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c672-123">Remarks</span></span>

<span data-ttu-id="7c672-124">Il backup viene in genere attivato da un evento esterno al meccanismo di processo e tramite questa API, l'applicazione ESENT stessa effettuerà altre chiamate alle API di backup di flusso per avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7c672-124">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="7c672-125">La maggior parte delle API di backup di flusso inizierà a non riuscire con JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="7c672-125">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="7c672-126">Di conseguenza, lo stato di avanzamento del backup di flusso, ad esempio [JetReadFileInstance](./jetreadfileinstance-function.md), restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="7c672-126">As such, any streaming backup progress (such as [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="7c672-127">Verranno comunque consentite le operazioni di backup che fanno parte della terminazione del backup (ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)).</span><span class="sxs-lookup"><span data-stu-id="7c672-127">Backup operations which are part of the backup termination (like [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7c672-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c672-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c672-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7c672-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7c672-130">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c672-130">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c672-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7c672-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c672-132">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7c672-132">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c672-133"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="7c672-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7c672-134">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="7c672-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c672-135"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="7c672-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7c672-136">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7c672-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c672-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7c672-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7c672-138">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7c672-138">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7c672-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7c672-139">See Also</span></span>

[<span data-ttu-id="7c672-140">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7c672-140">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7c672-141">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7c672-141">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7c672-142">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="7c672-142">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="7c672-143">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="7c672-143">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="7c672-144">JetStopService</span><span class="sxs-lookup"><span data-stu-id="7c672-144">JetStopService</span></span>](./jetstopservice-function.md)

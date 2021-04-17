---
description: 'Altre informazioni su: funzione JetBeginExternalBackupInstance'
title: JetBeginExternalBackupInstance (funzione)
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484244"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="b1086-103">JetBeginExternalBackupInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1086-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="b1086-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b1086-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="b1086-105">JetBeginExternalBackupInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1086-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="b1086-106">La funzione **JetBeginExternalBackupInstance** avvia un backup esterno mentre il motore e il database sono online e attivi.</span><span class="sxs-lookup"><span data-stu-id="b1086-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="b1086-107">**Windows XP: JetBeginExternalBackupInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1086-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b1086-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1086-108">Parameters</span></span>

<span data-ttu-id="b1086-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="b1086-109">*instance*</span></span>

<span data-ttu-id="b1086-110">Istanza di database da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b1086-110">The database instance to use for this call.</span></span>

<span data-ttu-id="b1086-111">Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="b1086-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="b1086-112">In questo caso, l'utilizzo di questa istanza globale è implicito.</span><span class="sxs-lookup"><span data-stu-id="b1086-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="b1086-113">Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="b1086-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="b1086-114">In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="b1086-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="b1086-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b1086-115">*grbit*</span></span>

<span data-ttu-id="b1086-116">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1086-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1086-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b1086-117">Value</span></span></p></th>
<th><p><span data-ttu-id="b1086-118">Significato</span><span class="sxs-lookup"><span data-stu-id="b1086-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1086-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="b1086-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="b1086-120">Questo flag è deprecato.</span><span class="sxs-lookup"><span data-stu-id="b1086-120">This flag is deprecated.</span></span> <span data-ttu-id="b1086-121">L'utilizzo di questo bit comporterà la restituzione JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="b1086-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1086-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="b1086-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="b1086-123">Crea un backup incrementale anziché un backup completo.</span><span class="sxs-lookup"><span data-stu-id="b1086-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="b1086-124">Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</span><span class="sxs-lookup"><span data-stu-id="b1086-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1086-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="b1086-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="b1086-126">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="b1086-126">Reserved for future use.</span></span> <span data-ttu-id="b1086-127">Definito per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1086-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b1086-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1086-128">Return Value</span></span>

<span data-ttu-id="b1086-129">Il sistema può generare codici di esito positivo o negativo in seguito a una chiamata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b1086-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="b1086-130">Per un elenco completo degli errori per questa API, vedere [codici di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b1086-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="b1086-131">Vedere [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="b1086-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="b1086-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1086-132">Remarks</span></span>

<span data-ttu-id="b1086-133">**JetBeginExternalBackupInstance** è la prima funzione in una serie di funzioni che devono essere chiamate per eseguire un backup online (non basato su VSS) riuscito.</span><span class="sxs-lookup"><span data-stu-id="b1086-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="b1086-134">Vedere anche [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) e [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="b1086-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="b1086-135">Un backup esterno può essere utilizzato per implementare backup completi, incrementali o differenziali.</span><span class="sxs-lookup"><span data-stu-id="b1086-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="b1086-136">Il backup sarà fuzzy, in quanto il backup sarà coerente a un singolo momento della cronologia delle transazioni, ma al momento non è possibile controllare il momento esatto.</span><span class="sxs-lookup"><span data-stu-id="b1086-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b1086-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1086-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1086-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b1086-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b1086-139">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b1086-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1086-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b1086-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b1086-141">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b1086-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1086-142"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b1086-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b1086-143">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b1086-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1086-144"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b1086-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b1086-145">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b1086-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1086-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b1086-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b1086-147">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b1086-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b1086-148">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b1086-148">See Also</span></span>

[<span data-ttu-id="b1086-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b1086-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b1086-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b1086-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b1086-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b1086-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b1086-152">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b1086-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b1086-153">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="b1086-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="b1086-154">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="b1086-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="b1086-155">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="b1086-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="b1086-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="b1086-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="b1086-157">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="b1086-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="b1086-158">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="b1086-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="b1086-159">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="b1086-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="b1086-160">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="b1086-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="b1086-161">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="b1086-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="b1086-162">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="b1086-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)

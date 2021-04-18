---
description: 'Altre informazioni su: funzione JetOSSnapshotGetFreezeInfo'
title: JetOSSnapshotGetFreezeInfo (funzione)
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315612"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="2f53e-103">JetOSSnapshotGetFreezeInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f53e-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="2f53e-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2f53e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="2f53e-105">JetOSSnapshotGetFreezeInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f53e-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="2f53e-106">La funzione **JetOSSnapshotGetFreezeInfo** recupera l'elenco di istanze e database che fanno parte della sessione snapshot in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="2f53e-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="2f53e-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f53e-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2f53e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f53e-108">Parameters</span></span>

<span data-ttu-id="2f53e-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="2f53e-109">*snapId*</span></span>

<span data-ttu-id="2f53e-110">Identificatore della sessione snapshot da avviare.</span><span class="sxs-lookup"><span data-stu-id="2f53e-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="2f53e-111">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="2f53e-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="2f53e-112">Numero di istanze attualmente in esecuzione che fanno parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="2f53e-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="2f53e-113">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="2f53e-113">*paInstanceInfo*</span></span>

<span data-ttu-id="2f53e-114">Matrice di strutture, una per ogni istanza in esecuzione, che descrive l'istanza e i database che ne fanno parte.</span><span class="sxs-lookup"><span data-stu-id="2f53e-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="2f53e-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2f53e-115">*grbit*</span></span>

<span data-ttu-id="2f53e-116">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2f53e-116">The options for this call.</span></span> <span data-ttu-id="2f53e-117">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="2f53e-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="2f53e-118">L'unico valore valido è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2f53e-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="2f53e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f53e-119">Return Value</span></span>

<span data-ttu-id="2f53e-120">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="2f53e-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2f53e-121">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2f53e-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f53e-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2f53e-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="2f53e-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f53e-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f53e-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2f53e-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2f53e-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="2f53e-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f53e-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="2f53e-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="2f53e-127">La funzione non è riuscita a causa di una condizione di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="2f53e-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f53e-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2f53e-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2f53e-129"><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="2f53e-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f53e-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="2f53e-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="2f53e-131">Identificatore per la sessione snapshot non valido.</span><span class="sxs-lookup"><span data-stu-id="2f53e-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f53e-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="2f53e-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="2f53e-133">Una sessione snapshot non è in corso.</span><span class="sxs-lookup"><span data-stu-id="2f53e-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f53e-134">Se questa funzione ha esito positivo, le informazioni sull'istanza vengono riempite correttamente e devono essere liberate in un secondo momento chiamando [JetFreeBuffer](./jetfreebuffer-function.md) con il puntatore alla matrice di informazioni sull'istanza restituita.</span><span class="sxs-lookup"><span data-stu-id="2f53e-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="2f53e-135">Se questa funzione ha esito negativo, non viene apportata alcuna modifica allo stato del motore.</span><span class="sxs-lookup"><span data-stu-id="2f53e-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2f53e-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f53e-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f53e-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2f53e-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2f53e-138">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f53e-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f53e-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2f53e-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2f53e-140">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f53e-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f53e-141"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2f53e-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2f53e-142">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2f53e-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f53e-143"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2f53e-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2f53e-144">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2f53e-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f53e-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2f53e-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2f53e-146">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2f53e-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f53e-147"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2f53e-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2f53e-148">Implementato come <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) e <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2f53e-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2f53e-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2f53e-149">See Also</span></span>

[<span data-ttu-id="2f53e-150">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="2f53e-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="2f53e-151">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="2f53e-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="2f53e-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2f53e-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2f53e-153">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2f53e-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="2f53e-154">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="2f53e-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="2f53e-155">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="2f53e-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="2f53e-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="2f53e-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

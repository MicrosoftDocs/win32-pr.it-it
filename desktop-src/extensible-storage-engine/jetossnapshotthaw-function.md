---
description: 'Altre informazioni su: funzione JetOSSnapshotThaw'
title: JetOSSnapshotThaw (funzione)
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885585"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="327a6-103">JetOSSnapshotThaw (funzione)</span><span class="sxs-lookup"><span data-stu-id="327a6-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="327a6-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="327a6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="327a6-105">JetOSSnapshotThaw (funzione)</span><span class="sxs-lookup"><span data-stu-id="327a6-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="327a6-106">La funzione **JetOSSnapshotThaw** notifica al motore che può riprendere le normali operazioni di i/o dopo un periodo di blocco e uno snapshot riuscito.</span><span class="sxs-lookup"><span data-stu-id="327a6-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="327a6-107">**Windows XP:**  **JetOSSnapshotThaw** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="327a6-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="327a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="327a6-108">Parameters</span></span>

<span data-ttu-id="327a6-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="327a6-109">*snapId*</span></span>

<span data-ttu-id="327a6-110">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="327a6-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="327a6-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="327a6-111">*grbit*</span></span>

<span data-ttu-id="327a6-112">Questo parametro è riservato per utilizzi futuri e l'unico valore valido supportato è 0.</span><span class="sxs-lookup"><span data-stu-id="327a6-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="327a6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="327a6-113">Return Value</span></span>

<span data-ttu-id="327a6-114">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="327a6-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="327a6-115">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="327a6-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="327a6-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="327a6-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="327a6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="327a6-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="327a6-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="327a6-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="327a6-119">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="327a6-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="327a6-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="327a6-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="327a6-121">La sessione dello snapshot non è valida o il parametro <em>grbit</em> non è valido.</span><span class="sxs-lookup"><span data-stu-id="327a6-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="327a6-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="327a6-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="327a6-123">Il timeout della sessione snapshot è stato interno prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="327a6-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="327a6-124">Di conseguenza, le operazioni di i/o restituite al normale prima che questa chiamata venisse eseguita.</span><span class="sxs-lookup"><span data-stu-id="327a6-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="327a6-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="327a6-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="327a6-126">Identificatore per la sessione snapshot non valido.</span><span class="sxs-lookup"><span data-stu-id="327a6-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="327a6-127">Se questa funzione ha esito positivo, termina una sessione snapshot e il normale comportamento del motore riprende.</span><span class="sxs-lookup"><span data-stu-id="327a6-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="327a6-128">Una nuova sessione snapshot può essere avviata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="327a6-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="327a6-129">Se questa funzione ha esito negativo, la sessione snapshot corrente termina ma il blocco di IOs durante il periodo di snapshot non è stato rispettato internamente.</span><span class="sxs-lookup"><span data-stu-id="327a6-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="327a6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="327a6-130">Remarks</span></span>

<span data-ttu-id="327a6-131">Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="327a6-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="327a6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="327a6-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="327a6-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="327a6-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="327a6-134">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="327a6-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="327a6-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="327a6-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="327a6-136">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="327a6-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="327a6-137"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="327a6-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="327a6-138">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="327a6-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="327a6-139"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="327a6-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="327a6-140">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="327a6-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="327a6-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="327a6-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="327a6-142">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="327a6-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="327a6-143">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="327a6-143">See Also</span></span>

[<span data-ttu-id="327a6-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="327a6-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="327a6-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="327a6-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="327a6-146">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="327a6-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="327a6-147">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="327a6-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="327a6-148">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="327a6-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)

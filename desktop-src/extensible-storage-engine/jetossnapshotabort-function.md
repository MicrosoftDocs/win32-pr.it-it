---
description: 'Altre informazioni su: funzione JetOSSnapshotAbort'
title: JetOSSnapshotAbort (funzione)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315618"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="91782-103">JetOSSnapshotAbort (funzione)</span><span class="sxs-lookup"><span data-stu-id="91782-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="91782-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="91782-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="91782-105">JetOSSnapshotAbort (funzione)</span><span class="sxs-lookup"><span data-stu-id="91782-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="91782-106">La funzione **JetOSSnapshotAbort** notifica al motore che può riprendere le normali operazioni di i/o dopo un periodo di blocco terminato con uno snapshot non riuscito.</span><span class="sxs-lookup"><span data-stu-id="91782-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="91782-107">**Windows server 2003:**  **JetOSSnapshotAbort** è stato introdotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="91782-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="91782-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="91782-108">Parameters</span></span>

<span data-ttu-id="91782-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="91782-109">*snapId*</span></span>

<span data-ttu-id="91782-110">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="91782-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="91782-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="91782-111">*grbit*</span></span>

<span data-ttu-id="91782-112">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="91782-112">The options for this call.</span></span> <span data-ttu-id="91782-113">Questo parametro è riservato per utilizzi futuri e l'unico valore valido supportato è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="91782-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="91782-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91782-114">Return Value</span></span>

<span data-ttu-id="91782-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="91782-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="91782-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="91782-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91782-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="91782-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="91782-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91782-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91782-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="91782-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="91782-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="91782-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91782-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="91782-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="91782-122">La sessione dello snapshot non è valida o il parametro grbit non è valido.</span><span class="sxs-lookup"><span data-stu-id="91782-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91782-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="91782-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="91782-124">Identificatore per la sessione snapshot non valido.</span><span class="sxs-lookup"><span data-stu-id="91782-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91782-125">Se questa funzione ha esito positivo, la sessione snapshot verrà terminata e verrà ripreso il normale comportamento del motore.</span><span class="sxs-lookup"><span data-stu-id="91782-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="91782-126">Una nuova sessione snapshot può essere avviata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="91782-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="91782-127">Se questa funzione ha esito negativo, la sessione snapshot non verrà interrotta.</span><span class="sxs-lookup"><span data-stu-id="91782-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="91782-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="91782-128">Remarks</span></span>

<span data-ttu-id="91782-129">Questa funzione deve essere chiamata invece di [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) per informare il motore che lo snapshot è stato interrotto per i motivi che non sono correlati al motore.</span><span class="sxs-lookup"><span data-stu-id="91782-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="91782-130">Queste informazioni possono essere usate in un secondo momento per consentire l'emissione di messaggi del registro eventi sulla sessione snapshot o per determinare altre azioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="91782-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="91782-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91782-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91782-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="91782-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="91782-133">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="91782-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91782-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="91782-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="91782-135">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="91782-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91782-136"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="91782-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="91782-137">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="91782-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91782-138"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="91782-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="91782-139">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="91782-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91782-140"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="91782-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="91782-141">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="91782-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="91782-142">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="91782-142">See Also</span></span>

[<span data-ttu-id="91782-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="91782-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="91782-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="91782-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="91782-145">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="91782-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="91782-146">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="91782-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="91782-147">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="91782-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)

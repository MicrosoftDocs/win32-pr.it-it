---
description: 'Altre informazioni su: JET_PFNSTATUS funzione di callback'
title: Funzione di callback JET_PFNSTATUS
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232561"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="dd540-103">Funzione di callback JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="dd540-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="dd540-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dd540-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="dd540-105">Funzione di callback JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="dd540-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="dd540-106">La funzione di callback **JET_PFNSTATUS** riceve informazioni sullo stato di avanzamento delle operazioni a esecuzione prolungata, ad esempio operazioni di deframmentazione, backup o ripristino.</span><span class="sxs-lookup"><span data-stu-id="dd540-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="dd540-107">Durante tali operazioni, il motore di database chiama questa funzione di callback per fornire un aggiornamento sullo stato di avanzamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd540-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="dd540-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd540-108">Parameters</span></span>

<span data-ttu-id="dd540-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dd540-109">*sesid*</span></span>

<span data-ttu-id="dd540-110">Sessione di tipo [JET_SESID](./jet-sesid.md) con la quale è stata chiamata la funzione a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="dd540-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="dd540-111">*SNP*</span><span class="sxs-lookup"><span data-stu-id="dd540-111">*snp*</span></span>

<span data-ttu-id="dd540-112">Tipo di operazione come specificato in [JET_SNP](./jet-snp.md).</span><span class="sxs-lookup"><span data-stu-id="dd540-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="dd540-113">I tipi di operazioni includono ripristino, compattazione, ripristino, backup, aggiornamento, scrub e aggiornamento del formato di record.</span><span class="sxs-lookup"><span data-stu-id="dd540-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="dd540-114">*SNT*</span><span class="sxs-lookup"><span data-stu-id="dd540-114">*snt*</span></span>

<span data-ttu-id="dd540-115">Stato di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd540-115">The status of an operation.</span></span> <span data-ttu-id="dd540-116">I tipi di stato includono inizio, in corso, completamento o errore.</span><span class="sxs-lookup"><span data-stu-id="dd540-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="dd540-117">Lo stato verrà specificato con il terzo parametro di tipo [JET_SNT](./jet-snt.md).</span><span class="sxs-lookup"><span data-stu-id="dd540-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="dd540-118">*PV*</span><span class="sxs-lookup"><span data-stu-id="dd540-118">*pv*</span></span>

<span data-ttu-id="dd540-119">Puntatore facoltativo a una struttura di tipo [JET_SNPROG](./jet-snprog-structure.md).</span><span class="sxs-lookup"><span data-stu-id="dd540-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="dd540-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd540-120">Return Value</span></span>

<span data-ttu-id="dd540-121">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei [codici di errore Extensible Storage Engine](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dd540-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="dd540-122">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="dd540-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="dd540-123">In seguito all'esito positivo, l'operazione che ha emesso il callback può procedere normalmente.</span><span class="sxs-lookup"><span data-stu-id="dd540-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="dd540-124">In alcuni casi, il callback potrebbe restituire un avviso che influenza l'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd540-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="dd540-125">In caso di errore, l'operazione che ha emesso il callback potrebbe procedere normalmente o potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="dd540-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="dd540-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd540-126">Remarks</span></span>

<span data-ttu-id="dd540-127">Questa funzione di callback verrà utilizzata in una notifica di stato in cui la struttura indicherà lo stato corrente dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="dd540-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="dd540-128">Si noti che la funzione di callback potrebbe essere chiamata più volte per lo stato di avanzamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd540-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="dd540-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd540-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd540-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dd540-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dd540-131">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dd540-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd540-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dd540-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dd540-133">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dd540-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd540-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="dd540-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dd540-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="dd540-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="dd540-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dd540-136">See Also</span></span>

[<span data-ttu-id="dd540-137">Codici di errore di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="dd540-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="dd540-138">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="dd540-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="dd540-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dd540-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dd540-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="dd540-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="dd540-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="dd540-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="dd540-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="dd540-142">JET_SNT</span></span>](./jet-snt.md)

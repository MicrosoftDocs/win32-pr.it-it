---
description: 'Altre informazioni su: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315634"
---
# <a name="jet_tableid"></a><span data-ttu-id="70296-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="70296-103">JET_TABLEID</span></span>


<span data-ttu-id="70296-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="70296-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="70296-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="70296-105">JET_TABLEID</span></span>

<span data-ttu-id="70296-106">Il tipo di dati JET_TABLEID contiene un handle per il cursore del database da usare per una chiamata all'API JET.</span><span class="sxs-lookup"><span data-stu-id="70296-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="70296-107">Un cursore può essere utilizzato solo con la sessione utilizzata per aprire il cursore.</span><span class="sxs-lookup"><span data-stu-id="70296-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="70296-108">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="70296-108">Data Types</span></span>

<span data-ttu-id="70296-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="70296-109">JET_TABLEID</span></span>

<span data-ttu-id="70296-110">È possibile utilizzare **null** o [JET_tableidNil](./invalid-handle-constants.md) per indicare un handle di cursore non valido.</span><span class="sxs-lookup"><span data-stu-id="70296-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="70296-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="70296-111">Remarks</span></span>

<span data-ttu-id="70296-112">Un cursore gestisce l'utilizzo di una tabella per il motore di database.</span><span class="sxs-lookup"><span data-stu-id="70296-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="70296-113">Un cursore può eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="70296-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="70296-114">Analizza record</span><span class="sxs-lookup"><span data-stu-id="70296-114">Scan records</span></span>

  - <span data-ttu-id="70296-115">Cercare i record</span><span class="sxs-lookup"><span data-stu-id="70296-115">Search for records</span></span>

  - <span data-ttu-id="70296-116">Scegliere il tipo di ordinamento e la visibilità effettivi dei record</span><span class="sxs-lookup"><span data-stu-id="70296-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="70296-117">Creare, aggiornare o eliminare record</span><span class="sxs-lookup"><span data-stu-id="70296-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="70296-118">Modificare lo schema della tabella</span><span class="sxs-lookup"><span data-stu-id="70296-118">Modify the schema of the table</span></span>

<span data-ttu-id="70296-119">La funzionalità supportata del cursore può variare in base alla modifica dello stato o del tipo della tabella sottostante.</span><span class="sxs-lookup"><span data-stu-id="70296-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="70296-120">Ad esempio, una tabella temporanea potrebbe impedire la ricerca di dati quando viene aperta con determinate opzioni.</span><span class="sxs-lookup"><span data-stu-id="70296-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="70296-121">Il cursore è sempre completamente connesso alla tabella sottostante e interagisce direttamente con tali dati senza alcuna memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="70296-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="70296-122">Quasi tutte le funzionalità di base di ISAM esposte da questo motore di database vengono elaborate tramite il cursore.</span><span class="sxs-lookup"><span data-stu-id="70296-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="70296-123">È possibile creare un cursore utilizzando [JetOpenTable](./jetopentable-function.md) o [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="70296-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="70296-124">È possibile duplicare un cursore utilizzando [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="70296-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="70296-125">Un cursore può essere chiuso in modo esplicito tramite [JetCloseTable](./jetclosetable-function.md) o chiuso in modo implicito tramite [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="70296-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="70296-126">Un cursore può essere anche chiuso in modo implicito da [JetRollback](./jetrollback-function.md) se è stato aperto nella transazione interrotta.</span><span class="sxs-lookup"><span data-stu-id="70296-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="70296-127">Il numero massimo di cursori che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxCursors](./resource-parameters.md), che può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="70296-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="70296-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70296-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70296-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="70296-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="70296-130">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="70296-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70296-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="70296-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70296-132">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="70296-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70296-133"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="70296-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="70296-134">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="70296-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="70296-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="70296-135">See Also</span></span>

[<span data-ttu-id="70296-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="70296-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="70296-137">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="70296-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="70296-138">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="70296-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="70296-139">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="70296-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="70296-140">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="70296-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="70296-141">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="70296-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="70296-142">JetRollback</span><span class="sxs-lookup"><span data-stu-id="70296-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="70296-143">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="70296-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="70296-144">JetTerm</span><span class="sxs-lookup"><span data-stu-id="70296-144">JetTerm</span></span>](./jetterm-function.md)

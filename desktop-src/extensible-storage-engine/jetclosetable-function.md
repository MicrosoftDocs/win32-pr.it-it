---
description: 'Altre informazioni su: funzione JetCloseTable'
title: JetCloseTable (funzione)
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531099"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="82701-103">JetCloseTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="82701-103">JetCloseTable Function</span></span>


<span data-ttu-id="82701-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="82701-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="82701-105">JetCloseTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="82701-105">JetCloseTable Function</span></span>

<span data-ttu-id="82701-106">La funzione **JetCloseTable** chiude una tabella aperta in un database.</span><span class="sxs-lookup"><span data-stu-id="82701-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="82701-107">La tabella può essere una tabella temporanea o una tabella normale.</span><span class="sxs-lookup"><span data-stu-id="82701-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="82701-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="82701-108">Parameters</span></span>

<span data-ttu-id="82701-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="82701-109">*sesid*</span></span>

<span data-ttu-id="82701-110">Identifica il contesto della sessione di database che verrà usato per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="82701-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="82701-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="82701-111">*tableid*</span></span>

<span data-ttu-id="82701-112">Identifica la tabella da chiudere.</span><span class="sxs-lookup"><span data-stu-id="82701-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="82701-113">Impostare *TableID* su JET_tableidNil per rilasciare la memoria.</span><span class="sxs-lookup"><span data-stu-id="82701-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="82701-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82701-114">Return Value</span></span>

<span data-ttu-id="82701-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="82701-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="82701-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="82701-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82701-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="82701-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="82701-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82701-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82701-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="82701-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="82701-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="82701-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="82701-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="82701-121">Remarks</span></span>

<span data-ttu-id="82701-122">Questa funzione deve essere chiamata su tutte le tabelle aperte con [JetOpenTable](./jetopentable-function.md).</span><span class="sxs-lookup"><span data-stu-id="82701-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="82701-123">L'eccezione a questa regola si verifica quando [JetOpenTable](./jetopentable-function.md) viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="82701-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="82701-124">Quando si esegue il rollback di una transazione, la tabella viene chiusa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="82701-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="82701-125">In questo caso, è un errore chiudere la tabella con **JetCloseTable**.</span><span class="sxs-lookup"><span data-stu-id="82701-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="82701-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82701-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82701-127"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="82701-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="82701-128">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="82701-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82701-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="82701-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="82701-130">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="82701-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82701-131"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="82701-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="82701-132">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="82701-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82701-133"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="82701-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="82701-134">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="82701-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82701-135"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="82701-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="82701-136">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="82701-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="82701-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="82701-137">See Also</span></span>

[<span data-ttu-id="82701-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="82701-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="82701-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="82701-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="82701-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="82701-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="82701-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="82701-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="82701-142">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="82701-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="82701-143">JetRollback</span><span class="sxs-lookup"><span data-stu-id="82701-143">JetRollback</span></span>](./jetrollback-function.md)

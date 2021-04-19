---
description: 'Altre informazioni su: funzione JetDeleteTable'
title: JetDeleteTable (funzione)
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319641"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="ffd15-103">JetDeleteTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="ffd15-103">JetDeleteTable Function</span></span>


<span data-ttu-id="ffd15-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ffd15-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="ffd15-105">JetDeleteTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="ffd15-105">JetDeleteTable Function</span></span>

<span data-ttu-id="ffd15-106">La funzione **JetDeleteTable** Elimina una tabella in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="ffd15-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="ffd15-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffd15-107">Parameters</span></span>

<span data-ttu-id="ffd15-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ffd15-108">*sesid*</span></span>

<span data-ttu-id="ffd15-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="ffd15-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="ffd15-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="ffd15-110">*dbid*</span></span>

<span data-ttu-id="ffd15-111">Identificatore del database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="ffd15-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="ffd15-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="ffd15-112">*szTableName*</span></span>

<span data-ttu-id="ffd15-113">Nome della tabella da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ffd15-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="ffd15-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffd15-114">Return Value</span></span>

<span data-ttu-id="ffd15-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ffd15-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ffd15-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd15-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ffd15-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ffd15-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="ffd15-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffd15-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffd15-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ffd15-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ffd15-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ffd15-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffd15-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="ffd15-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="ffd15-122">È stato effettuato un tentativo di eliminare una tabella mentre un'altra sessione dispone di un ID di tabella aperto (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) con <a href="gg294118(v=exchg.10).md">JetOpenTable</a> o <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span><span class="sxs-lookup"><span data-stu-id="ffd15-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffd15-123">Tabella JET_errCannotDeletetemporary</span><span class="sxs-lookup"><span data-stu-id="ffd15-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="ffd15-124">È stato effettuato un tentativo di eliminare una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="ffd15-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="ffd15-125">Una tabella temporanea viene eliminata automaticamente quando viene chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="ffd15-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffd15-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="ffd15-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="ffd15-127">È stato effettuato un tentativo di eliminare una tabella modello, ovvero una tabella da cui è possibile ereditare DDL.</span><span class="sxs-lookup"><span data-stu-id="ffd15-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="ffd15-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffd15-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffd15-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ffd15-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ffd15-130">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ffd15-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffd15-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ffd15-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ffd15-132">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ffd15-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffd15-133"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ffd15-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ffd15-134">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ffd15-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffd15-135"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ffd15-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ffd15-136">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ffd15-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffd15-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ffd15-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ffd15-138">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ffd15-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffd15-139"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ffd15-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ffd15-140">Implementato come <strong>JetDeleteTableW</strong> (Unicode) e <strong>JetDeleteTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ffd15-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ffd15-141">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ffd15-141">See Also</span></span>

[<span data-ttu-id="ffd15-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ffd15-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ffd15-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ffd15-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ffd15-144">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="ffd15-144">JetCloseTable</span></span>](./jetclosetable-function.md)

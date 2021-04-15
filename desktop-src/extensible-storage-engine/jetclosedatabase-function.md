---
description: 'Altre informazioni su: funzione JetCloseDatabase'
title: JetCloseDatabase (funzione)
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524972"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="56a7d-103">JetCloseDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="56a7d-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="56a7d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56a7d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="56a7d-105">JetCloseDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="56a7d-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="56a7d-106">La funzione **JetCloseDatabase** chiude un file di database precedentemente aperto con [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="56a7d-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="56a7d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="56a7d-107">Parameters</span></span>

<span data-ttu-id="56a7d-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="56a7d-108">*sesid*</span></span>

<span data-ttu-id="56a7d-109">Contesto della sessione del database che verrà usato per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="56a7d-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="56a7d-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="56a7d-110">*dbid*</span></span>

<span data-ttu-id="56a7d-111">Database da chiudere.</span><span class="sxs-lookup"><span data-stu-id="56a7d-111">The database to be closed.</span></span>

<span data-ttu-id="56a7d-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="56a7d-112">*grbit*</span></span>

<span data-ttu-id="56a7d-113">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="56a7d-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="56a7d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56a7d-114">Return Value</span></span>

<span data-ttu-id="56a7d-115">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="56a7d-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56a7d-116">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="56a7d-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56a7d-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="56a7d-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="56a7d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a7d-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56a7d-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="56a7d-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="56a7d-120">Il database non è stato aperto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="56a7d-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a7d-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="56a7d-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="56a7d-122">Il parametro <em>dbid</em> non è un identificatore di database valido.</span><span class="sxs-lookup"><span data-stu-id="56a7d-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a7d-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56a7d-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56a7d-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="56a7d-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="56a7d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56a7d-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56a7d-126"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="56a7d-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56a7d-127">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="56a7d-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a7d-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="56a7d-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56a7d-129">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="56a7d-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a7d-130"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="56a7d-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56a7d-131">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="56a7d-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56a7d-132"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="56a7d-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56a7d-133">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="56a7d-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56a7d-134"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="56a7d-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56a7d-135">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="56a7d-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56a7d-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="56a7d-136">See Also</span></span>

[<span data-ttu-id="56a7d-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56a7d-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56a7d-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="56a7d-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="56a7d-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="56a7d-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="56a7d-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="56a7d-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="56a7d-141">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="56a7d-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="56a7d-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="56a7d-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="56a7d-143">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="56a7d-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)

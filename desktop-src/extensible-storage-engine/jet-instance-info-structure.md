---
description: 'Altre informazioni su: struttura JET_INSTANCE_INFO'
title: Struttura JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885025"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="ce956-103">Struttura JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ce956-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="ce956-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ce956-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="ce956-105">Struttura JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ce956-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="ce956-106">La struttura **JET_INSTANCE_INFO** riceve informazioni sulle istanze di database in esecuzione quando vengono utilizzate con le funzioni [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) e [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ce956-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="ce956-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ce956-107">Members</span></span>

<span data-ttu-id="ce956-108">**hInstanceId**</span><span class="sxs-lookup"><span data-stu-id="ce956-108">**hInstanceId**</span></span>

<span data-ttu-id="ce956-109">[JET_INSTANCE](./jet-instance.md) dell'istanza di specificata.</span><span class="sxs-lookup"><span data-stu-id="ce956-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="ce956-110">**szInstanceName**</span><span class="sxs-lookup"><span data-stu-id="ce956-110">**szInstanceName**</span></span>

<span data-ttu-id="ce956-111">Il nome dell'istanza di database.</span><span class="sxs-lookup"><span data-stu-id="ce956-111">The name of the database instance.</span></span> <span data-ttu-id="ce956-112">Questo valore può essere **null** se l'istanza non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="ce956-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="ce956-113">**cDatabases**</span><span class="sxs-lookup"><span data-stu-id="ce956-113">**cDatabases**</span></span>

<span data-ttu-id="ce956-114">Numero di database collegati all'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="ce956-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="ce956-115">**cDatabases** include inoltre la dimensione delle matrici di stringhe restituite in **szDatabaseFileName**, **szDatabaseDisplayName** e **szDatabaseSLVFileName**.</span><span class="sxs-lookup"><span data-stu-id="ce956-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="ce956-116">**szDatabaseFileName**</span><span class="sxs-lookup"><span data-stu-id="ce956-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="ce956-117">Matrice di stringhe, ognuna delle quali contiene il nome file di un database associato all'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="ce956-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="ce956-118">La matrice contiene elementi **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="ce956-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="ce956-119">**szDatabaseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ce956-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="ce956-120">Matrice di stringhe, ognuna delle quali contiene il nome visualizzato di un database.</span><span class="sxs-lookup"><span data-stu-id="ce956-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="ce956-121">Attualmente la stringa può essere NULL.</span><span class="sxs-lookup"><span data-stu-id="ce956-121">Currently the string can be NULL.</span></span> <span data-ttu-id="ce956-122">La matrice contiene elementi **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="ce956-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="ce956-123">**szDatabaseSLVFileName**</span><span class="sxs-lookup"><span data-stu-id="ce956-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="ce956-124">Matrice di stringhe, ognuna delle quali contiene il nome file del file SLV collegato all'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="ce956-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="ce956-125">La matrice contiene elementi **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="ce956-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="ce956-126">I file SLV non sono supportati, pertanto questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ce956-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="ce956-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce956-127">Remarks</span></span>

<span data-ttu-id="ce956-128">A ogni istanza di database possono essere collegati diversi database.</span><span class="sxs-lookup"><span data-stu-id="ce956-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="ce956-129">Per una determinata struttura di **JET_INSTANCE_INFO** , la matrice di stringhe restituita per i database si trova nello stesso ordine.</span><span class="sxs-lookup"><span data-stu-id="ce956-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="ce956-130">Ad esempio, "szDatabaseDisplayName \[ i \] " e "szDatabaseFileName \[ i \] " si riferiscono entrambi allo stesso database.</span><span class="sxs-lookup"><span data-stu-id="ce956-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="ce956-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce956-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce956-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ce956-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ce956-133">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ce956-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce956-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ce956-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ce956-135">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ce956-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce956-136"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ce956-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ce956-137">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ce956-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce956-138"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ce956-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ce956-139">Implementato come <strong>JET_INSTANCE_INFO_W</strong> (Unicode) e <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ce956-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ce956-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ce956-140">See Also</span></span>

[<span data-ttu-id="ce956-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="ce956-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="ce956-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ce956-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ce956-143">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="ce956-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="ce956-144">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="ce956-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)

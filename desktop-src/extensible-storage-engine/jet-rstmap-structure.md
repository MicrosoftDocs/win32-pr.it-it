---
description: 'Altre informazioni su: struttura JET_RSTMAP'
title: Struttura JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750554"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="ef102-103">Struttura JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="ef102-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="ef102-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef102-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="ef102-105">Struttura JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="ef102-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="ef102-106">La struttura di **JET_RSTMAP** consente di rimappare i percorsi dei file di database archiviati nei log delle transazioni durante il ripristino, se utilizzati dalle funzioni [JetInit](./jetinit-function.md) e [JetExternalRestore](./jetexternalrestore-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ef102-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="ef102-107">Ciò consente lo spostamento dei database in modalità offline o quando vengono ripristinati dal backup.</span><span class="sxs-lookup"><span data-stu-id="ef102-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="ef102-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ef102-108">Members</span></span>

<span data-ttu-id="ef102-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="ef102-109">**szDatabaseName**</span></span>

<span data-ttu-id="ef102-110">Percorso assoluto corrente di un database associato ai log delle transazioni riprodotti durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="ef102-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="ef102-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="ef102-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="ef102-112">Nuovo percorso assoluto per il database.</span><span class="sxs-lookup"><span data-stu-id="ef102-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="ef102-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef102-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef102-114"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ef102-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef102-115">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ef102-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef102-116"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef102-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef102-117">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ef102-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef102-118"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ef102-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef102-119">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ef102-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef102-120"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ef102-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ef102-121">Implementato come <strong>JET_RSTMAP_W</strong> (Unicode) e <strong>JET_RSTMAP_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ef102-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ef102-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ef102-122">See Also</span></span>

[<span data-ttu-id="ef102-123">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="ef102-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="ef102-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="ef102-124">JetInit</span></span>](./jetinit-function.md)

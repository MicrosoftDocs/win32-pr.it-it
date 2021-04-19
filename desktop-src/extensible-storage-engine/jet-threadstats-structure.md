---
description: 'Altre informazioni su: struttura JET_THREADSTATS'
title: Struttura JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316471"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="d75fe-103">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="d75fe-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="d75fe-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d75fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="d75fe-105">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="d75fe-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="d75fe-106">La struttura **JET_THREADSTATS** contiene statistiche cumulative sul lavoro eseguito dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="d75fe-107">Queste informazioni vengono restituite tramite [JetGetThreadStats](./jetgetthreadstats-function.md).</span><span class="sxs-lookup"><span data-stu-id="d75fe-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="d75fe-108">**Windows Vista:**  La struttura **JET_THREADSTATS** è stata introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d75fe-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="d75fe-109">Membri</span><span class="sxs-lookup"><span data-stu-id="d75fe-109">Members</span></span>

<span data-ttu-id="d75fe-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d75fe-110">**cbStruct**</span></span>

<span data-ttu-id="d75fe-111">Dimensioni in byte della struttura **JET_THREADSTATS** restituita.</span><span class="sxs-lookup"><span data-stu-id="d75fe-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="d75fe-112">**Nota**  La struttura di **JET_THREADSTATS** si espanderà in futuro per contenere più statistiche.</span><span class="sxs-lookup"><span data-stu-id="d75fe-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="d75fe-113">Le nuove statistiche verranno aggiunte alla fine della struttura e potranno essere recuperate con una dimensione del buffer di output maggiore.</span><span class="sxs-lookup"><span data-stu-id="d75fe-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="d75fe-114">La presenza di statistiche aggiuntive può essere dedotta da un valore **cbStruct** più grande.</span><span class="sxs-lookup"><span data-stu-id="d75fe-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="d75fe-115">**cPageReferenced**</span><span class="sxs-lookup"><span data-stu-id="d75fe-115">**cPageReferenced**</span></span>

<span data-ttu-id="d75fe-116">Numero totale di pagine di database visitate dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="d75fe-117">**cPageRead**</span><span class="sxs-lookup"><span data-stu-id="d75fe-117">**cPageRead**</span></span>

<span data-ttu-id="d75fe-118">Numero totale di pagine del database recuperate dal disco dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="d75fe-119">**cPagePreread**</span><span class="sxs-lookup"><span data-stu-id="d75fe-119">**cPagePreread**</span></span>

<span data-ttu-id="d75fe-120">Numero totale di pagine di database prelette dal disco dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="d75fe-121">**cPageDirtied**</span><span class="sxs-lookup"><span data-stu-id="d75fe-121">**cPageDirtied**</span></span>

<span data-ttu-id="d75fe-122">Numero totale di pagine di database, senza modifiche non scritte, modificate dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="d75fe-123">**cPageRedirtied**</span><span class="sxs-lookup"><span data-stu-id="d75fe-123">**cPageRedirtied**</span></span>

<span data-ttu-id="d75fe-124">Numero totale di pagine di database, con modifiche non scritte, modificate dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="d75fe-125">**cLogRecord**</span><span class="sxs-lookup"><span data-stu-id="d75fe-125">**cLogRecord**</span></span>

<span data-ttu-id="d75fe-126">Numero totale di record del log delle transazioni generati dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="d75fe-127">**cbLogRecord**</span><span class="sxs-lookup"><span data-stu-id="d75fe-127">**cbLogRecord**</span></span>

<span data-ttu-id="d75fe-128">Dimensioni totali in byte dei record del log delle transazioni generati dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="d75fe-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="d75fe-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d75fe-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d75fe-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d75fe-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d75fe-131">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d75fe-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d75fe-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d75fe-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d75fe-133">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d75fe-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d75fe-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="d75fe-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d75fe-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="d75fe-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d75fe-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d75fe-136">See Also</span></span>

[<span data-ttu-id="d75fe-137">JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="d75fe-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)

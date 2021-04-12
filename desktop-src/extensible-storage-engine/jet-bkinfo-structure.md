---
description: 'Altre informazioni su: struttura JET_BKINFO'
title: Struttura JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233374"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="cff96-103">Struttura JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="cff96-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="cff96-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cff96-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="cff96-105">Struttura JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="cff96-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="cff96-106">La struttura **JET_BKINFO** include una raccolta di dati relativi a un evento di backup specifico.</span><span class="sxs-lookup"><span data-stu-id="cff96-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="cff96-107">Membri</span><span class="sxs-lookup"><span data-stu-id="cff96-107">Members</span></span>

<span data-ttu-id="cff96-108">**lgposMark**</span><span class="sxs-lookup"><span data-stu-id="cff96-108">**lgposMark**</span></span>

<span data-ttu-id="cff96-109">ID di questo backup.</span><span class="sxs-lookup"><span data-stu-id="cff96-109">The ID of this backup.</span></span>

<span data-ttu-id="cff96-110">**logtimeMark**</span><span class="sxs-lookup"><span data-stu-id="cff96-110">**logtimeMark**</span></span>

<span data-ttu-id="cff96-111">Ora di questo evento di backup.</span><span class="sxs-lookup"><span data-stu-id="cff96-111">The time of this backup event.</span></span>

<span data-ttu-id="cff96-112">**bklogtimeMark**</span><span class="sxs-lookup"><span data-stu-id="cff96-112">**bklogtimeMark**</span></span>

<span data-ttu-id="cff96-113">Ora di questo evento di backup, con ulteriori bit per indicare un backup di snapshot.</span><span class="sxs-lookup"><span data-stu-id="cff96-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="cff96-114">**Windows Vista: bklogtimeMark** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cff96-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="cff96-115">**genLow**</span><span class="sxs-lookup"><span data-stu-id="cff96-115">**genLow**</span></span>

<span data-ttu-id="cff96-116">Numero di generazione del log basso associato a questo evento di backup.</span><span class="sxs-lookup"><span data-stu-id="cff96-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="cff96-117">**genHigh**</span><span class="sxs-lookup"><span data-stu-id="cff96-117">**genHigh**</span></span>

<span data-ttu-id="cff96-118">Numero di generazione del log elevato associato a questo evento di backup.</span><span class="sxs-lookup"><span data-stu-id="cff96-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="cff96-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cff96-119">Remarks</span></span>

<span data-ttu-id="cff96-120">Questa struttura viene utilizzata all'interno della struttura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) per rappresentare i dati relativi all'evento di backup del database.</span><span class="sxs-lookup"><span data-stu-id="cff96-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="cff96-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cff96-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cff96-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cff96-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cff96-123">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cff96-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cff96-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cff96-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cff96-125">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cff96-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cff96-126"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="cff96-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cff96-127">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="cff96-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cff96-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cff96-128">See Also</span></span>

[<span data-ttu-id="cff96-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="cff96-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="cff96-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="cff96-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="cff96-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="cff96-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="cff96-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="cff96-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)

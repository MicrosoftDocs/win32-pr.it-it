---
description: 'Altre informazioni su: struttura JET_LGPOS'
title: Struttura JET_LGPOS
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: 25f00c73a4bb922a8152335babe222b539c70ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057937"
---
# <a name="jet_lgpos-structure"></a><span data-ttu-id="e1811-103">Struttura JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="e1811-103">JET_LGPOS Structure</span></span>


<span data-ttu-id="e1811-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e1811-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_lgpos-structure"></a><span data-ttu-id="e1811-105">Struttura JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="e1811-105">JET_LGPOS Structure</span></span>

<span data-ttu-id="e1811-106">La struttura **JET_LGPOS** include i dati interni al meccanismo di registrazione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="e1811-106">The **JET_LGPOS** structure holds data that is internal to the logging mechanism of the database engine.</span></span> <span data-ttu-id="e1811-107">Questa struttura è considerata interna.</span><span class="sxs-lookup"><span data-stu-id="e1811-107">This structure is considered internal.</span></span>

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a><span data-ttu-id="e1811-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e1811-108">Members</span></span>

<span data-ttu-id="e1811-109">**IB**</span><span class="sxs-lookup"><span data-stu-id="e1811-109">**ib**</span></span>

<span data-ttu-id="e1811-110">Supporta l'infrastruttura ESE e non può essere utilizzata dal codice.</span><span class="sxs-lookup"><span data-stu-id="e1811-110">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="e1811-111">**ISEC**</span><span class="sxs-lookup"><span data-stu-id="e1811-111">**isec**</span></span>

<span data-ttu-id="e1811-112">Supporta l'infrastruttura ESE e non può essere utilizzata dal codice.</span><span class="sxs-lookup"><span data-stu-id="e1811-112">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="e1811-113">**lGeneration**</span><span class="sxs-lookup"><span data-stu-id="e1811-113">**lGeneration**</span></span>

<span data-ttu-id="e1811-114">Supporta l'infrastruttura ESE e non può essere utilizzata dal codice.</span><span class="sxs-lookup"><span data-stu-id="e1811-114">Supports the ESE infrastructure and cannot be used from your code.</span></span>

### <a name="requirements"></a><span data-ttu-id="e1811-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1811-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1811-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e1811-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e1811-117">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e1811-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1811-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e1811-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e1811-119">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e1811-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1811-120"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e1811-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e1811-121">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e1811-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e1811-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e1811-122">See Also</span></span>

[<span data-ttu-id="e1811-123">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="e1811-123">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="e1811-124">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="e1811-124">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)

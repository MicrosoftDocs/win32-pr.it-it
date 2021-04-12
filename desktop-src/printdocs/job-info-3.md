---
description: La \_ struttura info processo \_ 3 viene utilizzata per collegare insieme un set di processi di stampa.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Struttura JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233722"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="639a7-103">\_Struttura info processo \_ 3</span><span class="sxs-lookup"><span data-stu-id="639a7-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="639a7-104">La **struttura \_ info processo \_ 3** viene utilizzata per collegare insieme un set di processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="639a7-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="639a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="639a7-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="639a7-106">Members</span><span class="sxs-lookup"><span data-stu-id="639a7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="639a7-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="639a7-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="639a7-108">Identificatore del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="639a7-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="639a7-109">**NextJobId**</span><span class="sxs-lookup"><span data-stu-id="639a7-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="639a7-110">Identificatore del processo di stampa per il processo di stampa successivo nel set collegato di processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="639a7-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="639a7-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="639a7-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="639a7-112">Questo valore è riservato per l'uso futuro.</span><span class="sxs-lookup"><span data-stu-id="639a7-112">This value is reserved for future use.</span></span> <span data-ttu-id="639a7-113">È necessario impostarlo su zero.</span><span class="sxs-lookup"><span data-stu-id="639a7-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="639a7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="639a7-114">Requirements</span></span>



| <span data-ttu-id="639a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="639a7-115">Requirement</span></span> | <span data-ttu-id="639a7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="639a7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="639a7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="639a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="639a7-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="639a7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="639a7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="639a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="639a7-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="639a7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="639a7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="639a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="639a7-122"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="639a7-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="639a7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="639a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639a7-124">Stampa</span><span class="sxs-lookup"><span data-stu-id="639a7-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="639a7-125">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="639a7-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="639a7-126">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="639a7-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="639a7-127">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="639a7-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="639a7-128">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="639a7-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 





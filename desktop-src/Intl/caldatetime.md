---
description: Deprecato. Rappresenta un istante di tempo, in genere espresso come data e ora del giorno e un calendario corrispondente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Struttura CALDATETIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319986"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="56d63-104">Struttura CALDATETIME</span><span class="sxs-lookup"><span data-stu-id="56d63-104">CALDATETIME structure</span></span>

<span data-ttu-id="56d63-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="56d63-105">Deprecated.</span></span> <span data-ttu-id="56d63-106">Rappresenta un istante di tempo, in genere espresso come data e ora del giorno e un calendario corrispondente.</span><span class="sxs-lookup"><span data-stu-id="56d63-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d63-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56d63-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="56d63-108">Members</span><span class="sxs-lookup"><span data-stu-id="56d63-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="56d63-109">**CalId**</span><span class="sxs-lookup"><span data-stu-id="56d63-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-110">[Identificatore del calendario](calendar-identifiers.md) per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-111">**Era**</span><span class="sxs-lookup"><span data-stu-id="56d63-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-112">Informazioni sull'era per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-113">**Anno**</span><span class="sxs-lookup"><span data-stu-id="56d63-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-114">Anno per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-115">**Mese**</span><span class="sxs-lookup"><span data-stu-id="56d63-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-116">Mese per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-117">**Day**</span><span class="sxs-lookup"><span data-stu-id="56d63-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-118">Giorno per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="56d63-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-120">Il giorno della settimana per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-121">**Ora**</span><span class="sxs-lookup"><span data-stu-id="56d63-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-122">Ora dell'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-123">**Minuto**</span><span class="sxs-lookup"><span data-stu-id="56d63-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-124">Minuto per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-125">**Secondo**</span><span class="sxs-lookup"><span data-stu-id="56d63-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-126">Secondo oggetto per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="56d63-127">**Tick**</span><span class="sxs-lookup"><span data-stu-id="56d63-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="56d63-128">Segno di selezione per l'istante di tempo.</span><span class="sxs-lookup"><span data-stu-id="56d63-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56d63-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56d63-129">Requirements</span></span>



| <span data-ttu-id="56d63-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="56d63-130">Requirement</span></span> | <span data-ttu-id="56d63-131">Valore</span><span class="sxs-lookup"><span data-stu-id="56d63-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56d63-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56d63-132">Minimum supported client</span></span><br/> | <span data-ttu-id="56d63-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56d63-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56d63-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56d63-134">Minimum supported server</span></span><br/> | <span data-ttu-id="56d63-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56d63-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56d63-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56d63-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d63-137">Strutture di supporto della lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="56d63-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 





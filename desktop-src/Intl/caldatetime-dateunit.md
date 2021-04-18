---
description: Deprecato. Specifica le unità di data per modificare la struttura CALDATETIME.
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: Enumerazione CALDATETIME_DATEUNIT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306618"
---
# <a name="caldatetime_dateunit-enumeration"></a><span data-ttu-id="d5b6a-104">\_Enumerazione CALDATETIME DATEUNIT</span><span class="sxs-lookup"><span data-stu-id="d5b6a-104">CALDATETIME\_DATEUNIT enumeration</span></span>

<span data-ttu-id="d5b6a-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-105">Deprecated.</span></span> <span data-ttu-id="d5b6a-106">Specifica le unità di data per modificare la struttura [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="d5b6a-106">Specifies the date units for adjusting the [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b6a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5b6a-107">Syntax</span></span>


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a><span data-ttu-id="d5b6a-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="d5b6a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d5b6a-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-110">Unità di data e ora dell'era.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-110">The era date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-112">Unità di data e ora dell'anno.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-112">The year date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-114">Unità di data/ora del mese.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-114">The month date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-116">Unità di data/ora della settimana.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-116">The week date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-118">Unità di data/ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-118">The day date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-120">Unità di data e ora.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-120">The hour date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-122">Unità di data/ora di minuti.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-122">The minute date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-124">Seconda unità di data/ora.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-124">The second date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d5b6a-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span><span class="sxs-lookup"><span data-stu-id="d5b6a-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d5b6a-126">Unità di data e ora del segno di selezione.</span><span class="sxs-lookup"><span data-stu-id="d5b6a-126">The tick date time unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5b6a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5b6a-127">Requirements</span></span>



| <span data-ttu-id="d5b6a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5b6a-128">Requirement</span></span> | <span data-ttu-id="d5b6a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d5b6a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5b6a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5b6a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b6a-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5b6a-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5b6a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5b6a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b6a-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5b6a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5b6a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5b6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b6a-135">Tipi di enumerazione del supporto linguistico nazionale</span><span class="sxs-lookup"><span data-stu-id="d5b6a-135">National Language Support Enumeration Types</span></span>](national-language-support-enumeration-types.md)
</dt> </dl>

 

 





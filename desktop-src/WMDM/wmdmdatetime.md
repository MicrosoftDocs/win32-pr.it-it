---
title: Struttura WMDMDATETIME
description: La struttura WMDMDATETIME contiene una data e un'ora del giorno.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Struttura WMDMDATETIME Windows Media Gestione dispositivi
- Puntatore alla struttura PWMDMDATETIME Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324403"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="d86a9-105">Struttura WMDMDATETIME</span><span class="sxs-lookup"><span data-stu-id="d86a9-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="d86a9-106">La struttura **WMDMDATETIME** contiene una data e un'ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="d86a9-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d86a9-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="d86a9-108">Members</span><span class="sxs-lookup"><span data-stu-id="d86a9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d86a9-109">**wYear**</span><span class="sxs-lookup"><span data-stu-id="d86a9-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="d86a9-110">Parola contenente l'anno a quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="d86a9-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="d86a9-111">**wMonth**</span><span class="sxs-lookup"><span data-stu-id="d86a9-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="d86a9-112">Parola contenente il mese (1-12).</span><span class="sxs-lookup"><span data-stu-id="d86a9-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="d86a9-113">**wDay**</span><span class="sxs-lookup"><span data-stu-id="d86a9-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="d86a9-114">Parola contenente il giorno del mese (1-31).</span><span class="sxs-lookup"><span data-stu-id="d86a9-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="d86a9-115">**wHour**</span><span class="sxs-lookup"><span data-stu-id="d86a9-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="d86a9-116">Parola contenente l'ora (0-23).</span><span class="sxs-lookup"><span data-stu-id="d86a9-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="d86a9-117">**wMinute**</span><span class="sxs-lookup"><span data-stu-id="d86a9-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="d86a9-118">Parola contenente il minuto (0-59).</span><span class="sxs-lookup"><span data-stu-id="d86a9-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="d86a9-119">**wSecond**</span><span class="sxs-lookup"><span data-stu-id="d86a9-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="d86a9-120">Parola contenente il secondo (0-59).</span><span class="sxs-lookup"><span data-stu-id="d86a9-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d86a9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d86a9-121">Requirements</span></span>



| <span data-ttu-id="d86a9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86a9-122">Requirement</span></span> | <span data-ttu-id="d86a9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d86a9-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d86a9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d86a9-124">Header</span></span><br/> | <dl> <span data-ttu-id="d86a9-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d86a9-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86a9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d86a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86a9-127">**IMDSPStorage:: GETDATE**</span><span class="sxs-lookup"><span data-stu-id="d86a9-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="d86a9-128">**IWMDMStorage:: GETDATE**</span><span class="sxs-lookup"><span data-stu-id="d86a9-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="d86a9-129">**WMDMRIGHTS**</span><span class="sxs-lookup"><span data-stu-id="d86a9-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="d86a9-130">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="d86a9-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 






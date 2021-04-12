---
description: Contiene informazioni su un processore.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Struttura PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345486"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="1293b-103">\_ \_ Struttura delle informazioni sul risparmio di energia del processore</span><span class="sxs-lookup"><span data-stu-id="1293b-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="1293b-104">Contiene informazioni su un processore.</span><span class="sxs-lookup"><span data-stu-id="1293b-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1293b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1293b-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="1293b-106">Members</span><span class="sxs-lookup"><span data-stu-id="1293b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1293b-107">**Number**</span><span class="sxs-lookup"><span data-stu-id="1293b-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="1293b-108">Numero di processori del sistema.</span><span class="sxs-lookup"><span data-stu-id="1293b-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="1293b-109">**MaxMhz**</span><span class="sxs-lookup"><span data-stu-id="1293b-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="1293b-110">Frequenza di clock massima specificata del processore di sistema, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="1293b-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="1293b-111">**CurrentMhz**</span><span class="sxs-lookup"><span data-stu-id="1293b-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="1293b-112">Frequenza di clock del processore, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="1293b-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="1293b-113">Questo numero è la frequenza di clock del processore massima specificata moltiplicata per la limitazione del processore corrente.</span><span class="sxs-lookup"><span data-stu-id="1293b-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="1293b-114">**MhzLimit**</span><span class="sxs-lookup"><span data-stu-id="1293b-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="1293b-115">Limite sulla frequenza di clock del processore, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="1293b-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="1293b-116">Questo numero è la frequenza di clock del processore massima specificata moltiplicata per il limite di limitazione termica del processore corrente.</span><span class="sxs-lookup"><span data-stu-id="1293b-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="1293b-117">**MaxIdleState**</span><span class="sxs-lookup"><span data-stu-id="1293b-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="1293b-118">Stato di inattività massimo del processore.</span><span class="sxs-lookup"><span data-stu-id="1293b-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="1293b-119">**CurrentIdleState**</span><span class="sxs-lookup"><span data-stu-id="1293b-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="1293b-120">Stato di inattività corrente del processore.</span><span class="sxs-lookup"><span data-stu-id="1293b-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1293b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1293b-121">Remarks</span></span>

<span data-ttu-id="1293b-122">Si noti che questa definizione di struttura è stata accidentalmente omessa da WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="1293b-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="1293b-123">Questo errore verrà corretto in futuro.</span><span class="sxs-lookup"><span data-stu-id="1293b-123">This error will be corrected in the future.</span></span> <span data-ttu-id="1293b-124">Nel frattempo, per compilare l'applicazione, includere la definizione della struttura contenuta in questo argomento nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="1293b-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1293b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1293b-125">Requirements</span></span>



| <span data-ttu-id="1293b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1293b-126">Requirement</span></span> | <span data-ttu-id="1293b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1293b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1293b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1293b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1293b-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1293b-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1293b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1293b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1293b-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1293b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1293b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1293b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1293b-133">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="1293b-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 





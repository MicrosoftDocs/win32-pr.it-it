---
description: Contiene informazioni sull'inattività del sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Struttura SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967486"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="3fae8-103">\_ \_ Struttura delle informazioni sull'alimentazione del sistema</span><span class="sxs-lookup"><span data-stu-id="3fae8-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="3fae8-104">Contiene informazioni sull'inattività del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fae8-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fae8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fae8-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="3fae8-106">Members</span><span class="sxs-lookup"><span data-stu-id="3fae8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3fae8-107">**MaxIdlenessAllowed**</span><span class="sxs-lookup"><span data-stu-id="3fae8-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="3fae8-108">L'inattività in cui il sistema viene considerato inattivo e il timeout di inattività inizia il conteggio, espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="3fae8-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="3fae8-109">Se si scende sotto questo numero, il timer verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="3fae8-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="3fae8-110">**Inattività**</span><span class="sxs-lookup"><span data-stu-id="3fae8-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="3fae8-111">Il livello di inattività corrente, espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="3fae8-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="3fae8-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="3fae8-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="3fae8-113">Tempo rimanente del timer di inattività, in secondi.</span><span class="sxs-lookup"><span data-stu-id="3fae8-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="3fae8-114">**CoolingMode**</span><span class="sxs-lookup"><span data-stu-id="3fae8-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="3fae8-115">Modalità di raffreddamento del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="3fae8-115">The current system cooling mode.</span></span> <span data-ttu-id="3fae8-116">Questo membro deve avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3fae8-116">This member must one of the following values.</span></span>



| <span data-ttu-id="3fae8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3fae8-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="3fae8-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3fae8-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="3fae8-119"><dt>**Ordine di acquisto \_ TZ \_ attivo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3fae8-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="3fae8-120">Il sistema è attualmente in modalità di raffreddamento attiva.</span><span class="sxs-lookup"><span data-stu-id="3fae8-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="3fae8-121"><dt>**Ordine di acquisto \_ TZ \_ \_ modalità non valida**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3fae8-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3fae8-122">Il sistema non supporta la limitazione della CPU oppure non è stata definita alcuna zona termica nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3fae8-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="3fae8-123"><dt>**Ordine di acquisto \_ TZ \_ passive**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3fae8-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="3fae8-124">Il sistema è attualmente in modalità di raffreddamento passiva.</span><span class="sxs-lookup"><span data-stu-id="3fae8-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fae8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fae8-125">Remarks</span></span>

<span data-ttu-id="3fae8-126">Si noti che questa definizione di struttura è stata accidentalmente omessa da WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="3fae8-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="3fae8-127">Questo errore verrà corretto in futuro.</span><span class="sxs-lookup"><span data-stu-id="3fae8-127">This error will be corrected in the future.</span></span> <span data-ttu-id="3fae8-128">Nel frattempo, per compilare l'applicazione, includere la definizione della struttura contenuta in questo argomento nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="3fae8-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fae8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fae8-129">Requirements</span></span>



| <span data-ttu-id="3fae8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fae8-130">Requirement</span></span> | <span data-ttu-id="3fae8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3fae8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fae8-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fae8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3fae8-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3fae8-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3fae8-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fae8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3fae8-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fae8-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fae8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fae8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fae8-137">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="3fae8-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 





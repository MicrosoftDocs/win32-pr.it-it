---
description: La struttura STATIONQUERY fornisce informazioni su un computer specifico utilizzando Network Monitor.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Struttura STATIONQUERY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310480"
---
# <a name="stationquery-structure"></a><span data-ttu-id="d69be-103">Struttura STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="d69be-103">STATIONQUERY structure</span></span>

<span data-ttu-id="d69be-104">La struttura **STATIONQUERY** fornisce informazioni su un computer specifico utilizzando Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d69be-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d69be-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="d69be-106">Members</span><span class="sxs-lookup"><span data-stu-id="d69be-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d69be-107">**Flag**</span><span class="sxs-lookup"><span data-stu-id="d69be-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-108">Flag che identificano lo stato corrente del Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d69be-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="d69be-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d69be-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="d69be-110">Significato</span><span class="sxs-lookup"><span data-stu-id="d69be-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="d69be-111"><dt>**\_flag STATIONQUERY \_ caricati**</dt></span><span class="sxs-lookup"><span data-stu-id="d69be-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="d69be-112">Il driver viene caricato, ma il kernel non lo è.</span><span class="sxs-lookup"><span data-stu-id="d69be-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="d69be-113"><dt>**\_flag STATIONQUERY \_ in esecuzione**</dt></span><span class="sxs-lookup"><span data-stu-id="d69be-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="d69be-114">Il driver viene caricato ma non acquisisce i dati.</span><span class="sxs-lookup"><span data-stu-id="d69be-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="d69be-115"><dt>**\_acquisizione di flag STATIONQUERY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d69be-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="d69be-116">Il driver è attivamente coinvolto in un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d69be-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="d69be-117"><dt>**\_trasmissione di flag STATIONQUERY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d69be-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="d69be-118">Questo flag è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d69be-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="d69be-119">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="d69be-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-120">Numero di versione secondario di Network Monitor installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="d69be-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-121">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="d69be-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-122">Numero di versione principale di Network Monitor installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="d69be-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-123">**LicenseNumber**</span><span class="sxs-lookup"><span data-stu-id="d69be-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-124">Numero di licenza software.</span><span class="sxs-lookup"><span data-stu-id="d69be-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="d69be-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-126">Nome del produttore del computer, se presente.</span><span class="sxs-lookup"><span data-stu-id="d69be-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-127">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d69be-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-128">Nome utente o identificatore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d69be-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-129">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d69be-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-130">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="d69be-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-131">**AdapterAddress**</span><span class="sxs-lookup"><span data-stu-id="d69be-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-132">Indirizzo NIC.</span><span class="sxs-lookup"><span data-stu-id="d69be-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-133">**WMachineName**</span><span class="sxs-lookup"><span data-stu-id="d69be-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-134">Nome del computer Unicode.</span><span class="sxs-lookup"><span data-stu-id="d69be-134">Unicode computer name.</span></span> <span data-ttu-id="d69be-135">Questo membro si applica a Network Monitor 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d69be-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="d69be-136">**WUserName**</span><span class="sxs-lookup"><span data-stu-id="d69be-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="d69be-137">Nome utente Unicode.</span><span class="sxs-lookup"><span data-stu-id="d69be-137">Unicode user name.</span></span> <span data-ttu-id="d69be-138">Questo membro si applica a Network Monitor 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="d69be-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d69be-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="d69be-139">Remarks</span></span>

<span data-ttu-id="d69be-140">Una matrice di queste strutture viene utilizzata dalla struttura [QUERYTABLE](querytable.md) per fornire un elenco dei computer che attualmente utilizzano Network Monitor per acquisire i dati.</span><span class="sxs-lookup"><span data-stu-id="d69be-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69be-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d69be-141">Requirements</span></span>



| <span data-ttu-id="d69be-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d69be-142">Requirement</span></span> | <span data-ttu-id="d69be-143">Valore</span><span class="sxs-lookup"><span data-stu-id="d69be-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d69be-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d69be-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d69be-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d69be-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d69be-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d69be-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d69be-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d69be-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d69be-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d69be-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69be-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69be-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d69be-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d69be-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69be-151">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="d69be-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 





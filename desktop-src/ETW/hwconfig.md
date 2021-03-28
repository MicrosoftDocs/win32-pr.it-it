---
description: La classe HWConfig è la classe padre per gli eventi di configurazione hardware in Windows XP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Classe HWConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885562"
---
# <a name="hwconfig-class"></a><span data-ttu-id="52c8e-104">Classe HWConfig</span><span class="sxs-lookup"><span data-stu-id="52c8e-104">HWConfig class</span></span>

<span data-ttu-id="52c8e-105">La classe **HWConfig** è la classe padre per gli eventi di configurazione hardware in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52c8e-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="52c8e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="52c8e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c8e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52c8e-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="52c8e-108">Members</span><span class="sxs-lookup"><span data-stu-id="52c8e-108">Members</span></span>

<span data-ttu-id="52c8e-109">La classe **HWConfig** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="52c8e-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c8e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c8e-110">Remarks</span></span>

<span data-ttu-id="52c8e-111">Questi eventi forniscono la configurazione hardware del computer.</span><span class="sxs-lookup"><span data-stu-id="52c8e-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="52c8e-112">Diversamente dagli altri eventi del logger di kernel NT, la sessione kernel genera automaticamente gli eventi di configurazione hardware. questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.</span><span class="sxs-lookup"><span data-stu-id="52c8e-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="52c8e-113">**Windows 2000:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="52c8e-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="52c8e-114">Per gli eventi di configurazione hardware in Windows Vista e Windows Server 2003, vedere la classe [SystemConfig](systemconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="52c8e-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="52c8e-115">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="52c8e-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="52c8e-116">Usare i tipi di eventi seguenti per identificare l'evento di configurazione hardware effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="52c8e-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="52c8e-117">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="52c8e-117">Event type</span></span>                                                                      | <span data-ttu-id="52c8e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52c8e-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c8e-119">**Evento \_ Tipo di traccia \_ \_ \_ CPU di configurazione**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="52c8e-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="52c8e-120">Evento di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="52c8e-120">CPU configuration event.</span></span> <span data-ttu-id="52c8e-121">Le classi MOF della [**\_ CPU HWConfig**](hwconfig-cpu.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="52c8e-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="52c8e-122">**Evento \_ Tipo di traccia \_ \_ config \_ disco logico**(il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="52c8e-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="52c8e-123">Evento configurazione disco logico.</span><span class="sxs-lookup"><span data-stu-id="52c8e-123">Logical disk configuration event.</span></span> <span data-ttu-id="52c8e-124">La classe MOF delle classi MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="52c8e-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="52c8e-125">**Evento \_ \_ \_ \_ Scheda** di interfaccia di rete di tipo traccia (valore del tipo di evento 13)</span><span class="sxs-lookup"><span data-stu-id="52c8e-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="52c8e-126">Evento di configurazione NIC.</span><span class="sxs-lookup"><span data-stu-id="52c8e-126">NIC configuration event.</span></span> <span data-ttu-id="52c8e-127">Le classi MOF di [**\_ NIC HWConfig**](hwconfig-nic.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="52c8e-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="52c8e-128">**Evento \_ Tipo di traccia \_ \_ config \_ PHYSICALDISK**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="52c8e-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="52c8e-129">Evento di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="52c8e-129">Physical disk configuration event.</span></span> <span data-ttu-id="52c8e-130">Le classi MOF [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="52c8e-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="52c8e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c8e-131">Requirements</span></span>



| <span data-ttu-id="52c8e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c8e-132">Requirement</span></span> | <span data-ttu-id="52c8e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="52c8e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="52c8e-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c8e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="52c8e-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="52c8e-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="52c8e-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c8e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="52c8e-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="52c8e-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="52c8e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52c8e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c8e-139">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="52c8e-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="52c8e-140">**\_CPU HWConfig**</span><span class="sxs-lookup"><span data-stu-id="52c8e-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="52c8e-141">**\_LogDisk HWConfig**</span><span class="sxs-lookup"><span data-stu-id="52c8e-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="52c8e-142">**Scheda di interfaccia di rete HWConfig \_**</span><span class="sxs-lookup"><span data-stu-id="52c8e-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="52c8e-143">**\_PhyDisk HWConfig**</span><span class="sxs-lookup"><span data-stu-id="52c8e-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 

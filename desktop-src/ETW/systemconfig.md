---
description: Questa classe è la classe padre per gli eventi di configurazione hardware. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Classe SystemConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885872"
---
# <a name="systemconfig-class"></a><span data-ttu-id="53235-104">Classe SystemConfig</span><span class="sxs-lookup"><span data-stu-id="53235-104">SystemConfig class</span></span>

<span data-ttu-id="53235-105">Questa classe è la classe padre per gli eventi di configurazione hardware.</span><span class="sxs-lookup"><span data-stu-id="53235-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="53235-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="53235-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53235-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53235-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="53235-108">Members</span><span class="sxs-lookup"><span data-stu-id="53235-108">Members</span></span>

<span data-ttu-id="53235-109">La classe **SystemConfig** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="53235-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="53235-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="53235-110">Remarks</span></span>

<span data-ttu-id="53235-111">Questi eventi forniscono la configurazione hardware del computer.</span><span class="sxs-lookup"><span data-stu-id="53235-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="53235-112">Diversamente dagli altri eventi del logger di kernel NT, la sessione kernel genera automaticamente gli eventi di configurazione hardware. questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.</span><span class="sxs-lookup"><span data-stu-id="53235-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="53235-113">Per gli eventi di configurazione hardware in Windows XP, vedere la classe [HWConfig](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="53235-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="53235-114">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="53235-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="53235-115">Usare i tipi di eventi seguenti per identificare l'evento di configurazione hardware effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="53235-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="53235-116">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="53235-116">Event type</span></span>                                                                      | <span data-ttu-id="53235-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53235-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53235-118">**Evento \_ Tipo di traccia \_ \_ \_ CPU di configurazione**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="53235-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="53235-119">Evento di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="53235-119">CPU configuration event.</span></span> <span data-ttu-id="53235-120">Le classi MOF della [**\_ CPU SystemConfig**](systemconfig-cpu.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="53235-121">**Evento \_ Tipo di traccia \_ \_ config \_ IDECHANNEL**(il valore del tipo di evento è 23)</span><span class="sxs-lookup"><span data-stu-id="53235-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="53235-122">Evento di configurazione del canale IDE primario e secondario.</span><span class="sxs-lookup"><span data-stu-id="53235-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="53235-123">La classe MOF delle classi MOF [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="53235-124">**Evento \_ \_ \_ \_ IRQ Config del tipo di traccia**(il valore del tipo di evento è 21)</span><span class="sxs-lookup"><span data-stu-id="53235-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="53235-125">Evento di richiesta di interrupt (IRQ).</span><span class="sxs-lookup"><span data-stu-id="53235-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="53235-126">La classe MOF di [**SystemConfig \_ IRQ**](systemconfig-irq.md) Classis definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="53235-127">**Evento \_ Tipo di traccia \_ \_ config \_ disco logico**(il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="53235-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="53235-128">Evento configurazione disco logico.</span><span class="sxs-lookup"><span data-stu-id="53235-128">Logical disk configuration event.</span></span> <span data-ttu-id="53235-129">La classe MOF delle classi MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="53235-130">**Evento \_ Tipo di traccia \_ \_ config \_ NetInfo**(il valore del tipo di evento è 17)</span><span class="sxs-lookup"><span data-stu-id="53235-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="53235-131">Evento Iformation di rete.</span><span class="sxs-lookup"><span data-stu-id="53235-131">Network iformation event.</span></span> <span data-ttu-id="53235-132">La classe MOF di [**\_ rete SystemConfig**](systemconfig-network.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="53235-133">**Evento \_ \_ \_ \_ Scheda** di interfaccia di rete di tipo traccia (valore del tipo di evento 13)</span><span class="sxs-lookup"><span data-stu-id="53235-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="53235-134">Evento di configurazione NIC.</span><span class="sxs-lookup"><span data-stu-id="53235-134">NIC configuration event.</span></span> <span data-ttu-id="53235-135">Le classi MOF di [**\_ NIC SystemConfig**](systemconfig-nic.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="53235-136">**Evento \_ Tipo di traccia \_ \_ config \_ PHYSICALDISK**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="53235-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="53235-137">Evento di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="53235-137">Physical disk configuration event.</span></span> <span data-ttu-id="53235-138">Le classi MOF [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="53235-139">**Evento \_ Configurazione del tipo di traccia \_ \_ \_ PNP**(il valore del tipo di evento è 22)</span><span class="sxs-lookup"><span data-stu-id="53235-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="53235-140">Evento plug and Play.</span><span class="sxs-lookup"><span data-stu-id="53235-140">Plug and play event.</span></span> <span data-ttu-id="53235-141">La classe MOF [**SystemConfig \_ PNP**](systemconfig-pnp.md) classi MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="53235-142">**Evento \_ Configurazione del tipo di traccia \_ \_ \_ Power**(il valore del tipo di evento è 16)</span><span class="sxs-lookup"><span data-stu-id="53235-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="53235-143">Evento di configurazione risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="53235-143">Power configuration event.</span></span> <span data-ttu-id="53235-144">La classe [**SystemConfig di \_ Power**](systemconfig-power.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="53235-145">**Evento \_ \_Servizi di \_ configurazione \_ del tipo di traccia**(il valore del tipo di evento è 15)</span><span class="sxs-lookup"><span data-stu-id="53235-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="53235-146">Evento di configurazione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="53235-146">Services configuration event.</span></span> <span data-ttu-id="53235-147">La classe MOF dei [**\_ Servizi SystemConfig**](systemconfig-services.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="53235-148">**Evento \_ Tipo di traccia \_ \_ \_ video di configurazione**(il valore del tipo di evento è 14)</span><span class="sxs-lookup"><span data-stu-id="53235-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="53235-149">Evento di configurazione della scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="53235-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="53235-150">La classe MOF [**\_ video SystemConfig**](systemconfig-video.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="53235-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="53235-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53235-151">Requirements</span></span>



| <span data-ttu-id="53235-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="53235-152">Requirement</span></span> | <span data-ttu-id="53235-153">Valore</span><span class="sxs-lookup"><span data-stu-id="53235-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53235-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53235-154">Minimum supported client</span></span><br/> | <span data-ttu-id="53235-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53235-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53235-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53235-156">Minimum supported server</span></span><br/> | <span data-ttu-id="53235-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53235-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53235-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53235-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53235-159">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="53235-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="53235-160">**\_CPU SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="53235-161">**\_IDEChannel SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="53235-162">**\_IRQ SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="53235-163">**\_LogDisk SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="53235-164">**\_Rete SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="53235-165">**Scheda di interfaccia di rete SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="53235-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="53235-166">**\_PhyDisk SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="53235-167">**SystemConfig \_ PNP**</span><span class="sxs-lookup"><span data-stu-id="53235-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="53235-168">**\_Power SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="53235-169">**\_Servizi SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="53235-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="53235-170">**Video di SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="53235-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="53235-171">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="53235-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 

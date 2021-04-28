---
description: 'Classe SystemConfig: questa classe è la classe padre per gli eventi di configurazione hardware. La sintassi seguente è semplificata dal codice MOF.'
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
ms.openlocfilehash: 232214aa2c33485d909525d54965f59fdc891a29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105869"
---
# <a name="systemconfig-class"></a><span data-ttu-id="f9adc-104">Classe SystemConfig</span><span class="sxs-lookup"><span data-stu-id="f9adc-104">SystemConfig class</span></span>

<span data-ttu-id="f9adc-105">Questa classe è la classe padre per gli eventi di configurazione hardware.</span><span class="sxs-lookup"><span data-stu-id="f9adc-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="f9adc-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f9adc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9adc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9adc-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f9adc-108">Members</span><span class="sxs-lookup"><span data-stu-id="f9adc-108">Members</span></span>

<span data-ttu-id="f9adc-109">La **classe SystemConfig** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="f9adc-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9adc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9adc-110">Remarks</span></span>

<span data-ttu-id="f9adc-111">Questi eventi forniscono la configurazione hardware del computer.</span><span class="sxs-lookup"><span data-stu-id="f9adc-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="f9adc-112">A differenza di altri eventi del logger del kernel NT, la sessione del kernel genera automaticamente eventi di configurazione hardware. questi eventi non vengono abilitati all'avvio della sessione del logger del kernel NT.</span><span class="sxs-lookup"><span data-stu-id="f9adc-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="f9adc-113">Per gli eventi di configurazione hardware in Windows XP, vedere la [classe HWConfig.](hwconfig.md)</span><span class="sxs-lookup"><span data-stu-id="f9adc-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="f9adc-114">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di configurazione hardware chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="f9adc-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="f9adc-115">Usare i tipi di evento seguenti per identificare l'evento di configurazione hardware effettivo quando si usano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f9adc-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="f9adc-116">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="f9adc-116">Event type</span></span>                                                                      | <span data-ttu-id="f9adc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9adc-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9adc-118">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="f9adc-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="f9adc-119">Evento di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="f9adc-119">CPU configuration event.</span></span> <span data-ttu-id="f9adc-120">Le [**classi MOF \_ della CPU SystemConfig**](systemconfig-cpu.md) definiscono i dati degli eventi per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="f9adc-121">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ IDECHANNEL**(il valore del tipo di evento è 23)</span><span class="sxs-lookup"><span data-stu-id="f9adc-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="f9adc-122">Evento di configurazione del canale IDE primario e secondario.</span><span class="sxs-lookup"><span data-stu-id="f9adc-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="f9adc-123">La classe MOF delle classi MOF [**SYSTEMConfig \_ IDEChannel**](systemconfig-idechannel.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="f9adc-124">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ IRQ**(il valore del tipo di evento è 21)</span><span class="sxs-lookup"><span data-stu-id="f9adc-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="f9adc-125">Evento di richiesta di interruzione (IRQ).</span><span class="sxs-lookup"><span data-stu-id="f9adc-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="f9adc-126">La classe MOF delle classi MOF [**SystemConfig \_ IRQ**](systemconfig-irq.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="f9adc-127">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="f9adc-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="f9adc-128">Evento di configurazione del disco logico.</span><span class="sxs-lookup"><span data-stu-id="f9adc-128">Logical disk configuration event.</span></span> <span data-ttu-id="f9adc-129">La classe MOF delle classi MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="f9adc-130">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ NETINFO**(il valore del tipo di evento è 17)</span><span class="sxs-lookup"><span data-stu-id="f9adc-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="f9adc-131">Evento di iformazione di rete.</span><span class="sxs-lookup"><span data-stu-id="f9adc-131">Network iformation event.</span></span> <span data-ttu-id="f9adc-132">La [**classe MOF \_ di**](systemconfig-network.md) rete SystemConfig definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="f9adc-133">**EVENTO \_ SCHEDA \_ DI INTERFACCIA DI \_ \_ RETE TRACE TYPE CONFIG**(il valore del tipo di evento è 13)</span><span class="sxs-lookup"><span data-stu-id="f9adc-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="f9adc-134">Evento di configurazione della scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f9adc-134">NIC configuration event.</span></span> <span data-ttu-id="f9adc-135">Le [**classi MOF \_ della**](systemconfig-nic.md) scheda di interfaccia di rete SystemConfig definiscono i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="f9adc-136">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="f9adc-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="f9adc-137">Evento di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="f9adc-137">Physical disk configuration event.</span></span> <span data-ttu-id="f9adc-138">Le [**classi MOF \_ SystemConfig PhyDisk**](systemconfig-phydisk.md) definiscono i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="f9adc-139">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ PNP**(il valore del tipo di evento è 22)</span><span class="sxs-lookup"><span data-stu-id="f9adc-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="f9adc-140">Evento Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="f9adc-140">Plug and play event.</span></span> <span data-ttu-id="f9adc-141">La classe MOF delle classi MOF [**\_ SystemConfig PNP**](systemconfig-pnp.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="f9adc-142">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ POWER**(il valore del tipo di evento è 16)</span><span class="sxs-lookup"><span data-stu-id="f9adc-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="f9adc-143">Evento di configurazione dell'alimentazione.</span><span class="sxs-lookup"><span data-stu-id="f9adc-143">Power configuration event.</span></span> <span data-ttu-id="f9adc-144">La [**classe SystemConfig \_ Power**](systemconfig-power.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="f9adc-145">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ SERVICES**(il valore del tipo di evento è 15)</span><span class="sxs-lookup"><span data-stu-id="f9adc-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="f9adc-146">Evento di configurazione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="f9adc-146">Services configuration event.</span></span> <span data-ttu-id="f9adc-147">La [**classe MOF di SystemConfig \_ Services**](systemconfig-services.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="f9adc-148">**EVENTO \_ TRACE \_ TYPE \_ CONFIG \_ VIDEO**(il valore del tipo di evento è 14)</span><span class="sxs-lookup"><span data-stu-id="f9adc-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="f9adc-149">Evento di configurazione dell'adattatore grafico.</span><span class="sxs-lookup"><span data-stu-id="f9adc-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="f9adc-150">La [**classe MOF \_ SystemConfig Video**](systemconfig-video.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f9adc-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="f9adc-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9adc-151">Requirements</span></span>



| <span data-ttu-id="f9adc-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9adc-152">Requirement</span></span> | <span data-ttu-id="f9adc-153">Valore</span><span class="sxs-lookup"><span data-stu-id="f9adc-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9adc-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9adc-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f9adc-155">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9adc-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9adc-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9adc-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f9adc-157">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9adc-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9adc-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9adc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9adc-159">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="f9adc-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="f9adc-160">**SystemConfig \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="f9adc-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="f9adc-161">**SystemConfig \_ IDEChannel**</span><span class="sxs-lookup"><span data-stu-id="f9adc-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="f9adc-162">**SystemConfig \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="f9adc-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="f9adc-163">**SystemConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="f9adc-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="f9adc-164">**Rete \_ SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f9adc-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="f9adc-165">**Scheda di interfaccia di rete SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="f9adc-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="f9adc-166">**SystemConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="f9adc-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="f9adc-167">**SystemConfig \_ PNP**</span><span class="sxs-lookup"><span data-stu-id="f9adc-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="f9adc-168">**SystemConfig \_ Power**</span><span class="sxs-lookup"><span data-stu-id="f9adc-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="f9adc-169">**Servizi \_ SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f9adc-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="f9adc-170">**Video di \_ SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f9adc-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="f9adc-171">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="f9adc-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 

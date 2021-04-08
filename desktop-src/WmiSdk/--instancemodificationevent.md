---
description: Segnala un evento di modifica dell'istanza, ovvero un tipo di evento intrinseco generato quando un'istanza viene modificata nello spazio dei nomi.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Classe __InstanceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883549"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="b246c-103">\_\_Classe InstanceModificationEvent</span><span class="sxs-lookup"><span data-stu-id="b246c-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="b246c-104">La classe di sistema **\_ \_ InstanceModificationEvent** segnala un evento di modifica dell'istanza, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando un'istanza viene modificata nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b246c-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="b246c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b246c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b246c-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b246c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b246c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b246c-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="b246c-108">Members</span><span class="sxs-lookup"><span data-stu-id="b246c-108">Members</span></span>

<span data-ttu-id="b246c-109">La classe **\_ \_ InstanceModificationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b246c-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b246c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b246c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b246c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b246c-111">Properties</span></span>

<span data-ttu-id="b246c-112">La classe **\_ \_ InstanceModificationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b246c-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b246c-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="b246c-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b246c-114">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="b246c-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b246c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b246c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b246c-116">Copia dell'istanza prima della modifica.</span><span class="sxs-lookup"><span data-stu-id="b246c-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="b246c-117">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="b246c-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b246c-118">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b246c-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b246c-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b246c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b246c-120">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="b246c-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b246c-121">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b246c-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="b246c-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="b246c-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b246c-123">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="b246c-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b246c-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b246c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b246c-125">Nuova versione dell'istanza modificata.</span><span class="sxs-lookup"><span data-stu-id="b246c-125">New version of the changed instance.</span></span> <span data-ttu-id="b246c-126">Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="b246c-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b246c-127">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="b246c-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b246c-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b246c-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b246c-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b246c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b246c-130">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b246c-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b246c-131">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="b246c-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b246c-132">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="b246c-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="b246c-133">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b246c-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b246c-134">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b246c-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b246c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="b246c-135">Remarks</span></span>

<span data-ttu-id="b246c-136">La classe **\_ \_ InstanceModificationEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="b246c-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="b246c-137">**Modifica di una risorsa: \_ \_ InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="b246c-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="b246c-138">Si supponga di sospettare che un'applicazione di gestione in uso modifichi erroneamente il tipo di avvio di un servizio in uno dei server.</span><span class="sxs-lookup"><span data-stu-id="b246c-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="b246c-139">Si desidera scrivere uno script WMI per monitorare tutte le modifiche apportate alla configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="b246c-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="b246c-140">Non appena viene apportata una modifica a un servizio, il TargetInstance corrispondente riflette la modifica.</span><span class="sxs-lookup"><span data-stu-id="b246c-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="b246c-141">Se si registra il proprio interesse in questo evento, una modifica alla configurazione del servizio comporta la creazione di un'istanza della classe **\_ \_ InstanceModificationEvent** .</span><span class="sxs-lookup"><span data-stu-id="b246c-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="b246c-142">Per le query di notifica che richiedono la notifica della modifica di una risorsa e l'utilizzo di eventi intrinseci tutti viene utilizzata una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="b246c-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="b246c-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="b246c-143">Examples</span></span>

<span data-ttu-id="b246c-144">L'esempio di [monitoraggio del processo di modifica dell'evento](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sulla raccolta TechNet utilizza **\_ \_ InstanceModificationEvent** per monitorare la prima occorrenza di un evento di modifica dell'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="b246c-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="b246c-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b246c-145">Requirements</span></span>



| <span data-ttu-id="b246c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b246c-146">Requirement</span></span> | <span data-ttu-id="b246c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="b246c-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b246c-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b246c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b246c-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b246c-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b246c-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b246c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b246c-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b246c-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b246c-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b246c-152">Namespace</span></span><br/>                | <span data-ttu-id="b246c-153">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="b246c-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b246c-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b246c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b246c-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="b246c-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="b246c-156">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b246c-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


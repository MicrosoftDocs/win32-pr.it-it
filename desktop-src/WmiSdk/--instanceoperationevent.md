---
description: Funge da classe base per tutti gli eventi intrinseci correlati a un'istanza di.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Classe __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317592"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="12d76-103">\_\_Classe InstanceOperationEvent</span><span class="sxs-lookup"><span data-stu-id="12d76-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="12d76-104">La classe di sistema **\_ \_ InstanceOperationEvent** funge da classe di base per tutti gli eventi intrinseci correlati a un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="12d76-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="12d76-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="12d76-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="12d76-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="12d76-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d76-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12d76-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="12d76-108">Members</span><span class="sxs-lookup"><span data-stu-id="12d76-108">Members</span></span>

<span data-ttu-id="12d76-109">La classe **\_ \_ InstanceOperationEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="12d76-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="12d76-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12d76-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12d76-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12d76-111">Properties</span></span>

<span data-ttu-id="12d76-112">La classe **\_ \_ InstanceOperationEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="12d76-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12d76-113">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="12d76-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d76-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="12d76-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="12d76-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12d76-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d76-116">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="12d76-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="12d76-117">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="12d76-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="12d76-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="12d76-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d76-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="12d76-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="12d76-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12d76-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d76-121">Istanza interessata dall'evento.</span><span class="sxs-lookup"><span data-stu-id="12d76-121">Instance affected by the event.</span></span> <span data-ttu-id="12d76-122">Per gli eventi di creazione, si tratta dell'istanza appena creata.</span><span class="sxs-lookup"><span data-stu-id="12d76-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="12d76-123">Per gli eventi di modifica, si tratta della nuova versione dell'istanza modificata.</span><span class="sxs-lookup"><span data-stu-id="12d76-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="12d76-124">Per gli eventi di eliminazione, si tratta dell'istanza eliminata.</span><span class="sxs-lookup"><span data-stu-id="12d76-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="12d76-125">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="12d76-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d76-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12d76-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12d76-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12d76-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d76-128">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="12d76-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="12d76-129">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="12d76-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="12d76-130">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="12d76-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="12d76-131">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="12d76-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="12d76-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12d76-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12d76-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="12d76-133">Remarks</span></span>

<span data-ttu-id="12d76-134">La classe **\_ \_ InstanceOperationEvent** è derivata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="12d76-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="12d76-135">Le istanze di **\_ \_ InstanceOperationEvent** non vengono create. vengono create solo le istanze delle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="12d76-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="12d76-136">Le classi seguenti derivano da **\_ \_ InstanceOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="12d76-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="12d76-137">**\_\_InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="12d76-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="12d76-138">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="12d76-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="12d76-139">**\_\_InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="12d76-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="12d76-140">**Overview**</span><span class="sxs-lookup"><span data-stu-id="12d76-140">**Overview**</span></span>

<span data-ttu-id="12d76-141">Analogamente a una classe WMI che rappresenta ogni tipo di risorsa di sistema che può essere gestita tramite WMI, esiste una classe WMI che rappresenta ogni tipo di evento WMI.</span><span class="sxs-lookup"><span data-stu-id="12d76-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="12d76-142">Quando si verifica un evento che può essere monitorato da WMI, viene creata un'istanza della classe di evento WMI corrispondente.</span><span class="sxs-lookup"><span data-stu-id="12d76-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="12d76-143">Un evento WMI si verifica quando viene creata l'istanza.</span><span class="sxs-lookup"><span data-stu-id="12d76-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="12d76-144">Esistono tre tipi principali di classi di evento WMI, che derivano tutti dalla classe WMI dell' [**\_ \_ evento**](--event.md) : eventi intrinseci, eventi estrinseci ed eventi del timer.</span><span class="sxs-lookup"><span data-stu-id="12d76-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="12d76-145">Gli eventi intrinseci, a loro volta, sono rappresentati da tre classi distinte derivate dalla classe di **\_ \_ evento** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** e [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="12d76-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="12d76-146">Eventi intrinseci</span><span class="sxs-lookup"><span data-stu-id="12d76-146">Intrinsic Events</span></span>

<span data-ttu-id="12d76-147">Gli eventi intrinseci vengono usati per monitorare una risorsa rappresentata da una classe nel repository CIM.</span><span class="sxs-lookup"><span data-stu-id="12d76-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="12d76-148">Ogni risorsa è rappresentata da un'istanza di una classe.</span><span class="sxs-lookup"><span data-stu-id="12d76-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="12d76-149">Questo significa che il monitoraggio di una risorsa tramite WMI comporta effettivamente il monitoraggio delle istanze che corrispondono alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="12d76-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="12d76-150">Gli eventi intrinseci possono essere usati anche per monitorare le modifiche apportate a uno spazio dei nomi o a una classe nel repository.</span><span class="sxs-lookup"><span data-stu-id="12d76-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="12d76-151">Tuttavia, il monitoraggio delle modifiche apportate agli spazi dei nomi o alle classi ha un valore limitato per gli amministratori di sistema.</span><span class="sxs-lookup"><span data-stu-id="12d76-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="12d76-152">Un evento intrinseco è rappresentato da un'istanza di una classe derivata da \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent o \_ \_ ClassOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="12d76-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="12d76-153">Tutte le modifiche apportate alle istanze in WMI sono rappresentate dalla \_ \_ classe InstanceOperationEvent e dalle classi derivate: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.</span><span class="sxs-lookup"><span data-stu-id="12d76-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="12d76-154">Il monitoraggio delle risorse tramite WMI prevede il monitoraggio di istanze e tutte le modifiche alle istanze sono rappresentate da \_ \_ InstanceOperationEvent e dalle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="12d76-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="12d76-155">Questo significa che le risorse di monitoraggio includono in definitiva le istanze di monitoraggio delle \_ \_ classi derivate da InstanceOperationEvent.</span><span class="sxs-lookup"><span data-stu-id="12d76-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="12d76-156">Per registrare l'interesse nelle istanze di una di queste classi, è necessario emettere una query di notifica espressa in WQL.</span><span class="sxs-lookup"><span data-stu-id="12d76-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="12d76-157">La query utilizza una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="12d76-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="12d76-158">Per una discussione più lunga sull'utilizzo degli eventi dell'istanza WMI per monitorare l'attività del computer, vedere [come è possibile monitorare i diversi tipi di eventi con un solo script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="12d76-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="12d76-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="12d76-159">Examples</span></span>

<span data-ttu-id="12d76-160">L'esempio di codice per l' [evento di monitoraggio](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript della raccolta TechNet USA **\_ \_ InstanceOperationEvent** per monitorare il primo evento dell'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="12d76-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="12d76-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d76-161">Requirements</span></span>



| <span data-ttu-id="12d76-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d76-162">Requirement</span></span> | <span data-ttu-id="12d76-163">Valore</span><span class="sxs-lookup"><span data-stu-id="12d76-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="12d76-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d76-164">Minimum supported client</span></span><br/> | <span data-ttu-id="12d76-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12d76-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="12d76-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d76-166">Minimum supported server</span></span><br/> | <span data-ttu-id="12d76-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12d76-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="12d76-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12d76-168">Namespace</span></span><br/>                | <span data-ttu-id="12d76-169">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="12d76-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="12d76-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12d76-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d76-171">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="12d76-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="12d76-172">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="12d76-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="12d76-173">Determinazione del tipo di evento da ricevere</span><span class="sxs-lookup"><span data-stu-id="12d76-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="12d76-174">Scrittura in un file di log in base a un evento</span><span class="sxs-lookup"><span data-stu-id="12d76-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 


---
description: Per la registrazione di un consumer di eventi permanenti è necessaria un'istanza della \_ \_ classe di sistema eventfilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: Classe __EventFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314607"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="45ed8-103">\_\_Classe EventFilter</span><span class="sxs-lookup"><span data-stu-id="45ed8-103">\_\_EventFilter class</span></span>

<span data-ttu-id="45ed8-104">Per la registrazione di un consumer di eventi permanenti è necessaria un'istanza della classe di sistema **\_ \_ EventFilter** .</span><span class="sxs-lookup"><span data-stu-id="45ed8-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="45ed8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="45ed8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="45ed8-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="45ed8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ed8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45ed8-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="45ed8-108">Members</span><span class="sxs-lookup"><span data-stu-id="45ed8-108">Members</span></span>

<span data-ttu-id="45ed8-109">La classe **\_ \_ EventFilter** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="45ed8-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="45ed8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45ed8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45ed8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45ed8-111">Properties</span></span>

<span data-ttu-id="45ed8-112">La classe **\_ \_ EventFilter** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="45ed8-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45ed8-113">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="45ed8-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ed8-114">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="45ed8-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45ed8-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45ed8-116">ID di sicurezza (SID) che identifica in modo univoco l'utente che crea il filtro.</span><span class="sxs-lookup"><span data-stu-id="45ed8-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="45ed8-117">In Strumentazione gestione Windows (WMI) viene archiviato il SID dell'utente che crea un'istanza di **\_ \_ EventFilter** o il SID Administrator, a seconda del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="45ed8-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="45ed8-118">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="45ed8-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="45ed8-119">**EventAccess**</span><span class="sxs-lookup"><span data-stu-id="45ed8-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ed8-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45ed8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45ed8-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45ed8-122">Descrittore di sicurezza (SD) in Security Descriptor Definition Language (SDDL) che controlla l'accesso agli eventi recapitati al filtro.</span><span class="sxs-lookup"><span data-stu-id="45ed8-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="45ed8-123">Usare questa proprietà per specificare che solo gli eventi nel contesto di sicurezza di account specifici possono essere recapitati a questo filtro.</span><span class="sxs-lookup"><span data-stu-id="45ed8-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="45ed8-124">Un consumer di eventi permanenti può ad esempio cancellare i registri di sicurezza solo quando un determinato evento viene generato da un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="45ed8-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="45ed8-125">Per specificare gli utenti che possono pubblicare eventi in questo filtro, usare la maschera di **\_ \_ pubblicazione a destra WBEM** nella voce di controllo di accesso (ACE) per la proprietà del [**\_ descrittore di sicurezza**](--event.md) .</span><span class="sxs-lookup"><span data-stu-id="45ed8-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="45ed8-126">Per ulteriori informazioni, vedere [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="45ed8-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="45ed8-127">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="45ed8-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="45ed8-128">Per ulteriori informazioni ed esempi, vedere Replace:[ricezione di eventi](receiving-events-securely.md)in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="45ed8-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="45ed8-129">È possibile configurare un descrittore di sicurezza per l'accesso agli eventi per consentire il recapito di un evento solo quando l'account di sistema locale genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="45ed8-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="45ed8-130">Per ulteriori informazioni sulla creazione di un descrittore di sicurezza e l'autorizzazione dell'accesso, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="45ed8-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="45ed8-131">Esempio: la stringa SDDL seguente consente solo agli amministratori di fornire eventi al filtro.</span><span class="sxs-lookup"><span data-stu-id="45ed8-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="45ed8-132">Il diritto necessario per fornire gli eventi è **WBEM \_ right \_ Publish** (X80).</span><span class="sxs-lookup"><span data-stu-id="45ed8-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="45ed8-133">**EventNamespace**</span><span class="sxs-lookup"><span data-stu-id="45ed8-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ed8-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45ed8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45ed8-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45ed8-136">Spazio dei nomi dell'istanza di evento utilizzata per le sottoscrizioni tra gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="45ed8-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="45ed8-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="45ed8-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ed8-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45ed8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45ed8-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-140">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="45ed8-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="45ed8-141">Identificatore univoco di un filtro evento.</span><span class="sxs-lookup"><span data-stu-id="45ed8-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="45ed8-142">Poiché un filtro eventi viene utilizzato solo internamente da WMI, è consigliabile impostare questa proprietà su un identificatore univoco globale (**GUID**) convertito in una stringa.</span><span class="sxs-lookup"><span data-stu-id="45ed8-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="45ed8-143">Tuttavia, i consumer possono utilizzare qualsiasi schema privato per un nome di filtro, purché non esista un conflitto con altri filtri.</span><span class="sxs-lookup"><span data-stu-id="45ed8-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="45ed8-144">**Query**</span><span class="sxs-lookup"><span data-stu-id="45ed8-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ed8-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45ed8-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45ed8-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45ed8-147">Query di evento WQL (Strumentazione gestione Windows Query Language) che specifica il set di eventi per la notifica del consumer e le condizioni specifiche per la notifica.</span><span class="sxs-lookup"><span data-stu-id="45ed8-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="45ed8-148">**QueryLanguage**</span><span class="sxs-lookup"><span data-stu-id="45ed8-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45ed8-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45ed8-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45ed8-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45ed8-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45ed8-151">Lingua utilizzata per la query.</span><span class="sxs-lookup"><span data-stu-id="45ed8-151">Language used for the query.</span></span> <span data-ttu-id="45ed8-152">Poiché WMI supporta attualmente solo WMI Query Language (WQL) come linguaggio di query, questa proprietà deve essere impostata su "WQL".</span><span class="sxs-lookup"><span data-stu-id="45ed8-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45ed8-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="45ed8-153">Remarks</span></span>

<span data-ttu-id="45ed8-154">La classe **\_ \_ EventFilter** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md).</span><span class="sxs-lookup"><span data-stu-id="45ed8-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="45ed8-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="45ed8-155">Examples</span></span>

<span data-ttu-id="45ed8-156">Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **\_ \_ EventFilter** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="45ed8-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ed8-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45ed8-157">Requirements</span></span>



| <span data-ttu-id="45ed8-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="45ed8-158">Requirement</span></span> | <span data-ttu-id="45ed8-159">Valore</span><span class="sxs-lookup"><span data-stu-id="45ed8-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="45ed8-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45ed8-160">Minimum supported client</span></span><br/> | <span data-ttu-id="45ed8-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45ed8-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="45ed8-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45ed8-162">Minimum supported server</span></span><br/> | <span data-ttu-id="45ed8-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45ed8-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="45ed8-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45ed8-164">Namespace</span></span><br/>                | <span data-ttu-id="45ed8-165">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="45ed8-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="45ed8-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45ed8-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ed8-167">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="45ed8-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="45ed8-168">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="45ed8-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="45ed8-169">Creazione di un filtro eventi</span><span class="sxs-lookup"><span data-stu-id="45ed8-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="45ed8-170">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="45ed8-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="45ed8-171">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="45ed8-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="45ed8-172">Monitoraggio degli eventi</span><span class="sxs-lookup"><span data-stu-id="45ed8-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="45ed8-173">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="45ed8-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="45ed8-174">Protezione degli eventi WMI</span><span class="sxs-lookup"><span data-stu-id="45ed8-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 


---
description: Viene utilizzato nella registrazione di consumer di eventi permanenti per correlare un'istanza di \_ \_ EventConsumer a un'istanza di \_ \_ eventfilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Classe __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
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
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317596"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="651d6-103">\_\_Classe FilterToConsumerBinding</span><span class="sxs-lookup"><span data-stu-id="651d6-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="651d6-104">La classe di sistema **\_ \_ FilterToConsumerBinding** viene utilizzata per la registrazione di consumer di eventi permanenti per correlare un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) a un'istanza di [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** è una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="651d6-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="651d6-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="651d6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="651d6-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="651d6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="651d6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="651d6-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="651d6-108">Members</span><span class="sxs-lookup"><span data-stu-id="651d6-108">Members</span></span>

<span data-ttu-id="651d6-109">La classe **\_ \_ FilterToConsumerBinding** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="651d6-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="651d6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="651d6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="651d6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="651d6-111">Properties</span></span>

<span data-ttu-id="651d6-112">La classe **\_ \_ FilterToConsumerBinding** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="651d6-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="651d6-113">**Consumer**</span><span class="sxs-lookup"><span data-stu-id="651d6-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-114">Tipo di dati: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="651d6-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="651d6-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="651d6-116">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="651d6-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="651d6-117">Riferimento a un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) che rappresenta il percorso dell'oggetto a un consumer logico, il destinatario di un evento.</span><span class="sxs-lookup"><span data-stu-id="651d6-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="651d6-118">Un consumer logico è un'istanza di una classe derivata da **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="651d6-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="651d6-119">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="651d6-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-120">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="651d6-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="651d6-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="651d6-122">ID di sicurezza (SID) che identifica in modo univoco l'utente che ha creato l'associazione.</span><span class="sxs-lookup"><span data-stu-id="651d6-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="651d6-123">A seconda del sistema operativo, WMI archivia il SID amministratore o il SID dell'utente che crea un'istanza di **\_ \_ FilterToConsumerBinding**.</span><span class="sxs-lookup"><span data-stu-id="651d6-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="651d6-124">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="651d6-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="651d6-125">**DeliverSynchronously**</span><span class="sxs-lookup"><span data-stu-id="651d6-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="651d6-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="651d6-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="651d6-128">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="651d6-128">Obsolete.</span></span> <span data-ttu-id="651d6-129">Usare invece la proprietà **DeliveryQoS** al posto di questa proprietà, perché se **DeliverSynchronously** è impostato su **true** , viene eseguito l'override dell'impostazione della proprietà **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="651d6-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="651d6-130">**DeliveryQoS**</span><span class="sxs-lookup"><span data-stu-id="651d6-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="651d6-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="651d6-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="651d6-133">Qualità del servizio per una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="651d6-133">Quality of service for a subscription.</span></span> <span data-ttu-id="651d6-134">Se la proprietà **DeliverSynchronously** è impostata su **true**, esegue l'override dell'impostazione della proprietà **DeliveryQoS** .</span><span class="sxs-lookup"><span data-stu-id="651d6-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="651d6-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ FLAG \_ QoS \_ sincrono** (0)</span><span class="sxs-lookup"><span data-stu-id="651d6-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="651d6-136">Recapito sincrono</span><span class="sxs-lookup"><span data-stu-id="651d6-136">Synchronous delivery</span></span>

<span data-ttu-id="651d6-137">**False**.</span><span class="sxs-lookup"><span data-stu-id="651d6-137">**False**.</span></span> <span data-ttu-id="651d6-138">L'evento viene recapitato in modo sincrono al consumer logico.</span><span class="sxs-lookup"><span data-stu-id="651d6-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="651d6-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ FLAG \_ QoS \_ Express** (1)</span><span class="sxs-lookup"><span data-stu-id="651d6-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="651d6-140">Recapito rapido</span><span class="sxs-lookup"><span data-stu-id="651d6-140">Express delivery</span></span>

<span data-ttu-id="651d6-141">**True**.</span><span class="sxs-lookup"><span data-stu-id="651d6-141">**True**.</span></span> <span data-ttu-id="651d6-142">L'evento viene recapitato al consumer logico in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="651d6-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="651d6-143">**Filter**</span><span class="sxs-lookup"><span data-stu-id="651d6-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-144">Tipo di dati: **\_ \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="651d6-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="651d6-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="651d6-146">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="651d6-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="651d6-147">Riferimento a un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) che rappresenta il percorso dell'oggetto a un filtro eventi che è una query che specifica il tipo di evento da ricevere.</span><span class="sxs-lookup"><span data-stu-id="651d6-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="651d6-148">**MaintainSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="651d6-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-149">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="651d6-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="651d6-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="651d6-151">Se **true**, gli eventi vengono recapitati nello stesso contesto di sicurezza in cui si trovava il provider al momento della loro fornitura.</span><span class="sxs-lookup"><span data-stu-id="651d6-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="651d6-152">Solo un consumer implementato come DLL (un consumer in-process) può ricevere eventi nel contesto di sicurezza del provider.</span><span class="sxs-lookup"><span data-stu-id="651d6-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="651d6-153">Per ulteriori informazioni sulla sicurezza e sui provider in-process, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="651d6-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="651d6-154">Per ulteriori informazioni ed esempi, vedere Replace:[ricezione di eventi](receiving-events-securely.md)in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="651d6-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="651d6-155">**SlowDownProviders**</span><span class="sxs-lookup"><span data-stu-id="651d6-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="651d6-156">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="651d6-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="651d6-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="651d6-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="651d6-158">Se **true**, i provider vengono rallentati se il consumer non è in grado di rimanere attivi.</span><span class="sxs-lookup"><span data-stu-id="651d6-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="651d6-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="651d6-159">Remarks</span></span>

<span data-ttu-id="651d6-160">La classe **\_ \_ FilterToConsumerBinding** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="651d6-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="651d6-161">I consumer di eventi permanenti usano la classe di sistema **\_ \_ FilterToConsumerBinding** per associare i filtri eventi ai consumer finali.</span><span class="sxs-lookup"><span data-stu-id="651d6-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="651d6-162">Dopo aver associato il filtro e il consumer, WMI può inviare gli eventi che corrispondono al filtro al consumer corrispondente.</span><span class="sxs-lookup"><span data-stu-id="651d6-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="651d6-163">Esempio</span><span class="sxs-lookup"><span data-stu-id="651d6-163">Examples</span></span>

<span data-ttu-id="651d6-164">Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **\_ \_ FilterToConsumerBinding** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="651d6-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="651d6-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="651d6-165">Requirements</span></span>



| <span data-ttu-id="651d6-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="651d6-166">Requirement</span></span> | <span data-ttu-id="651d6-167">Valore</span><span class="sxs-lookup"><span data-stu-id="651d6-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="651d6-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651d6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="651d6-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="651d6-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="651d6-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651d6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="651d6-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="651d6-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="651d6-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="651d6-172">Namespace</span></span><br/>                | <span data-ttu-id="651d6-173">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="651d6-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="651d6-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="651d6-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651d6-175">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="651d6-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="651d6-176">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="651d6-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="651d6-177">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="651d6-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="651d6-178">Monitoraggio degli eventi</span><span class="sxs-lookup"><span data-stu-id="651d6-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="651d6-179">Creazione di un filtro eventi</span><span class="sxs-lookup"><span data-stu-id="651d6-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="651d6-180">Protezione degli eventi WMI</span><span class="sxs-lookup"><span data-stu-id="651d6-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 





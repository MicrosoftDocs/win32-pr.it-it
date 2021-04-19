---
description: La \_ classe CIM ClusteringService rappresenta la funzionalità fornita da un cluster. Ad esempio, la funzionalità di failover può essere modellata come servizio di un cluster di failover.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: Classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304980"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="54486-104">CIM \_ ClusteringService (classe)</span><span class="sxs-lookup"><span data-stu-id="54486-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="54486-105">La classe **CIM \_ ClusteringService** rappresenta la funzionalità fornita da un cluster.</span><span class="sxs-lookup"><span data-stu-id="54486-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="54486-106">Ad esempio, la funzionalità di failover può essere modellata come servizio di un cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="54486-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54486-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="54486-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="54486-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="54486-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="54486-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="54486-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="54486-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="54486-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54486-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54486-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="54486-112">Members</span><span class="sxs-lookup"><span data-stu-id="54486-112">Members</span></span>

<span data-ttu-id="54486-113">La classe **CIM \_ ClusteringService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54486-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="54486-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="54486-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="54486-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54486-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54486-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="54486-116">Methods</span></span>

<span data-ttu-id="54486-117">La classe **CIM \_ ClusteringService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="54486-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="54486-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="54486-118">Method</span></span>                                                                     | <span data-ttu-id="54486-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54486-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54486-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="54486-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="54486-121">Metodo della classe che porta un nuovo sistema di computer in un cluster.</span><span class="sxs-lookup"><span data-stu-id="54486-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="54486-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="54486-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="54486-123">**EvictNode**</span><span class="sxs-lookup"><span data-stu-id="54486-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="54486-124">Metodo della classe che rimuove un sistema di computer da un cluster.</span><span class="sxs-lookup"><span data-stu-id="54486-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="54486-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="54486-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="54486-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="54486-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="54486-127">Metodo della classe che tenta di collocare il servizio nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="54486-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="54486-128">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="54486-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="54486-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="54486-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="54486-130">Metodo della classe che inserisce il servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="54486-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="54486-131">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="54486-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="54486-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54486-132">Properties</span></span>

<span data-ttu-id="54486-133">La classe **CIM \_ ClusteringService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="54486-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54486-134">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="54486-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-137">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="54486-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="54486-138">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54486-138">A short textual description of the object.</span></span>

<span data-ttu-id="54486-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54486-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-140">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="54486-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-143">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="54486-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="54486-144">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="54486-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="54486-145">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="54486-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="54486-146">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-147">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="54486-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-150">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="54486-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="54486-151">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54486-151">A textual description of the object.</span></span>

<span data-ttu-id="54486-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54486-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="54486-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-154">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="54486-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54486-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-156">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="54486-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="54486-157">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="54486-157">Indicates when the object was installed.</span></span> <span data-ttu-id="54486-158">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="54486-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="54486-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54486-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="54486-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-163">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54486-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54486-164">La proprietà Name identifica in modo univoco il servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="54486-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="54486-165">Questa funzionalità è descritta più dettagliatamente nella proprietà Description dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54486-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="54486-166">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-167">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="54486-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="54486-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="54486-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-170">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="54486-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="54486-171">Se **true**, il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="54486-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="54486-172">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-173">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="54486-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-176">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="54486-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="54486-177">Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="54486-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="54486-178">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="54486-179">**Automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="54486-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="54486-180">**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="54486-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54486-181">**Status**</span><span class="sxs-lookup"><span data-stu-id="54486-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-184">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="54486-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="54486-185">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54486-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="54486-186">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="54486-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="54486-187">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="54486-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="54486-188">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="54486-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="54486-189">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="54486-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="54486-190">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="54486-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="54486-191">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="54486-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="54486-192">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54486-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="54486-193">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="54486-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="54486-194">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="54486-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="54486-195">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="54486-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="54486-196">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="54486-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54486-197">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="54486-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="54486-198">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="54486-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="54486-199">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="54486-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="54486-200">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="54486-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="54486-201">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="54486-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="54486-202">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="54486-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="54486-203">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="54486-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="54486-204">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="54486-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="54486-205">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="54486-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54486-206">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="54486-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-209">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="54486-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="54486-210">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="54486-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="54486-211">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="54486-212">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="54486-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54486-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="54486-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54486-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="54486-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54486-215">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="54486-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="54486-216">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="54486-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="54486-217">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54486-218">Commenti</span><span class="sxs-lookup"><span data-stu-id="54486-218">Remarks</span></span>

<span data-ttu-id="54486-219">La classe **CIM \_ ClusteringService** deriva dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="54486-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="54486-220">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="54486-220">WMI does not implement this class.</span></span>

<span data-ttu-id="54486-221">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="54486-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="54486-222">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="54486-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="54486-223">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54486-223">Requirements</span></span>



| <span data-ttu-id="54486-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="54486-224">Requirement</span></span> | <span data-ttu-id="54486-225">Valore</span><span class="sxs-lookup"><span data-stu-id="54486-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54486-226">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54486-226">Minimum supported client</span></span><br/> | <span data-ttu-id="54486-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54486-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54486-228">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54486-228">Minimum supported server</span></span><br/> | <span data-ttu-id="54486-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54486-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54486-230">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54486-230">Namespace</span></span><br/>                | <span data-ttu-id="54486-231">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="54486-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54486-232">MOF</span><span class="sxs-lookup"><span data-stu-id="54486-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54486-233"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54486-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54486-234">DLL</span><span class="sxs-lookup"><span data-stu-id="54486-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54486-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54486-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54486-236">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54486-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54486-237">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="54486-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


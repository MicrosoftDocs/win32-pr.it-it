---
description: La \_ classe del servizio CIM rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o del software.
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: Classe CIM_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304767"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ad16f-103">Classe CIM_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ad16f-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ad16f-104">La classe del **\_ servizio CIM** rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o del software.</span><span class="sxs-lookup"><span data-stu-id="ad16f-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="ad16f-105">Un servizio è un oggetto generico per la configurazione e la gestione dell'implementazione di funzionalità. non si tratta della funzionalità stessa.</span><span class="sxs-lookup"><span data-stu-id="ad16f-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad16f-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ad16f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ad16f-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ad16f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ad16f-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ad16f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ad16f-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ad16f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad16f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad16f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="ad16f-111">Members</span><span class="sxs-lookup"><span data-stu-id="ad16f-111">Members</span></span>

<span data-ttu-id="ad16f-112">La classe del **\_ servizio CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ad16f-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="ad16f-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="ad16f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ad16f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad16f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ad16f-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="ad16f-115">Methods</span></span>

<span data-ttu-id="ad16f-116">La classe del **\_ servizio CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ad16f-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="ad16f-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="ad16f-117">Method</span></span>                                                           | <span data-ttu-id="ad16f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad16f-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad16f-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="ad16f-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="ad16f-120">Tenta di inserire il servizio nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="ad16f-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="ad16f-121">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ad16f-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="ad16f-122">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ad16f-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="ad16f-123">Metodo della classe che inserisce il servizio nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="ad16f-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="ad16f-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ad16f-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ad16f-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad16f-125">Properties</span></span>

<span data-ttu-id="ad16f-126">La classe del **\_ servizio CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ad16f-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad16f-127">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ad16f-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ad16f-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-131">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad16f-131">A short textual description of the object.</span></span>

<span data-ttu-id="ad16f-132">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad16f-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ad16f-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-136">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="ad16f-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-137">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ad16f-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ad16f-138">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ad16f-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ad16f-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-142">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ad16f-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-143">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad16f-143">A textual description of the object.</span></span>

<span data-ttu-id="ad16f-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad16f-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ad16f-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad16f-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ad16f-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-149">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="ad16f-149">Indicates when the object was installed.</span></span> <span data-ttu-id="ad16f-150">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="ad16f-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ad16f-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad16f-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ad16f-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-155">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad16f-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-156">La proprietà Name identifica in modo univoco il servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="ad16f-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="ad16f-157">Questa funzionalità è descritta più dettagliatamente nella proprietà Description dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad16f-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-158">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="ad16f-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-159">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ad16f-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-161">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="ad16f-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-162">Se **true**, il servizio è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="ad16f-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-163">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="ad16f-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-166">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="ad16f-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-167">Indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, o se è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad16f-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ad16f-168">**Automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="ad16f-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="ad16f-169">**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="ad16f-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad16f-170">**Status**</span><span class="sxs-lookup"><span data-stu-id="ad16f-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-173">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ad16f-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-174">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad16f-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="ad16f-175">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="ad16f-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ad16f-176">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="ad16f-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ad16f-177">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="ad16f-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ad16f-178">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="ad16f-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ad16f-179">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="ad16f-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ad16f-180">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="ad16f-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ad16f-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad16f-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ad16f-182">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad16f-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ad16f-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ad16f-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ad16f-184">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ad16f-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ad16f-185">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ad16f-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad16f-186">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ad16f-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ad16f-187">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ad16f-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ad16f-188">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ad16f-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ad16f-189">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ad16f-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ad16f-190">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ad16f-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ad16f-191">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ad16f-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ad16f-192">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ad16f-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ad16f-193">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ad16f-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ad16f-194">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ad16f-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad16f-195">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ad16f-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-198">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="ad16f-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-199">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ad16f-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="ad16f-200">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ad16f-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad16f-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ad16f-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad16f-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad16f-203">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="ad16f-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ad16f-204">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="ad16f-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad16f-205">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad16f-205">Remarks</span></span>

<span data-ttu-id="ad16f-206">La classe del **\_ servizio CIM** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ad16f-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ad16f-207">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ad16f-207">WMI does not implement this class.</span></span> <span data-ttu-id="ad16f-208">Per le classi WMI derivate **dal \_ servizio CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ad16f-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ad16f-209">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ad16f-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ad16f-210">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ad16f-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad16f-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad16f-211">Requirements</span></span>



| <span data-ttu-id="ad16f-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad16f-212">Requirement</span></span> | <span data-ttu-id="ad16f-213">Valore</span><span class="sxs-lookup"><span data-stu-id="ad16f-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad16f-214">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad16f-214">Minimum supported client</span></span><br/> | <span data-ttu-id="ad16f-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad16f-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad16f-216">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad16f-216">Minimum supported server</span></span><br/> | <span data-ttu-id="ad16f-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad16f-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad16f-218">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad16f-218">Namespace</span></span><br/>                | <span data-ttu-id="ad16f-219">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ad16f-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad16f-220">MOF</span><span class="sxs-lookup"><span data-stu-id="ad16f-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad16f-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad16f-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad16f-222">DLL</span><span class="sxs-lookup"><span data-stu-id="ad16f-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad16f-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad16f-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad16f-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad16f-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad16f-225">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="ad16f-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 


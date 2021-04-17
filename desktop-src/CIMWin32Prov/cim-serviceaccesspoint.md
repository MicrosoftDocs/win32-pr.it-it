---
description: La \_ classe CIM serviceAccessPoint rappresenta la possibilità di usare o richiamare un servizio. I punti di accesso rappresentano i servizi disponibili per l'utilizzo da altre entità.
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: Classe CIM_ServiceAccessPoint (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523482"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="36f78-104">Classe CIM_ServiceAccessPoint (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="36f78-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="36f78-105">La classe **CIM \_ serviceAccessPoint** rappresenta la possibilità di usare o richiamare un servizio.</span><span class="sxs-lookup"><span data-stu-id="36f78-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="36f78-106">I punti di accesso rappresentano i servizi disponibili per l'utilizzo da altre entità.</span><span class="sxs-lookup"><span data-stu-id="36f78-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36f78-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="36f78-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36f78-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36f78-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36f78-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="36f78-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="36f78-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="36f78-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f78-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36f78-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="36f78-112">Members</span><span class="sxs-lookup"><span data-stu-id="36f78-112">Members</span></span>

<span data-ttu-id="36f78-113">La classe **CIM \_ serviceAccessPoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="36f78-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="36f78-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="36f78-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36f78-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="36f78-115">Properties</span></span>

<span data-ttu-id="36f78-116">La classe **CIM \_ serviceAccessPoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="36f78-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36f78-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="36f78-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="36f78-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="36f78-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36f78-121">A short textual description of the object.</span></span>

<span data-ttu-id="36f78-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36f78-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f78-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="36f78-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-126">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="36f78-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="36f78-127">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="36f78-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="36f78-128">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="36f78-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="36f78-129">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="36f78-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-132">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="36f78-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="36f78-133">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36f78-133">A textual description of the object.</span></span>

<span data-ttu-id="36f78-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36f78-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f78-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="36f78-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-136">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="36f78-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="36f78-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="36f78-139">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="36f78-139">Indicates when the object was installed.</span></span> <span data-ttu-id="36f78-140">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="36f78-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="36f78-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36f78-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f78-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="36f78-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-145">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="36f78-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="36f78-146">Identifica in modo univoco il punto di accesso al servizio e fornisce un'indicazione della funzionalità gestita.</span><span class="sxs-lookup"><span data-stu-id="36f78-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="36f78-147">Questa funzionalità è descritta più dettagliatamente nella proprietà Description dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36f78-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="36f78-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="36f78-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="36f78-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="36f78-152">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36f78-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="36f78-153">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="36f78-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="36f78-154">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="36f78-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="36f78-155">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="36f78-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="36f78-156">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="36f78-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="36f78-157">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="36f78-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="36f78-158">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="36f78-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="36f78-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36f78-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="36f78-160">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="36f78-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="36f78-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="36f78-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="36f78-162">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="36f78-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="36f78-163">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="36f78-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36f78-164">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="36f78-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="36f78-165">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="36f78-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="36f78-166">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="36f78-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="36f78-167">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="36f78-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="36f78-168">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="36f78-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="36f78-169">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="36f78-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="36f78-170">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="36f78-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="36f78-171">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="36f78-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="36f78-172">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="36f78-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36f78-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="36f78-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-176">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="36f78-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="36f78-177">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="36f78-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="36f78-178">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="36f78-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="36f78-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-181">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="36f78-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="36f78-182">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="36f78-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="36f78-183">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36f78-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f78-184">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36f78-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36f78-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f78-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f78-186">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="36f78-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="36f78-187">Tipo di SAP, ad esempio collegato o reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="36f78-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="36f78-188">**Scrittura** (1)</span><span class="sxs-lookup"><span data-stu-id="36f78-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="36f78-189">**Lettura** (2)</span><span class="sxs-lookup"><span data-stu-id="36f78-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="36f78-190">**Reindirizzato** (4)</span><span class="sxs-lookup"><span data-stu-id="36f78-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="36f78-191">**Rete \_ Collegato** (8)</span><span class="sxs-lookup"><span data-stu-id="36f78-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36f78-192">**sconosciuto** (16)</span><span class="sxs-lookup"><span data-stu-id="36f78-192">**unknown** (16)</span></span>


<span data-ttu-id="36f78-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36f78-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="36f78-194">Commenti</span><span class="sxs-lookup"><span data-stu-id="36f78-194">Remarks</span></span>

<span data-ttu-id="36f78-195">La classe **CIM \_ serviceAccessPoint** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="36f78-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="36f78-196">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="36f78-196">WMI does not implement this class.</span></span> <span data-ttu-id="36f78-197">Per le classi WMI derivate da **CIM \_ serviceAccessPoint**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36f78-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="36f78-198">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="36f78-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36f78-199">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="36f78-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f78-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36f78-200">Requirements</span></span>



| <span data-ttu-id="36f78-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f78-201">Requirement</span></span> | <span data-ttu-id="36f78-202">Valore</span><span class="sxs-lookup"><span data-stu-id="36f78-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36f78-203">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36f78-203">Minimum supported client</span></span><br/> | <span data-ttu-id="36f78-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36f78-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36f78-205">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36f78-205">Minimum supported server</span></span><br/> | <span data-ttu-id="36f78-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36f78-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36f78-207">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="36f78-207">Namespace</span></span><br/>                | <span data-ttu-id="36f78-208">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="36f78-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36f78-209">MOF</span><span class="sxs-lookup"><span data-stu-id="36f78-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36f78-210"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36f78-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36f78-211">DLL</span><span class="sxs-lookup"><span data-stu-id="36f78-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36f78-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36f78-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f78-213">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36f78-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f78-214">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="36f78-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 


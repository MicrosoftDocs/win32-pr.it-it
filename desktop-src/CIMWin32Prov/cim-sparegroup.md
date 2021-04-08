---
description: La \_ classe CIM SpareGroup è derivata dalla classe CIM \_ RedundancyGroup e indica che uno o più elementi aggregati possono essere risparmiati.
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: Classe CIM_SpareGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747831"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="5c5f2-103">CIM \_ SpareGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="5c5f2-104">La classe **CIM \_ SpareGroup** è derivata dalla classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) e indica che uno o più elementi aggregati possono essere risparmiati.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="5c5f2-105">Le sostituzioni vengono definite tramite l'associazione [**CIM \_ ActsAsSpare**](cim-actsasspare.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5f2-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="5c5f2-106">Un esempio di riserva è l'uso di schede di interfaccia di rete ridondanti in un computer, in cui una NIC è primaria e l'altra è di riserva.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="5c5f2-107">L'interfaccia di rete primaria è un membro del gruppo di riserva, associato usando la classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) e l'altra scheda di interfaccia di rete viene associata usando la relazione **CIM \_ ActsAsSpare** .</span><span class="sxs-lookup"><span data-stu-id="5c5f2-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c5f2-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5c5f2-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5c5f2-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5c5f2-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5f2-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c5f2-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="5c5f2-113">Members</span><span class="sxs-lookup"><span data-stu-id="5c5f2-113">Members</span></span>

<span data-ttu-id="5c5f2-114">La classe **CIM \_ SpareGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c5f2-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="5c5f2-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c5f2-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c5f2-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c5f2-116">Properties</span></span>

<span data-ttu-id="5c5f2-117">La classe **CIM \_ SpareGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c5f2-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-122">A short textual description of the object.</span></span>

<span data-ttu-id="5c5f2-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c5f2-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-127">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-128">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5c5f2-129">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5c5f2-130">Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c5f2-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-134">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-135">A textual description of the object.</span></span>

<span data-ttu-id="5c5f2-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c5f2-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-141">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-141">Indicates when the object was installed.</span></span> <span data-ttu-id="5c5f2-142">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5c5f2-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c5f2-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-147">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-148">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-148">Label by which the object is known.</span></span> <span data-ttu-id="5c5f2-149">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5c5f2-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c5f2-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-152">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-154">Informazioni sullo stato del gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="5c5f2-155">Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c5f2-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5c5f2-157">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c5f2-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5c5f2-159">Altro.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="5c5f2-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Completamente ridondante** (2)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5c5f2-161">È disponibile tutta la ridondanza configurata.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="5c5f2-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Ridondanza danneggiata** (3)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5c5f2-163">È disponibile una minore quantità di ridondanza a causa di alcuni errori.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="5c5f2-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Ridondanza persa** (4)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5c5f2-165">La ridondanza non è disponibile a causa di un numero sufficiente di errori.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="5c5f2-166">L'errore successivo provocherà un errore generale.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5c5f2-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5f2-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c5f2-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5f2-170">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5c5f2-171">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="5c5f2-172">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5c5f2-173">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="5c5f2-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5c5f2-174">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5c5f2-175">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5c5f2-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5c5f2-176">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5c5f2-177">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5c5f2-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5c5f2-179">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c5f2-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5c5f2-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5c5f2-181">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5c5f2-182">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="5c5f2-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c5f2-183">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5c5f2-184">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5c5f2-185">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5c5f2-186">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5c5f2-187">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5c5f2-188">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="5c5f2-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5c5f2-189">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5c5f2-190">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5c5f2-191">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="5c5f2-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5c5f2-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5c5f2-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5c5f2-193">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c5f2-193">Remarks</span></span>

<span data-ttu-id="5c5f2-194">La classe **CIM \_ SpareGroup** è derivata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f2-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="5c5f2-195">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-195">WMI does not implement this class.</span></span>

<span data-ttu-id="5c5f2-196">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5c5f2-197">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5c5f2-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c5f2-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c5f2-198">Requirements</span></span>



| <span data-ttu-id="5c5f2-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5f2-199">Requirement</span></span> | <span data-ttu-id="5c5f2-200">Valore</span><span class="sxs-lookup"><span data-stu-id="5c5f2-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5f2-201">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c5f2-201">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5f2-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c5f2-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c5f2-203">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c5f2-203">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5f2-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c5f2-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c5f2-205">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c5f2-205">Namespace</span></span><br/>                | <span data-ttu-id="5c5f2-206">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5c5f2-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c5f2-207">MOF</span><span class="sxs-lookup"><span data-stu-id="5c5f2-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c5f2-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c5f2-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c5f2-209">DLL</span><span class="sxs-lookup"><span data-stu-id="5c5f2-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c5f2-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c5f2-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c5f2-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c5f2-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5f2-212">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="5c5f2-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 


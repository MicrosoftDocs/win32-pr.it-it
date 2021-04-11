---
description: La \_ classe CIM ExtraCapacityGroup è derivata da un gruppo di ridondanza che indica che gli elementi aggregati hanno una capacità o una capacità superiore a quella necessaria.
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: Classe CIM_ExtraCapacityGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225686"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="efc4c-103">CIM \_ ExtraCapacityGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="efc4c-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="efc4c-104">La classe **CIM \_ ExtraCapacityGroup** è derivata da un gruppo di ridondanza che indica che gli elementi aggregati hanno una capacità o una capacità superiore a quella necessaria.</span><span class="sxs-lookup"><span data-stu-id="efc4c-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="efc4c-105">Un esempio di questo tipo di ridondanza è l'installazione di N + 1 alimentatori o ventilatori in un sistema.</span><span class="sxs-lookup"><span data-stu-id="efc4c-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efc4c-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="efc4c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="efc4c-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="efc4c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="efc4c-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="efc4c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="efc4c-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="efc4c-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc4c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efc4c-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="efc4c-111">Members</span><span class="sxs-lookup"><span data-stu-id="efc4c-111">Members</span></span>

<span data-ttu-id="efc4c-112">La classe **CIM \_ ExtraCapacityGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="efc4c-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="efc4c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efc4c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efc4c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efc4c-114">Properties</span></span>

<span data-ttu-id="efc4c-115">La classe **CIM \_ ExtraCapacityGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="efc4c-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efc4c-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="efc4c-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efc4c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="efc4c-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-120">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="efc4c-120">A short textual description of the object.</span></span>

<span data-ttu-id="efc4c-121">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efc4c-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="efc4c-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efc4c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-125">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="efc4c-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-126">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="efc4c-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="efc4c-127">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="efc4c-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="efc4c-128">Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="efc4c-129">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="efc4c-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efc4c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-132">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="efc4c-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-133">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="efc4c-133">A textual description of the object.</span></span>

<span data-ttu-id="efc4c-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efc4c-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="efc4c-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-136">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="efc4c-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="efc4c-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-139">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="efc4c-139">Indicates when the object was installed.</span></span> <span data-ttu-id="efc4c-140">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="efc4c-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="efc4c-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efc4c-142">**MinNumberNeeded**</span><span class="sxs-lookup"><span data-stu-id="efc4c-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efc4c-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-145">Numero più piccolo di elementi che devono essere operativi per la ridondanza.</span><span class="sxs-lookup"><span data-stu-id="efc4c-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="efc4c-146">Ad esempio, in una relazione di ridondanza N + 1, questa proprietà deve essere impostata su N.</span><span class="sxs-lookup"><span data-stu-id="efc4c-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="efc4c-147">**Nome**</span><span class="sxs-lookup"><span data-stu-id="efc4c-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efc4c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-150">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="efc4c-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-151">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="efc4c-151">Label by which the object is known.</span></span> <span data-ttu-id="efc4c-152">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="efc4c-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="efc4c-153">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="efc4c-154">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="efc4c-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efc4c-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-157">Informazioni sullo stato del gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="efc4c-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="efc4c-158">Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efc4c-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efc4c-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="efc4c-160">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="efc4c-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="efc4c-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="efc4c-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="efc4c-162">Altro.</span><span class="sxs-lookup"><span data-stu-id="efc4c-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="efc4c-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Completamente ridondante** (2)</span><span class="sxs-lookup"><span data-stu-id="efc4c-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="efc4c-164">È disponibile tutta la ridondanza configurata.</span><span class="sxs-lookup"><span data-stu-id="efc4c-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="efc4c-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Ridondanza danneggiata** (3)</span><span class="sxs-lookup"><span data-stu-id="efc4c-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="efc4c-166">È disponibile una minore quantità di ridondanza a causa di alcuni errori.</span><span class="sxs-lookup"><span data-stu-id="efc4c-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="efc4c-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Ridondanza persa** (4)</span><span class="sxs-lookup"><span data-stu-id="efc4c-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="efc4c-168">La ridondanza non è disponibile a causa di un numero sufficiente di errori.</span><span class="sxs-lookup"><span data-stu-id="efc4c-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="efc4c-169">L'errore successivo provocherà un errore generale.</span><span class="sxs-lookup"><span data-stu-id="efc4c-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="efc4c-170">**Status**</span><span class="sxs-lookup"><span data-stu-id="efc4c-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc4c-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efc4c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efc4c-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efc4c-173">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="efc4c-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="efc4c-174">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="efc4c-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="efc4c-175">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="efc4c-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="efc4c-176">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="efc4c-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="efc4c-177">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="efc4c-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="efc4c-178">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="efc4c-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="efc4c-179">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="efc4c-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="efc4c-180">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="efc4c-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="efc4c-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="efc4c-182">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="efc4c-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="efc4c-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="efc4c-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="efc4c-184">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="efc4c-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="efc4c-185">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="efc4c-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efc4c-186">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="efc4c-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="efc4c-187">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="efc4c-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="efc4c-188">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="efc4c-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="efc4c-189">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="efc4c-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="efc4c-190">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="efc4c-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="efc4c-191">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="efc4c-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="efc4c-192">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="efc4c-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="efc4c-193">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="efc4c-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="efc4c-194">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="efc4c-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="efc4c-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="efc4c-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="efc4c-196">Commenti</span><span class="sxs-lookup"><span data-stu-id="efc4c-196">Remarks</span></span>

<span data-ttu-id="efc4c-197">La classe **CIM \_ ExtraCapacityGroup** è derivata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="efc4c-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="efc4c-198">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="efc4c-198">WMI does not implement this class.</span></span>

<span data-ttu-id="efc4c-199">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="efc4c-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="efc4c-200">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="efc4c-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc4c-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efc4c-201">Requirements</span></span>



| <span data-ttu-id="efc4c-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc4c-202">Requirement</span></span> | <span data-ttu-id="efc4c-203">Valore</span><span class="sxs-lookup"><span data-stu-id="efc4c-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efc4c-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc4c-204">Minimum supported client</span></span><br/> | <span data-ttu-id="efc4c-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efc4c-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efc4c-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc4c-206">Minimum supported server</span></span><br/> | <span data-ttu-id="efc4c-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efc4c-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efc4c-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="efc4c-208">Namespace</span></span><br/>                | <span data-ttu-id="efc4c-209">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="efc4c-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="efc4c-210">MOF</span><span class="sxs-lookup"><span data-stu-id="efc4c-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efc4c-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efc4c-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="efc4c-212">DLL</span><span class="sxs-lookup"><span data-stu-id="efc4c-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efc4c-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efc4c-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc4c-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efc4c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc4c-215">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="efc4c-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 


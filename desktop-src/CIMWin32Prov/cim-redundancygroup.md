---
description: La \_ classe CIM RedundancyGroup rappresenta una raccolta di elementi di sistema gestiti, che indica che i componenti aggregati, insieme, forniscono la ridondanza.
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: Classe CIM_RedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877289"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="6e31d-103">CIM \_ RedundancyGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="6e31d-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="6e31d-104">La classe **CIM \_ RedundancyGroup** rappresenta una raccolta di elementi di sistema gestiti, che indica che i componenti aggregati, insieme, forniscono la ridondanza.</span><span class="sxs-lookup"><span data-stu-id="6e31d-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="6e31d-105">Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="6e31d-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e31d-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6e31d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6e31d-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6e31d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6e31d-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6e31d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6e31d-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6e31d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e31d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e31d-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="6e31d-111">Members</span><span class="sxs-lookup"><span data-stu-id="6e31d-111">Members</span></span>

<span data-ttu-id="6e31d-112">La classe **CIM \_ RedundancyGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6e31d-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="6e31d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6e31d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e31d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6e31d-114">Properties</span></span>

<span data-ttu-id="6e31d-115">La classe **CIM \_ RedundancyGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6e31d-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e31d-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="6e31d-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6e31d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6e31d-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-120">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6e31d-120">A short textual description of the object.</span></span>

<span data-ttu-id="6e31d-121">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e31d-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e31d-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6e31d-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6e31d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-125">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6e31d-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-126">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="6e31d-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6e31d-127">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="6e31d-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="6e31d-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6e31d-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6e31d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-131">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6e31d-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-132">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6e31d-132">A textual description of the object.</span></span>

<span data-ttu-id="6e31d-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e31d-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e31d-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6e31d-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-135">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e31d-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-137">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="6e31d-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-138">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="6e31d-138">Indicates when the object was installed.</span></span> <span data-ttu-id="6e31d-139">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="6e31d-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6e31d-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e31d-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e31d-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6e31d-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6e31d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-144">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6e31d-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-145">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="6e31d-145">Label by which the object is known.</span></span> <span data-ttu-id="6e31d-146">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="6e31d-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6e31d-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e31d-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e31d-148">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="6e31d-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e31d-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-151">Informazioni sullo stato del gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="6e31d-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e31d-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6e31d-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6e31d-153">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6e31d-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6e31d-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6e31d-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6e31d-155">Altro.</span><span class="sxs-lookup"><span data-stu-id="6e31d-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="6e31d-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Completamente ridondante** (2)</span><span class="sxs-lookup"><span data-stu-id="6e31d-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6e31d-157">È disponibile tutta la ridondanza configurata.</span><span class="sxs-lookup"><span data-stu-id="6e31d-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="6e31d-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Ridondanza danneggiata** (3)</span><span class="sxs-lookup"><span data-stu-id="6e31d-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6e31d-159">È disponibile una minore quantità di ridondanza a causa di alcuni errori.</span><span class="sxs-lookup"><span data-stu-id="6e31d-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="6e31d-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Ridondanza persa** (4)</span><span class="sxs-lookup"><span data-stu-id="6e31d-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6e31d-161">La ridondanza non è disponibile a causa di un numero sufficiente di errori.</span><span class="sxs-lookup"><span data-stu-id="6e31d-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="6e31d-162">L'errore successivo provocherà un errore generale.</span><span class="sxs-lookup"><span data-stu-id="6e31d-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6e31d-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="6e31d-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e31d-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6e31d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6e31d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e31d-166">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6e31d-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6e31d-167">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6e31d-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="6e31d-168">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="6e31d-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6e31d-169">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="6e31d-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6e31d-170">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="6e31d-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6e31d-171">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="6e31d-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6e31d-172">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="6e31d-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6e31d-173">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="6e31d-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6e31d-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e31d-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6e31d-175">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e31d-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6e31d-176">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6e31d-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6e31d-177">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="6e31d-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6e31d-178">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="6e31d-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e31d-179">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="6e31d-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6e31d-180">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="6e31d-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6e31d-181">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="6e31d-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6e31d-182">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="6e31d-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6e31d-183">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="6e31d-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6e31d-184">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="6e31d-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6e31d-185">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="6e31d-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6e31d-186">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="6e31d-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6e31d-187">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="6e31d-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6e31d-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6e31d-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6e31d-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e31d-189">Remarks</span></span>

<span data-ttu-id="6e31d-190">La classe **CIM \_ RedundancyGroup** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e31d-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="6e31d-191">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6e31d-191">WMI does not implement this class.</span></span>

<span data-ttu-id="6e31d-192">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6e31d-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6e31d-193">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6e31d-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e31d-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e31d-194">Requirements</span></span>



| <span data-ttu-id="6e31d-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e31d-195">Requirement</span></span> | <span data-ttu-id="6e31d-196">Valore</span><span class="sxs-lookup"><span data-stu-id="6e31d-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e31d-197">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e31d-197">Minimum supported client</span></span><br/> | <span data-ttu-id="6e31d-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e31d-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e31d-199">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e31d-199">Minimum supported server</span></span><br/> | <span data-ttu-id="6e31d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e31d-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e31d-201">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e31d-201">Namespace</span></span><br/>                | <span data-ttu-id="6e31d-202">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6e31d-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e31d-203">MOF</span><span class="sxs-lookup"><span data-stu-id="6e31d-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e31d-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e31d-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e31d-205">DLL</span><span class="sxs-lookup"><span data-stu-id="6e31d-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e31d-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e31d-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e31d-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e31d-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e31d-208">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="6e31d-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 


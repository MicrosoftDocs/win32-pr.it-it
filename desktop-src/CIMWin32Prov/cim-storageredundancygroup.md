---
description: La \_ classe CIM StorageRedundancyGroup rappresenta informazioni di ridondanza relative all'archiviazione di massa.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: Classe CIM_StorageRedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304484"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="c6fa8-103">CIM \_ StorageRedundancyGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="c6fa8-104">La classe **CIM \_ StorageRedundancyGroup** rappresenta informazioni di ridondanza relative all'archiviazione di massa.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="c6fa8-105">I gruppi di ridondanza di archiviazione vengono usati per proteggere i dati utente.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="c6fa8-106">Sono costituiti da uno o più extent fisici o da uno o più extent fisici aggregati.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="c6fa8-107">I gruppi di ridondanza dell'archiviazione possono sovrapporsi; Tuttavia, gli extent sottostanti all'interno della sovrapposizione non devono contenere dati di controllo.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6fa8-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c6fa8-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c6fa8-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c6fa8-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6fa8-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6fa8-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="c6fa8-113">Members</span><span class="sxs-lookup"><span data-stu-id="c6fa8-113">Members</span></span>

<span data-ttu-id="c6fa8-114">La classe **CIM \_ StorageRedundancyGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6fa8-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="c6fa8-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6fa8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6fa8-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6fa8-116">Properties</span></span>

<span data-ttu-id="c6fa8-117">La classe **CIM \_ StorageRedundancyGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6fa8-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-122">A short textual description of the object.</span></span>

<span data-ttu-id="c6fa8-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6fa8-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-127">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-128">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c6fa8-129">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c6fa8-130">Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6fa8-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-134">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-135">A textual description of the object.</span></span>

<span data-ttu-id="c6fa8-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6fa8-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-141">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-141">Indicates when the object was installed.</span></span> <span data-ttu-id="c6fa8-142">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c6fa8-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6fa8-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-147">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-148">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-148">Label by which the object is known.</span></span> <span data-ttu-id="c6fa8-149">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c6fa8-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6fa8-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-152">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-154">Informazioni sullo stato del gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="c6fa8-155">Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6fa8-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c6fa8-157">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6fa8-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c6fa8-159">Altro.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="c6fa8-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Completamente ridondante** (2)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c6fa8-161">È disponibile tutta la ridondanza configurata.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="c6fa8-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Ridondanza danneggiata** (3)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c6fa8-163">È disponibile una minore quantità di ridondanza a causa di alcuni errori.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="c6fa8-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Ridondanza persa** (4)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c6fa8-165">La ridondanza non è disponibile a causa di un numero sufficiente di errori.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="c6fa8-166">L'errore successivo provocherà un errore generale.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c6fa8-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-170">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-171">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="c6fa8-172">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c6fa8-173">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="c6fa8-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c6fa8-174">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c6fa8-175">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c6fa8-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c6fa8-176">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c6fa8-177">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c6fa8-178">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c6fa8-179">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6fa8-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c6fa8-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c6fa8-181">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c6fa8-182">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="c6fa8-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6fa8-183">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c6fa8-184">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c6fa8-185">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c6fa8-186">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c6fa8-187">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c6fa8-188">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c6fa8-189">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c6fa8-190">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c6fa8-191">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c6fa8-192">**TypeOfAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6fa8-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6fa8-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6fa8-195">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Gruppo di ridondanza DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c6fa8-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c6fa8-196">Algoritmo utilizzato per la ridondanza e la ricostruzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="c6fa8-197">Il valore 0 non è valido nello schema CIM perché rappresenta che non esiste alcuna ridondanza in DMI.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="c6fa8-198">In tal caso, non è necessario creare un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c6fa8-199">**Non definito** (0)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6fa8-200">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6fa8-201">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="c6fa8-202">**Copia** (3)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="c6fa8-203">**Xor** (4)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="c6fa8-204">**P + Q** (5)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="c6fa8-205">**S** (6)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="c6fa8-206">**P + S** (7)</span><span class="sxs-lookup"><span data-stu-id="c6fa8-206">**P+S** (7)</span></span>


<span data-ttu-id="c6fa8-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c6fa8-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c6fa8-208">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6fa8-208">Remarks</span></span>

<span data-ttu-id="c6fa8-209">La classe **CIM \_ StorageRedundancyGroup** è derivata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="c6fa8-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="c6fa8-210">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-210">WMI does not implement this class.</span></span>

<span data-ttu-id="c6fa8-211">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6fa8-212">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c6fa8-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6fa8-213">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6fa8-213">Requirements</span></span>



| <span data-ttu-id="c6fa8-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6fa8-214">Requirement</span></span> | <span data-ttu-id="c6fa8-215">Valore</span><span class="sxs-lookup"><span data-stu-id="c6fa8-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fa8-216">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6fa8-216">Minimum supported client</span></span><br/> | <span data-ttu-id="c6fa8-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6fa8-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6fa8-218">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6fa8-218">Minimum supported server</span></span><br/> | <span data-ttu-id="c6fa8-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6fa8-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6fa8-220">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6fa8-220">Namespace</span></span><br/>                | <span data-ttu-id="c6fa8-221">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c6fa8-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6fa8-222">MOF</span><span class="sxs-lookup"><span data-stu-id="c6fa8-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6fa8-223"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6fa8-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6fa8-224">DLL</span><span class="sxs-lookup"><span data-stu-id="c6fa8-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6fa8-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6fa8-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6fa8-226">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6fa8-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fa8-227">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="c6fa8-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 


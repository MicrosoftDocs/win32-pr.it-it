---
description: La \_ classe CIM MemoryMappedIO rappresenta l'I/O mappato alla memoria dell'architettura del computer. Questa classe indirizza le risorse di memoria e di I/O della porta.
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: Classe CIM_MemoryMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049230"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="31f32-104">CIM \_ MemoryMappedIO (classe)</span><span class="sxs-lookup"><span data-stu-id="31f32-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="31f32-105">La classe **CIM \_ MemoryMappedIO** rappresenta l'I/O mappato alla memoria dell'architettura del computer.</span><span class="sxs-lookup"><span data-stu-id="31f32-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="31f32-106">Questa classe indirizza le risorse di memoria e di I/O della porta.</span><span class="sxs-lookup"><span data-stu-id="31f32-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31f32-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="31f32-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31f32-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31f32-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31f32-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="31f32-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="31f32-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="31f32-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f32-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31f32-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="31f32-112">Members</span><span class="sxs-lookup"><span data-stu-id="31f32-112">Members</span></span>

<span data-ttu-id="31f32-113">La classe **CIM \_ MemoryMappedIO** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="31f32-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="31f32-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31f32-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31f32-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31f32-115">Properties</span></span>

<span data-ttu-id="31f32-116">La classe **CIM \_ MemoryMappedIO** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="31f32-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31f32-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="31f32-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="31f32-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31f32-121">A short textual description of the object.</span></span>

<span data-ttu-id="31f32-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31f32-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-126">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31f32-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31f32-127">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="31f32-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="31f32-128">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="31f32-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31f32-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-132">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="31f32-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="31f32-133">Proprietà **CreationClassName** dell'ambito del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="31f32-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="31f32-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-137">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31f32-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31f32-138">Proprietà del **nome** del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="31f32-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="31f32-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="31f32-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-142">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="31f32-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-143">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31f32-143">A textual description of the object.</span></span>

<span data-ttu-id="31f32-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-145">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="31f32-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-146">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="31f32-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|I/O con mapping della memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="31f32-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-149">Indirizzo finale dell'I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="31f32-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="31f32-150">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="31f32-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31f32-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-152">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31f32-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-154">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="31f32-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-155">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="31f32-155">Indicates when the object was installed.</span></span> <span data-ttu-id="31f32-156">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="31f32-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="31f32-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="31f32-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-161">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="31f32-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-162">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="31f32-162">Label by which the object is known.</span></span> <span data-ttu-id="31f32-163">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="31f32-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="31f32-164">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-165">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="31f32-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-166">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="31f32-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-168">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|I/O con mapping della memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="31f32-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-169">Indirizzo iniziale di I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="31f32-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="31f32-170">La proprietà dell'identificatore di risorsa hardware deve essere impostata su questo valore per costruire la chiave di risorsa I/O mappata.</span><span class="sxs-lookup"><span data-stu-id="31f32-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="31f32-171">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="31f32-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="31f32-172">**Status**</span><span class="sxs-lookup"><span data-stu-id="31f32-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f32-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31f32-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f32-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f32-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31f32-175">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="31f32-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="31f32-176">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31f32-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="31f32-177">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="31f32-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="31f32-178">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="31f32-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="31f32-179">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="31f32-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="31f32-180">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="31f32-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="31f32-181">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="31f32-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="31f32-182">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="31f32-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="31f32-183">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="31f32-184">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="31f32-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="31f32-185">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="31f32-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="31f32-186">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="31f32-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31f32-187">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="31f32-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31f32-188">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="31f32-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="31f32-189">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="31f32-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="31f32-190">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="31f32-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="31f32-191">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="31f32-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="31f32-192">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="31f32-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="31f32-193">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="31f32-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="31f32-194">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="31f32-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="31f32-195">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="31f32-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="31f32-196">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="31f32-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="31f32-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="31f32-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="31f32-198">Commenti</span><span class="sxs-lookup"><span data-stu-id="31f32-198">Remarks</span></span>

<span data-ttu-id="31f32-199">La classe **CIM \_ MemoryMappedIO** è derivata da [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="31f32-200">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="31f32-200">WMI does not implement this class.</span></span> <span data-ttu-id="31f32-201">Per le classi derivate da **CIM \_ MemoryMappedIO**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="31f32-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="31f32-202">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="31f32-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31f32-203">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="31f32-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31f32-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31f32-204">Requirements</span></span>



| <span data-ttu-id="31f32-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f32-205">Requirement</span></span> | <span data-ttu-id="31f32-206">Valore</span><span class="sxs-lookup"><span data-stu-id="31f32-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31f32-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31f32-207">Minimum supported client</span></span><br/> | <span data-ttu-id="31f32-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31f32-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31f32-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31f32-209">Minimum supported server</span></span><br/> | <span data-ttu-id="31f32-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31f32-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31f32-211">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31f32-211">Namespace</span></span><br/>                | <span data-ttu-id="31f32-212">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="31f32-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31f32-213">MOF</span><span class="sxs-lookup"><span data-stu-id="31f32-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31f32-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31f32-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31f32-215">DLL</span><span class="sxs-lookup"><span data-stu-id="31f32-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31f32-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31f32-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f32-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31f32-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f32-218">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="31f32-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 


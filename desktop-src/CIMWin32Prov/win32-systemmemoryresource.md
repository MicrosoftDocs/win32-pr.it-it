---
description: La \_ classe WMI astratta Win32 SystemMemoryResource rappresenta una risorsa di memoria di sistema in un sistema di computer che esegue Windows.
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Classe Win32_SystemMemoryResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878306"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="04d45-103">Win32 \_ SystemMemoryResource (classe)</span><span class="sxs-lookup"><span data-stu-id="04d45-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="04d45-104">La [classe WMI](../wmisdk/retrieving-a-class.md) astratta **Win32 \_ SystemMemoryResource** rappresenta una risorsa di memoria di sistema in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="04d45-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="04d45-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="04d45-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="04d45-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="04d45-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d45-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04d45-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
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

## <a name="members"></a><span data-ttu-id="04d45-108">Members</span><span class="sxs-lookup"><span data-stu-id="04d45-108">Members</span></span>

<span data-ttu-id="04d45-109">La classe **Win32 \_ SystemMemoryResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="04d45-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="04d45-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04d45-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04d45-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04d45-111">Properties</span></span>

<span data-ttu-id="04d45-112">La classe **Win32 \_ SystemMemoryResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="04d45-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04d45-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="04d45-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="04d45-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-117">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="04d45-117">A short textual description of the object.</span></span>

<span data-ttu-id="04d45-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04d45-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-122">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="04d45-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="04d45-123">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="04d45-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="04d45-124">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="04d45-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="04d45-125">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04d45-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-129">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="04d45-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04d45-130">Proprietà **CreationClassName** dell'ambito del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="04d45-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="04d45-131">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="04d45-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-135">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="04d45-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="04d45-136">Proprietà del **nome** del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="04d45-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="04d45-137">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-138">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="04d45-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-141">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="04d45-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-142">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="04d45-142">A textual description of the object.</span></span>

<span data-ttu-id="04d45-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="04d45-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-145">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04d45-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-147">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|I/O con mapping della memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="04d45-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-148">Indirizzo finale dell'I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="04d45-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="04d45-149">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="04d45-150">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="04d45-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-152">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="04d45-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-154">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="04d45-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-155">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="04d45-155">Indicates when the object was installed.</span></span> <span data-ttu-id="04d45-156">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="04d45-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="04d45-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="04d45-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-161">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="04d45-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-162">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="04d45-162">Label by which the object is known.</span></span> <span data-ttu-id="04d45-163">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="04d45-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="04d45-164">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-165">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="04d45-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-166">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04d45-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-168">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|I/O con mapping della memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="04d45-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-169">Indirizzo iniziale di I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="04d45-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="04d45-170">La proprietà dell'identificatore di risorsa hardware deve essere impostata su questo valore per costruire la chiave di risorsa I/O mappata.</span><span class="sxs-lookup"><span data-stu-id="04d45-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="04d45-171">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="04d45-172">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="04d45-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="04d45-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d45-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="04d45-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d45-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04d45-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04d45-176">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="04d45-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="04d45-177">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="04d45-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="04d45-178">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="04d45-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="04d45-179">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="04d45-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="04d45-180">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="04d45-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="04d45-181">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="04d45-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="04d45-182">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="04d45-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="04d45-183">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="04d45-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="04d45-184">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="04d45-185">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="04d45-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="04d45-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="04d45-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="04d45-187">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="04d45-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="04d45-188">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="04d45-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04d45-189">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="04d45-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="04d45-190">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="04d45-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="04d45-191">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="04d45-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="04d45-192">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="04d45-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="04d45-193">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="04d45-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="04d45-194">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="04d45-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="04d45-195">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="04d45-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="04d45-196">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="04d45-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="04d45-197">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="04d45-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="04d45-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="04d45-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="04d45-199">Commenti</span><span class="sxs-lookup"><span data-stu-id="04d45-199">Remarks</span></span>

<span data-ttu-id="04d45-200">La classe **Win32 \_ SystemMemoryResource** è derivata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="04d45-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04d45-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04d45-201">Requirements</span></span>



| <span data-ttu-id="04d45-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d45-202">Requirement</span></span> | <span data-ttu-id="04d45-203">Valore</span><span class="sxs-lookup"><span data-stu-id="04d45-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04d45-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04d45-204">Minimum supported client</span></span><br/> | <span data-ttu-id="04d45-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04d45-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04d45-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04d45-206">Minimum supported server</span></span><br/> | <span data-ttu-id="04d45-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04d45-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04d45-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="04d45-208">Namespace</span></span><br/>                | <span data-ttu-id="04d45-209">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="04d45-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04d45-210">MOF</span><span class="sxs-lookup"><span data-stu-id="04d45-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04d45-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04d45-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04d45-212">DLL</span><span class="sxs-lookup"><span data-stu-id="04d45-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d45-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d45-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d45-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04d45-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d45-215">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="04d45-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="04d45-216">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="04d45-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

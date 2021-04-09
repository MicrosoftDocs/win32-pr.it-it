---
description: La \_ classe WMI DeviceMemoryAddress Win32 rappresenta un indirizzo di memoria del dispositivo in un sistema di computer che esegue Windows.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Classe Win32_DeviceMemoryAddress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966265"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="c457f-103">Win32 \_ DeviceMemoryAddress (classe)</span><span class="sxs-lookup"><span data-stu-id="c457f-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="c457f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceMemoryAddress Win32** rappresenta un indirizzo di memoria del dispositivo in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="c457f-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="c457f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c457f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c457f-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c457f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c457f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c457f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="c457f-108">Members</span><span class="sxs-lookup"><span data-stu-id="c457f-108">Members</span></span>

<span data-ttu-id="c457f-109">La classe **Win32 \_ DeviceMemoryAddress** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c457f-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="c457f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c457f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c457f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c457f-111">Properties</span></span>

<span data-ttu-id="c457f-112">La classe **Win32 \_ DeviceMemoryAddress** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c457f-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c457f-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c457f-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c457f-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-117">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="c457f-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="c457f-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c457f-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c457f-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c457f-123">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="c457f-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c457f-124">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="c457f-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="c457f-125">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c457f-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-129">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c457f-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c457f-130">Nome della classe di creazione dell'ambito del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="c457f-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="c457f-131">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c457f-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-135">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c457f-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c457f-136">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="c457f-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="c457f-137">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-138">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c457f-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-141">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c457f-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-142">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c457f-142">Description of the object.</span></span>

<span data-ttu-id="c457f-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="c457f-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-145">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c457f-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-147">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|I/O con mapping della memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c457f-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-148">Indirizzo finale dell'I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="c457f-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="c457f-149">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="c457f-150">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c457f-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c457f-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-152">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c457f-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-154">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="c457f-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-155">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c457f-155">Date and time the object was installed.</span></span> <span data-ttu-id="c457f-156">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="c457f-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c457f-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-158">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="c457f-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-161">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| flag di \| \_ descrittore di risorse parziali Win32API SystemStructures cm \_ \_ \| ")</span><span class="sxs-lookup"><span data-stu-id="c457f-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-162">Caratteristiche della risorsa di memoria nel computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="c457f-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="c457f-163">I valori sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="c457f-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="c457f-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span><span class="sxs-lookup"><span data-stu-id="c457f-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-165">La memoria può essere letta e scritta.</span><span class="sxs-lookup"><span data-stu-id="c457f-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="c457f-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span><span class="sxs-lookup"><span data-stu-id="c457f-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-167">La memoria è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c457f-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="c457f-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span><span class="sxs-lookup"><span data-stu-id="c457f-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-169">La memoria può essere scritta solo.</span><span class="sxs-lookup"><span data-stu-id="c457f-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="c457f-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prerecuperabile** ("Prefetchable")</span><span class="sxs-lookup"><span data-stu-id="c457f-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-171">Un blocco di memoria viene copiato dalla memoria principale in un buffer di piccole dimensioni gestito dal chipset di memoria.</span><span class="sxs-lookup"><span data-stu-id="c457f-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="c457f-172">Le operazioni di lettura ripetute dalla stessa parte della memoria sono più veloci con la memoria prerecuperabile.</span><span class="sxs-lookup"><span data-stu-id="c457f-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="c457f-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span><span class="sxs-lookup"><span data-stu-id="c457f-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-174">TBD</span><span class="sxs-lookup"><span data-stu-id="c457f-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="c457f-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span><span class="sxs-lookup"><span data-stu-id="c457f-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-176">TBD</span><span class="sxs-lookup"><span data-stu-id="c457f-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="c457f-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Memorizzabile nella cache** ("memorizzabile nella cache")</span><span class="sxs-lookup"><span data-stu-id="c457f-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-178">TBD</span><span class="sxs-lookup"><span data-stu-id="c457f-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="c457f-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span><span class="sxs-lookup"><span data-stu-id="c457f-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-180">TBD</span><span class="sxs-lookup"><span data-stu-id="c457f-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="c457f-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Barra** ("barra")</span><span class="sxs-lookup"><span data-stu-id="c457f-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="c457f-182">TBD</span><span class="sxs-lookup"><span data-stu-id="c457f-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c457f-183">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c457f-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-186">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c457f-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-187">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="c457f-187">Label by which the object is known.</span></span> <span data-ttu-id="c457f-188">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="c457f-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c457f-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-190">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="c457f-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-191">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c457f-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-193">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("IndirizzoIniziale"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|I/O con mapping della memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="c457f-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-194">Indirizzo iniziale dell'I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="c457f-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="c457f-195">La proprietà dell'identificatore di risorsa hardware deve essere impostata su questo valore per costruire la chiave di risorsa I/O mappata.</span><span class="sxs-lookup"><span data-stu-id="c457f-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="c457f-196">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="c457f-197">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c457f-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c457f-198">**Status**</span><span class="sxs-lookup"><span data-stu-id="c457f-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c457f-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c457f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c457f-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c457f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c457f-201">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c457f-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c457f-202">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c457f-202">Current status of the object.</span></span> <span data-ttu-id="c457f-203">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="c457f-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c457f-204">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="c457f-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c457f-205">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c457f-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c457f-206">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c457f-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c457f-207">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c457f-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c457f-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c457f-209">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c457f-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c457f-210">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c457f-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c457f-211">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="c457f-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c457f-212">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="c457f-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c457f-213">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c457f-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c457f-214">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="c457f-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c457f-215">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="c457f-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c457f-216">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="c457f-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c457f-217">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="c457f-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c457f-218">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="c457f-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c457f-219">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="c457f-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c457f-220">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="c457f-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c457f-221">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="c457f-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c457f-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c457f-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c457f-223">Commenti</span><span class="sxs-lookup"><span data-stu-id="c457f-223">Remarks</span></span>

<span data-ttu-id="c457f-224">La classe **Win32 \_ DeviceMemoryAddress** è derivata da [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="c457f-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c457f-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c457f-225">Requirements</span></span>



| <span data-ttu-id="c457f-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="c457f-226">Requirement</span></span> | <span data-ttu-id="c457f-227">Valore</span><span class="sxs-lookup"><span data-stu-id="c457f-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c457f-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c457f-228">Minimum supported client</span></span><br/> | <span data-ttu-id="c457f-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c457f-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c457f-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c457f-230">Minimum supported server</span></span><br/> | <span data-ttu-id="c457f-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c457f-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c457f-232">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c457f-232">Namespace</span></span><br/>                | <span data-ttu-id="c457f-233">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c457f-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c457f-234">MOF</span><span class="sxs-lookup"><span data-stu-id="c457f-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c457f-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c457f-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c457f-236">DLL</span><span class="sxs-lookup"><span data-stu-id="c457f-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c457f-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c457f-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c457f-238">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c457f-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c457f-239">**\_SystemMemoryResource Win32**</span><span class="sxs-lookup"><span data-stu-id="c457f-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="c457f-240">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="c457f-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


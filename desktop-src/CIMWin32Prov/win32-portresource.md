---
description: La \_ classe WMI PortResource Win32 rappresenta una porta di I/O in un sistema di computer che esegue Windows.
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Classe Win32_PortResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965979"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="cce65-103">Win32 \_ PortResource (classe)</span><span class="sxs-lookup"><span data-stu-id="cce65-103">Win32\_PortResource class</span></span>

<span data-ttu-id="cce65-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortResource Win32** rappresenta una porta di I/O in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="cce65-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="cce65-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cce65-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cce65-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cce65-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce65-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cce65-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="cce65-108">Members</span><span class="sxs-lookup"><span data-stu-id="cce65-108">Members</span></span>

<span data-ttu-id="cce65-109">La classe **Win32 \_ PortResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cce65-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="cce65-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cce65-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cce65-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cce65-111">Properties</span></span>

<span data-ttu-id="cce65-112">La classe **Win32 \_ PortResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cce65-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cce65-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="cce65-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-114">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cce65-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-116">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Configuration Manager Structures \| \_ informazioni io")</span><span class="sxs-lookup"><span data-stu-id="cce65-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-117">Se **true**, questa istanza rappresenta uno degli intervalli con un alias.</span><span class="sxs-lookup"><span data-stu-id="cce65-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="cce65-118">Se **false**, l'istanza rappresenta un indirizzo di porta di base.</span><span class="sxs-lookup"><span data-stu-id="cce65-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="cce65-119">Un indirizzo di porta di base è un indirizzo di porta predeterminato dedicato a un servizio o un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="cce65-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="cce65-120">Un indirizzo alias di porta è uno a cui un dispositivo risponde come se fosse l'indirizzo effettivo di una porta di I/O.</span><span class="sxs-lookup"><span data-stu-id="cce65-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="cce65-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cce65-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-124">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cce65-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-125">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cce65-125">Short description of the object.</span></span>

<span data-ttu-id="cce65-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-127">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cce65-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-130">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="cce65-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="cce65-131">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="cce65-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="cce65-132">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="cce65-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cce65-133">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-134">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cce65-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-137">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cce65-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cce65-138">Nome della classe di creazione del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="cce65-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="cce65-139">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="cce65-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-143">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="cce65-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="cce65-144">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="cce65-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="cce65-145">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-146">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cce65-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-149">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cce65-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-150">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cce65-150">Description of the object.</span></span>

<span data-ttu-id="cce65-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-152">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="cce65-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-153">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cce65-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-155">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|I/O con mapping della memoria DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="cce65-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-156">Indirizzo finale dell'I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="cce65-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="cce65-157">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="cce65-158">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cce65-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-160">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cce65-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-162">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="cce65-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-163">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cce65-163">Date and time the object was installed.</span></span> <span data-ttu-id="cce65-164">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="cce65-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cce65-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cce65-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-169">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cce65-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-170">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="cce65-170">Label by which the object is known.</span></span> <span data-ttu-id="cce65-171">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="cce65-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="cce65-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-173">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="cce65-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-174">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cce65-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-176">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("IndirizzoIniziale"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|I/O con mapping della memoria DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="cce65-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-177">Indirizzo iniziale di I/O mappato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="cce65-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="cce65-178">La proprietà dell'identificatore di risorsa hardware deve essere impostata su questo valore per costruire la chiave di risorsa I/O mappata.</span><span class="sxs-lookup"><span data-stu-id="cce65-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="cce65-179">Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="cce65-180">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cce65-181">**Status**</span><span class="sxs-lookup"><span data-stu-id="cce65-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cce65-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cce65-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cce65-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cce65-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cce65-184">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="cce65-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cce65-185">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cce65-185">Current status of the object.</span></span> <span data-ttu-id="cce65-186">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="cce65-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cce65-187">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="cce65-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cce65-188">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="cce65-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cce65-189">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="cce65-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cce65-190">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="cce65-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cce65-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cce65-192">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cce65-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cce65-193">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cce65-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cce65-194">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="cce65-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cce65-195">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="cce65-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cce65-196">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="cce65-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cce65-197">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="cce65-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cce65-198">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="cce65-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cce65-199">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="cce65-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cce65-200">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="cce65-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cce65-201">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="cce65-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cce65-202">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="cce65-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cce65-203">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="cce65-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cce65-204">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="cce65-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="cce65-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cce65-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cce65-206">Commenti</span><span class="sxs-lookup"><span data-stu-id="cce65-206">Remarks</span></span>

<span data-ttu-id="cce65-207">La classe **Win32 \_ PortResource** è derivata da [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="cce65-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cce65-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cce65-208">Requirements</span></span>



| <span data-ttu-id="cce65-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce65-209">Requirement</span></span> | <span data-ttu-id="cce65-210">Valore</span><span class="sxs-lookup"><span data-stu-id="cce65-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cce65-211">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cce65-211">Minimum supported client</span></span><br/> | <span data-ttu-id="cce65-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cce65-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cce65-213">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cce65-213">Minimum supported server</span></span><br/> | <span data-ttu-id="cce65-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cce65-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cce65-215">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cce65-215">Namespace</span></span><br/>                | <span data-ttu-id="cce65-216">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cce65-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cce65-217">MOF</span><span class="sxs-lookup"><span data-stu-id="cce65-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cce65-218"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cce65-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cce65-219">DLL</span><span class="sxs-lookup"><span data-stu-id="cce65-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cce65-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cce65-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce65-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cce65-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce65-222">**\_SystemMemoryResource Win32**</span><span class="sxs-lookup"><span data-stu-id="cce65-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="cce65-223">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="cce65-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

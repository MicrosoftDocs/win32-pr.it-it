---
description: La \_ classe CIM OperatingSystem rappresenta un sistema operativo del computer, costituito da software e firmware che rendono utilizzabile l'hardware di un sistema di computer.
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: Classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523745"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="082d2-103">CIM \_ OperatingSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="082d2-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="082d2-104">La classe **CIM \_ OperatingSystem** rappresenta un sistema operativo del computer, costituito da software e firmware che rendono utilizzabile l'hardware di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="082d2-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="082d2-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="082d2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="082d2-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="082d2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="082d2-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="082d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="082d2-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="082d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="082d2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="082d2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="082d2-110">Members</span><span class="sxs-lookup"><span data-stu-id="082d2-110">Members</span></span>

<span data-ttu-id="082d2-111">La classe **CIM \_ OperatingSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="082d2-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="082d2-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="082d2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="082d2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="082d2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="082d2-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="082d2-114">Methods</span></span>

<span data-ttu-id="082d2-115">La classe **CIM \_ OperatingSystem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="082d2-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="082d2-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="082d2-116">Method</span></span>                                                           | <span data-ttu-id="082d2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="082d2-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="082d2-118">**Riavvio**</span><span class="sxs-lookup"><span data-stu-id="082d2-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="082d2-119">Metodo della classe che arresta il sistema del computer e quindi lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="082d2-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="082d2-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="082d2-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="082d2-121">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="082d2-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="082d2-122">Metodo della classe che Scarica programmi e dll nel punto in cui è sicuro disattivare il computer.</span><span class="sxs-lookup"><span data-stu-id="082d2-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="082d2-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="082d2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="082d2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="082d2-124">Properties</span></span>

<span data-ttu-id="082d2-125">La classe **CIM \_ OperatingSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="082d2-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="082d2-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="082d2-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="082d2-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="082d2-130">Short textual description of the object.</span></span>

<span data-ttu-id="082d2-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="082d2-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-135">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="082d2-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="082d2-136">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="082d2-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="082d2-137">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="082d2-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="082d2-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-141">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="082d2-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="082d2-142">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="082d2-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="082d2-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-146">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="082d2-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="082d2-147">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="082d2-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-148">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="082d2-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-149">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="082d2-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-151">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="082d2-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-152">Numero di minuti di offset del sistema operativo rispetto all'ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="082d2-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="082d2-153">Il numero è positivo, negativo o zero.</span><span class="sxs-lookup"><span data-stu-id="082d2-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-154">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="082d2-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-157">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="082d2-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-158">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="082d2-158">Textual description of the object.</span></span>

<span data-ttu-id="082d2-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-160">**Distribuita**</span><span class="sxs-lookup"><span data-stu-id="082d2-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-161">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="082d2-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="082d2-163">Se **true**, il sistema operativo viene distribuito tra più nodi di sistema del computer, che devono essere raggruppati come cluster.</span><span class="sxs-lookup"><span data-stu-id="082d2-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-164">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="082d2-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-165">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-167">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="082d2-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-168">Numero di kilobyte di memoria fisica attualmente inutilizzati e disponibili.</span><span class="sxs-lookup"><span data-stu-id="082d2-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="082d2-169">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-170">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="082d2-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-171">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-173">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Impostazioni memoria \| di sistema 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="082d2-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-174">Numero di kilobyte di cui è possibile eseguire il mapping nei file di paging del sistema operativo senza causare lo swapping di altre pagine. Il valore 0 indica che non sono presenti file di paging.</span><span class="sxs-lookup"><span data-stu-id="082d2-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="082d2-175">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-176">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="082d2-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-177">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-179">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="082d2-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-180">Numero di kilobyte di memoria virtuale attualmente inutilizzata e disponibile.</span><span class="sxs-lookup"><span data-stu-id="082d2-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="082d2-181">Questo può essere calcolato, ad esempio, aggiungendo la quantità di RAM libera alla quantità di spazio di paging disponibile, ovvero aggiungendo le proprietà **FreePhysicalMemory** e **FreeSpaceInPagingFiles** .</span><span class="sxs-lookup"><span data-stu-id="082d2-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="082d2-182">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="082d2-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-184">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="082d2-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-186">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="082d2-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-187">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="082d2-187">Date and time the object was installed.</span></span> <span data-ttu-id="082d2-188">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="082d2-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="082d2-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="082d2-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-191">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="082d2-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="082d2-193">Ora dell'ultimo avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-194">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="082d2-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-195">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="082d2-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-197">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrSystemDate "," MIF. DMTF \| informazioni generali \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="082d2-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-198">Nozione del sistema operativo della data e dell'ora locali del giorno.</span><span class="sxs-lookup"><span data-stu-id="082d2-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-199">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="082d2-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-200">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="082d2-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-202">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="082d2-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-203">Numero massimo di contesti di processo che il sistema operativo può supportare.</span><span class="sxs-lookup"><span data-stu-id="082d2-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="082d2-204">Se non è presente alcun valore massimo fisso, il valore deve essere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="082d2-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="082d2-205">Nei sistemi con un valore massimo fisso, questo oggetto può aiutare a diagnosticare gli errori che si verificano quando viene raggiunto il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="082d2-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="082d2-206">Se è sconosciuto, immettere-1.</span><span class="sxs-lookup"><span data-stu-id="082d2-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-207">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="082d2-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-208">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-210">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="082d2-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-211">Numero massimo di kilobyte di memoria che possono essere allocati a un processo.</span><span class="sxs-lookup"><span data-stu-id="082d2-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="082d2-212">Per i sistemi operativi senza memoria virtuale, questo valore è in genere uguale alla quantità totale di memoria fisica, meno la memoria usata dal BIOS e dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="082d2-213">Per alcuni sistemi operativi, questo valore può essere infinito, nel qual caso è necessario immettere 0.</span><span class="sxs-lookup"><span data-stu-id="082d2-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="082d2-214">In altri casi, questo valore può essere una costante, ad esempio 2 GB o 4 GB.</span><span class="sxs-lookup"><span data-stu-id="082d2-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="082d2-215">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-216">**Nome**</span><span class="sxs-lookup"><span data-stu-id="082d2-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-219">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="082d2-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-220">Chiave di un'istanza del sistema operativo all'interno di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="082d2-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="082d2-221">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-222">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="082d2-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-223">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="082d2-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="082d2-225">Numero di licenze utente per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="082d2-226">Se è illimitato, immettere 0, se sconosciuto, immettere-1.</span><span class="sxs-lookup"><span data-stu-id="082d2-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-227">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="082d2-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-228">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="082d2-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-230">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="082d2-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-231">Numero di contesti di processo attualmente caricati o in esecuzione nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-232">**NumberOfUsers**</span><span class="sxs-lookup"><span data-stu-id="082d2-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-233">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="082d2-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-235">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="082d2-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-236">Numero di sessioni utente per le quali il sistema operativo archivia attualmente le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="082d2-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="082d2-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="082d2-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="082d2-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-240">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="082d2-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-241">Tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="082d2-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="082d2-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="082d2-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="082d2-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="082d2-244"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="082d2-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-245">Mac OS</span><span class="sxs-lookup"><span data-stu-id="082d2-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="082d2-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="082d2-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-247">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="082d2-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="082d2-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="082d2-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="082d2-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="082d2-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="082d2-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="082d2-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="082d2-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="082d2-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-252">Apri VM</span><span class="sxs-lookup"><span data-stu-id="082d2-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="082d2-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="082d2-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="082d2-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="082d2-255"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="082d2-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="082d2-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="082d2-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="082d2-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="082d2-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="082d2-258"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="082d2-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="082d2-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="082d2-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-260">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="082d2-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="082d2-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="082d2-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="082d2-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="082d2-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-263">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="082d2-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="082d2-264"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="082d2-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="082d2-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="082d2-266"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="082d2-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="082d2-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="082d2-268"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="082d2-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="082d2-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="082d2-270"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="082d2-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="082d2-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="082d2-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="082d2-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-273">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="082d2-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="082d2-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="082d2-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="082d2-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="082d2-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="082d2-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="082d2-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="082d2-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="082d2-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="082d2-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="082d2-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="082d2-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="082d2-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="082d2-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="082d2-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="082d2-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="082d2-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="082d2-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="082d2-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="082d2-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="082d2-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="082d2-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="082d2-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="082d2-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="082d2-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-286">Serie A</span><span class="sxs-lookup"><span data-stu-id="082d2-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="082d2-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="082d2-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-288">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="082d2-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="082d2-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="082d2-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-290">NT tandem</span><span class="sxs-lookup"><span data-stu-id="082d2-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="082d2-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="082d2-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="082d2-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="082d2-293"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="082d2-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="082d2-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="082d2-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="082d2-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="082d2-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="082d2-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="082d2-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="082d2-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="082d2-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="082d2-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="082d2-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-299">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="082d2-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="082d2-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="082d2-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="082d2-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="082d2-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="082d2-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="082d2-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="082d2-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="082d2-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="082d2-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="082d2-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="082d2-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="082d2-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="082d2-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="082d2-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="082d2-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="082d2-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="082d2-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="082d2-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="082d2-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="082d2-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="082d2-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="082d2-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="082d2-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="082d2-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="082d2-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="082d2-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="082d2-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="082d2-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="082d2-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="082d2-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="082d2-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="082d2-316">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="082d2-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="082d2-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="082d2-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="082d2-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="082d2-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="082d2-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="082d2-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="082d2-320"><span id="OS_390"></span><span id="os_390"></span>**Sistema operativo/390** (60)</span><span class="sxs-lookup"><span data-stu-id="082d2-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="082d2-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="082d2-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="082d2-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="082d2-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="082d2-323">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="082d2-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-326">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ OperatingSystem**.**OSType**")</span><span class="sxs-lookup"><span data-stu-id="082d2-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-327">Descrive il produttore e il tipo di sistema operativo quando la proprietà **OSType** è impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="082d2-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="082d2-328">Il formato della stringa inserita in **OtherTypeDescription** dovrebbe essere simile a quello delle stringhe dei **valori** definiti per **OSType**.</span><span class="sxs-lookup"><span data-stu-id="082d2-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="082d2-329">Questa proprietà deve essere impostata su null quando **OSType** è un valore diverso da 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="082d2-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-330">**SizeStoredInPagingFiles)**</span><span class="sxs-lookup"><span data-stu-id="082d2-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-331">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-333">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Impostazioni memoria \| di sistema 001,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="082d2-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-334">Numero di kilobyte che possono essere archiviati nei file di paging del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="082d2-335">Questo numero non rappresenta le dimensioni fisiche effettive del file di paging su disco.</span><span class="sxs-lookup"><span data-stu-id="082d2-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="082d2-336">Il valore 0 (zero) indica che non sono presenti file di paging.</span><span class="sxs-lookup"><span data-stu-id="082d2-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="082d2-337">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-338">**Status**</span><span class="sxs-lookup"><span data-stu-id="082d2-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-341">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="082d2-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-342">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="082d2-342">Current status of the object.</span></span>

<span data-ttu-id="082d2-343">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="082d2-344">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="082d2-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="082d2-345">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="082d2-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="082d2-346">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="082d2-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="082d2-347">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="082d2-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="082d2-348">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="082d2-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="082d2-349">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="082d2-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="082d2-350">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="082d2-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="082d2-351">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="082d2-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="082d2-352">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="082d2-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="082d2-353">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="082d2-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="082d2-354">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="082d2-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="082d2-355">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="082d2-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="082d2-356">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="082d2-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="082d2-357">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="082d2-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-358">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-360">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="082d2-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-361">Spazio di swapping totale, in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="082d2-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="082d2-362">Questo valore può essere null (non specificato) se lo spazio di swapping non è distinto dai file di paging.</span><span class="sxs-lookup"><span data-stu-id="082d2-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="082d2-363">Tuttavia, alcuni sistemi operativi distinguono questi concetti.</span><span class="sxs-lookup"><span data-stu-id="082d2-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="082d2-364">Ad esempio, interi processi possono essere "scambiati" in UNIX quando l'elenco di pagine disponibili è inferiore a un importo specificato.</span><span class="sxs-lookup"><span data-stu-id="082d2-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="082d2-365">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-366">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="082d2-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-367">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-369">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="082d2-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-370">Numero di kilobyte di memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="082d2-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="082d2-371">Ad esempio, calcolare questa operazione aggiungendo la quantità di RAM totale alla quantità di spazio di paging (ovvero, aggiungere la quantità di memoria in o aggregata dal sistema del computer alla proprietà **SizeStoredInPagingFiles)** .</span><span class="sxs-lookup"><span data-stu-id="082d2-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="082d2-372">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-373">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="082d2-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-374">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="082d2-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-376">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="082d2-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-377">Quantità totale di memoria fisica, espressa in kilobyte, disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="082d2-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="082d2-378">Questo valore non indica necessariamente la vera quantità di memoria fisica, ma ciò che viene segnalato al sistema operativo come disponibile.</span><span class="sxs-lookup"><span data-stu-id="082d2-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="082d2-379">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="082d2-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="082d2-380">**Versione**</span><span class="sxs-lookup"><span data-stu-id="082d2-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="082d2-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="082d2-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="082d2-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="082d2-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="082d2-383">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operativo DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="082d2-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="082d2-384">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="082d2-384">Version of the operation.</span></span>

<span data-ttu-id="082d2-385">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="082d2-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="082d2-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="082d2-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="082d2-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="082d2-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="082d2-388">Commenti</span><span class="sxs-lookup"><span data-stu-id="082d2-388">Remarks</span></span>

<span data-ttu-id="082d2-389">La classe **CIM \_ OperatingSystem** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="082d2-390">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="082d2-390">WMI does not implement this class.</span></span> <span data-ttu-id="082d2-391">Per le classi WMI derivate da **CIM \_ OperatingSystem**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="082d2-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="082d2-392">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="082d2-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="082d2-393">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="082d2-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="082d2-394">Requisiti</span><span class="sxs-lookup"><span data-stu-id="082d2-394">Requirements</span></span>



| <span data-ttu-id="082d2-395">Requisito</span><span class="sxs-lookup"><span data-stu-id="082d2-395">Requirement</span></span> | <span data-ttu-id="082d2-396">Valore</span><span class="sxs-lookup"><span data-stu-id="082d2-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="082d2-397">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="082d2-397">Minimum supported client</span></span><br/> | <span data-ttu-id="082d2-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="082d2-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="082d2-399">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="082d2-399">Minimum supported server</span></span><br/> | <span data-ttu-id="082d2-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="082d2-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="082d2-401">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="082d2-401">Namespace</span></span><br/>                | <span data-ttu-id="082d2-402">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="082d2-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="082d2-403">MOF</span><span class="sxs-lookup"><span data-stu-id="082d2-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="082d2-404"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="082d2-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="082d2-405">DLL</span><span class="sxs-lookup"><span data-stu-id="082d2-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="082d2-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="082d2-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="082d2-407">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="082d2-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="082d2-408">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="082d2-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 


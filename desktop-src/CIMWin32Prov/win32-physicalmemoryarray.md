---
description: Win32 \_ PhysicalMemoryArray&\# 160; Classe WMI rappresenta i dettagli sulla memoria fisica del sistema del computer. Sono inclusi il numero di dispositivi di memoria, la capacità di memoria disponibile e il tipo di memoria&\# 8212, ad esempio la memoria di sistema o video.
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966360"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="25823-104">Win32 \_ PhysicalMemoryArray (classe)</span><span class="sxs-lookup"><span data-stu-id="25823-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="25823-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemoryArray Win32** rappresenta i dettagli sulla memoria fisica del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="25823-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="25823-106">Sono inclusi il numero di dispositivi di memoria, la capacità di memoria disponibile e il tipo di memoria, ad esempio memoria di sistema o video.</span><span class="sxs-lookup"><span data-stu-id="25823-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="25823-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="25823-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="25823-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="25823-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="25823-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25823-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="25823-110">Members</span><span class="sxs-lookup"><span data-stu-id="25823-110">Members</span></span>

<span data-ttu-id="25823-111">La classe **Win32 \_ PhysicalMemoryArray** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="25823-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="25823-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="25823-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="25823-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25823-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="25823-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="25823-114">Methods</span></span>

<span data-ttu-id="25823-115">La classe **Win32 \_ PhysicalMemoryArray** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="25823-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="25823-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="25823-116">Method</span></span>           | <span data-ttu-id="25823-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25823-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="25823-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="25823-118">**IsCompatible**</span></span> | <span data-ttu-id="25823-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="25823-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="25823-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25823-120">Properties</span></span>

<span data-ttu-id="25823-121">La classe **Win32 \_ PhysicalMemoryArray** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="25823-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25823-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="25823-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-125">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="25823-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="25823-126">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="25823-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="25823-127">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-128">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="25823-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-131">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="25823-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="25823-132">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="25823-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="25823-133">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="25823-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="25823-134">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-135">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="25823-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-136">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="25823-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="25823-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-138">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="25823-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="25823-139">Profondità del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="25823-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="25823-140">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-141">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="25823-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-144">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="25823-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="25823-145">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="25823-145">Description of the object.</span></span>

<span data-ttu-id="25823-146">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-147">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="25823-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-148">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="25823-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="25823-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-150">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="25823-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="25823-151">Altezza del pacchetto fisico, in pollici.</span><span class="sxs-lookup"><span data-stu-id="25823-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="25823-152">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-153">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="25823-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-154">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25823-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25823-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25823-156">Se è **true**, un pacchetto fisico può essere scambiato a caldo (se è possibile sostituire l'elemento con un oggetto fisicamente diverso ma equivalente mentre al pacchetto che lo contiene è stata applicata la potenza, è "on").</span><span class="sxs-lookup"><span data-stu-id="25823-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="25823-157">Ad esempio, un pacchetto di unità disco inserito usando i connettori SCA è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="25823-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="25823-158">Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="25823-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="25823-159">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="25823-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-161">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="25823-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="25823-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-163">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="25823-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="25823-164">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="25823-164">Date and time the object was installed.</span></span> <span data-ttu-id="25823-165">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="25823-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="25823-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-167">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="25823-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25823-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25823-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-170">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 \| location")</span><span class="sxs-lookup"><span data-stu-id="25823-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="25823-171">Posizione fisica della matrice di memoria.</span><span class="sxs-lookup"><span data-stu-id="25823-171">Physical location of the memory array.</span></span>

<span data-ttu-id="25823-172">Questo valore deriva dal membro **location** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="25823-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="25823-173">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="25823-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25823-174">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="25823-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25823-175">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="25823-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="25823-176">Scheda di **sistema o scheda madre** (3)</span><span class="sxs-lookup"><span data-stu-id="25823-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="25823-177">**Scheda componente aggiuntivo ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="25823-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="25823-178">**Scheda componente aggiuntivo EISA** (5)</span><span class="sxs-lookup"><span data-stu-id="25823-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="25823-179">**Scheda componente aggiuntivo PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="25823-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="25823-180">**Scheda componente aggiuntivo MCA** (7)</span><span class="sxs-lookup"><span data-stu-id="25823-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="25823-181">**Scheda componente aggiuntivo PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="25823-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="25823-182">**Scheda componente aggiuntivo proprietaria** (9)</span><span class="sxs-lookup"><span data-stu-id="25823-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="25823-183">**Nubus** (10)</span><span class="sxs-lookup"><span data-stu-id="25823-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="25823-184">**Scheda componente aggiuntivo PC-98/C20** (11)</span><span class="sxs-lookup"><span data-stu-id="25823-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="25823-185">**Scheda componente aggiuntivo PC-98/C24** (12)</span><span class="sxs-lookup"><span data-stu-id="25823-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="25823-186">**Scheda componente aggiuntivo PC-98/E** (13)</span><span class="sxs-lookup"><span data-stu-id="25823-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="25823-187">**Scheda aggiuntivo PC-98/bus locale** (14)</span><span class="sxs-lookup"><span data-stu-id="25823-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25823-188">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="25823-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-191">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="25823-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="25823-192">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="25823-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="25823-193">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="25823-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-195">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25823-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25823-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-197">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 \| capacità massima")</span><span class="sxs-lookup"><span data-stu-id="25823-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="25823-198">In alternativa, usare la proprietà **MaxCapacityEx** .</span><span class="sxs-lookup"><span data-stu-id="25823-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="25823-199">Questo valore deriva dal membro di **capacità massima** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="25823-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="25823-200">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Dimensione massima della memoria (in byte) installabile per questa particolare matrice di memoria.</span><span class="sxs-lookup"><span data-stu-id="25823-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="25823-201">Se la dimensione è sconosciuta, alla proprietà viene assegnato un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="25823-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="25823-202">**MaxCapacityEx**</span><span class="sxs-lookup"><span data-stu-id="25823-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-203">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="25823-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="25823-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-205">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Extended maximum capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="25823-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="25823-206">Dimensione massima della memoria (in kilobyte) installabile per la matrice di memoria specifica.</span><span class="sxs-lookup"><span data-stu-id="25823-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="25823-207">Se la dimensione è sconosciuta, alla proprietà viene assegnato un valore pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="25823-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="25823-208">Questo valore deriva dal membro di **capacità massima estesa** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="25823-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="25823-209">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="25823-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="25823-210">**MemoryDevices**</span><span class="sxs-lookup"><span data-stu-id="25823-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25823-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25823-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-213">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 \| numero di dispositivi di memoria")</span><span class="sxs-lookup"><span data-stu-id="25823-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="25823-214">Numero di slot o socket fisici disponibili in questa matrice di memoria.</span><span class="sxs-lookup"><span data-stu-id="25823-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="25823-215">Questo valore deriva dal **numero di dispositivi di memoria** membro della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="25823-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="25823-216">**MemoryErrorCorrection**</span><span class="sxs-lookup"><span data-stu-id="25823-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-217">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25823-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25823-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-219">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Memory Error Correction")</span><span class="sxs-lookup"><span data-stu-id="25823-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="25823-220">Tipo di correzione di errore utilizzata dalla matrice di memoria.</span><span class="sxs-lookup"><span data-stu-id="25823-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="25823-221">Questo valore deriva dal membro di **correzione degli errori di memoria** della struttura della matrice di **memoria fisica** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="25823-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="25823-222">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="25823-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25823-223">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="25823-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25823-224">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="25823-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="25823-225">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="25823-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="25823-226">**Parità** (4)</span><span class="sxs-lookup"><span data-stu-id="25823-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="25823-227">**Ecc a bit singolo** (5)</span><span class="sxs-lookup"><span data-stu-id="25823-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="25823-228">**Ecc a più bit** (6)</span><span class="sxs-lookup"><span data-stu-id="25823-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="25823-229">**CRC** (7)</span><span class="sxs-lookup"><span data-stu-id="25823-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25823-230">**Modello**</span><span class="sxs-lookup"><span data-stu-id="25823-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-233">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="25823-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="25823-234">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="25823-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="25823-235">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-236">**Nome**</span><span class="sxs-lookup"><span data-stu-id="25823-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-239">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="25823-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="25823-240">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="25823-240">Label by which the object is known.</span></span> <span data-ttu-id="25823-241">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="25823-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="25823-242">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="25823-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25823-246">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="25823-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="25823-247">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="25823-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="25823-248">Si noti che se sono disponibili solo i dati del codice a barre ed è univoco o in grado di essere utilizzati come chiave di elemento, questa proprietà sarà **null** e i dati del codice a barre utilizzati come chiave della classe nella proprietà Tag.</span><span class="sxs-lookup"><span data-stu-id="25823-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="25823-249">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-250">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="25823-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-253">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="25823-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="25823-254">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="25823-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="25823-255">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-256">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="25823-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-257">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25823-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25823-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25823-259">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="25823-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="25823-260">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-261">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="25823-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-262">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25823-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25823-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25823-264">Se il valore è **true**, un pacchetto fisico è rimovibile (se è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti).</span><span class="sxs-lookup"><span data-stu-id="25823-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="25823-265">Un pacchetto può ancora essere rimovibile se l'alimentazione deve essere "off" per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="25823-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="25823-266">Se Power può essere "on" e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="25823-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="25823-267">Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando i connettori SCA.</span><span class="sxs-lookup"><span data-stu-id="25823-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="25823-268">Tuttavia, quest'ultimo può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="25823-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="25823-269">La visualizzazione di un computer portatile non è rimovibile, né è un alimentatore non ridondante.</span><span class="sxs-lookup"><span data-stu-id="25823-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="25823-270">La rimozione di questi componenti influirà sulla funzione della creazione complessiva dei pacchetti o non è possibile grazie alla stretta integrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="25823-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="25823-271">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-272">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="25823-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-273">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25823-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25823-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25823-275">Se **true**, questo componente multimediale fisico può essere sostituito con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="25823-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="25823-276">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="25823-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="25823-277">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="25823-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="25823-278">Un altro esempio è un pacchetto di alimentazione montato sulle guide scorrevoli.</span><span class="sxs-lookup"><span data-stu-id="25823-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="25823-279">Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="25823-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="25823-280">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-281">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="25823-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-284">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="25823-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="25823-285">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="25823-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="25823-286">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-287">**SKU**</span><span class="sxs-lookup"><span data-stu-id="25823-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-290">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="25823-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="25823-291">Numero di unità di stockkeeping per l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="25823-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="25823-292">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-293">**Status**</span><span class="sxs-lookup"><span data-stu-id="25823-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-296">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="25823-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="25823-297">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="25823-297">Current status of the object.</span></span> <span data-ttu-id="25823-298">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="25823-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="25823-299">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="25823-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="25823-300">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="25823-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="25823-301">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="25823-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="25823-302">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="25823-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="25823-303">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="25823-304">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="25823-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="25823-305">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="25823-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="25823-306">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="25823-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="25823-307">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="25823-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25823-308">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="25823-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="25823-309">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="25823-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="25823-310">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="25823-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="25823-311">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="25823-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="25823-312">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="25823-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="25823-313">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="25823-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="25823-314">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="25823-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="25823-315">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="25823-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="25823-316">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="25823-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25823-317">**Tag**</span><span class="sxs-lookup"><span data-stu-id="25823-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-320">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="25823-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="25823-321">Identificatore univoco della matrice di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="25823-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="25823-322">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="25823-323">Esempio: "matrice di memoria fisica 1"</span><span class="sxs-lookup"><span data-stu-id="25823-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="25823-324">**Uso**</span><span class="sxs-lookup"><span data-stu-id="25823-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-325">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25823-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25823-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-327">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| use")</span><span class="sxs-lookup"><span data-stu-id="25823-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="25823-328">Modalità di utilizzo della memoria nel computer.</span><span class="sxs-lookup"><span data-stu-id="25823-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="25823-329">Questo valore deriva dal membro **use** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="25823-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="25823-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="25823-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25823-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="25823-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25823-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="25823-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="25823-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**Memoria di sistema** (3)</span><span class="sxs-lookup"><span data-stu-id="25823-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="25823-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Memoria video** (4)</span><span class="sxs-lookup"><span data-stu-id="25823-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="25823-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Memoria flash** (5)</span><span class="sxs-lookup"><span data-stu-id="25823-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="25823-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**RAM non volatile** (6)</span><span class="sxs-lookup"><span data-stu-id="25823-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="25823-337">RAM non volatile</span><span class="sxs-lookup"><span data-stu-id="25823-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="25823-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Memoria cache** (7)</span><span class="sxs-lookup"><span data-stu-id="25823-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25823-339">**Versione**</span><span class="sxs-lookup"><span data-stu-id="25823-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25823-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25823-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-342">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="25823-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="25823-343">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="25823-343">Version of the physical element.</span></span>

<span data-ttu-id="25823-344">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="25823-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-345">**Weight**</span><span class="sxs-lookup"><span data-stu-id="25823-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-346">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="25823-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="25823-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-348">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("libbre")</span><span class="sxs-lookup"><span data-stu-id="25823-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="25823-349">Peso del pacchetto fisico in sterline.</span><span class="sxs-lookup"><span data-stu-id="25823-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="25823-350">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="25823-351">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="25823-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25823-352">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="25823-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="25823-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25823-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25823-354">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="25823-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="25823-355">Larghezza del pacchetto fisico in pollici.</span><span class="sxs-lookup"><span data-stu-id="25823-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="25823-356">Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25823-357">Commenti</span><span class="sxs-lookup"><span data-stu-id="25823-357">Remarks</span></span>

<span data-ttu-id="25823-358">La classe **Win32 \_ PhysicalMemoryArray** è derivata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="25823-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="25823-359">Esempio</span><span class="sxs-lookup"><span data-stu-id="25823-359">Examples</span></span>

<span data-ttu-id="25823-360">L'esempio di PowerShell seguente recupera il numero di slot di memoria e la quantità di memoria installata in un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="25823-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="25823-361">Nell'esempio di codice VBScript seguente vengono restituite informazioni sulla memoria fisica installata in un computer.</span><span class="sxs-lookup"><span data-stu-id="25823-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="25823-362">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25823-362">Requirements</span></span>



| <span data-ttu-id="25823-363">Requisito</span><span class="sxs-lookup"><span data-stu-id="25823-363">Requirement</span></span> | <span data-ttu-id="25823-364">Valore</span><span class="sxs-lookup"><span data-stu-id="25823-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25823-365">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25823-365">Minimum supported client</span></span><br/> | <span data-ttu-id="25823-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25823-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25823-367">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25823-367">Minimum supported server</span></span><br/> | <span data-ttu-id="25823-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25823-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25823-369">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="25823-369">Namespace</span></span><br/>                | <span data-ttu-id="25823-370">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="25823-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25823-371">MOF</span><span class="sxs-lookup"><span data-stu-id="25823-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25823-372"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25823-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25823-373">DLL</span><span class="sxs-lookup"><span data-stu-id="25823-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25823-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25823-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25823-375">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25823-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25823-376">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="25823-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="25823-377">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="25823-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="25823-378">**\_MemoryArrayLocation Win32**</span><span class="sxs-lookup"><span data-stu-id="25823-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 

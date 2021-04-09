---
description: La \_ classe CIM PhysicalMemory rappresenta dispositivi di memoria di basso livello, ad esempio SIMM, DIMM, chip di memoria RAW e così via.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878178"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="59a54-103">CIM \_ PhysicalMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="59a54-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="59a54-104">La classe **CIM \_ PhysicalMemory** rappresenta dispositivi di memoria di basso livello, ad esempio SIMM, DIMM, chip di memoria RAW e così via.</span><span class="sxs-lookup"><span data-stu-id="59a54-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59a54-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="59a54-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="59a54-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="59a54-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="59a54-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="59a54-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="59a54-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="59a54-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a54-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59a54-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="59a54-110">Members</span><span class="sxs-lookup"><span data-stu-id="59a54-110">Members</span></span>

<span data-ttu-id="59a54-111">La classe **CIM \_ PhysicalMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="59a54-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="59a54-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59a54-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59a54-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59a54-113">Properties</span></span>

<span data-ttu-id="59a54-114">La classe **CIM \_ PhysicalMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="59a54-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59a54-115">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="59a54-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| dispositivo di memoria \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="59a54-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-119">Con etichetta Bank in cui si trova la memoria.</span><span class="sxs-lookup"><span data-stu-id="59a54-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="59a54-120">Ad esempio, "Bank 0" o "Bank A".</span><span class="sxs-lookup"><span data-stu-id="59a54-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="59a54-121">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="59a54-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-122">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59a54-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-124">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo di memoria DMTF \| 002,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" byte ")</span><span class="sxs-lookup"><span data-stu-id="59a54-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-125">Capacità totale della memoria fisica, in byte.</span><span class="sxs-lookup"><span data-stu-id="59a54-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="59a54-126">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="59a54-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-127">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="59a54-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="59a54-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-131">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="59a54-131">Short textual description of the object.</span></span>

<span data-ttu-id="59a54-132">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="59a54-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-136">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="59a54-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-137">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="59a54-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="59a54-138">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="59a54-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="59a54-139">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="59a54-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59a54-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo di memoria DMTF \| 002,8 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="59a54-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-144">Larghezza dei dati della memoria fisica, in bit.</span><span class="sxs-lookup"><span data-stu-id="59a54-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="59a54-145">Una larghezza di dati pari a 0 (zero) e una larghezza totale di 8 indica che la memoria viene utilizzata solo per fornire i bit di correzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="59a54-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="59a54-146">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="59a54-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-149">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="59a54-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-150">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="59a54-150">Textual description of the object.</span></span>

<span data-ttu-id="59a54-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-152">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="59a54-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59a54-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-155">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Formfactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| dispositivo di memoria \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="59a54-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-156">Fattore di forma dell'implementazione per il chip.</span><span class="sxs-lookup"><span data-stu-id="59a54-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="59a54-157">È ad esempio possibile specificare valori come SIMM, TSOP o PGA.</span><span class="sxs-lookup"><span data-stu-id="59a54-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="59a54-158">Questa proprietà viene ereditata [**dal \_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="59a54-159">0</span><span class="sxs-lookup"><span data-stu-id="59a54-159">0</span></span>
</dt> <dd>

<span data-ttu-id="59a54-160">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="59a54-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="59a54-161">1</span><span class="sxs-lookup"><span data-stu-id="59a54-161">1</span></span>
</dt> <dd>

<span data-ttu-id="59a54-162">Altro</span><span class="sxs-lookup"><span data-stu-id="59a54-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="59a54-163">2</span><span class="sxs-lookup"><span data-stu-id="59a54-163">2</span></span>
</dt> <dd>

<span data-ttu-id="59a54-164">SIP</span><span class="sxs-lookup"><span data-stu-id="59a54-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-165">3</span><span class="sxs-lookup"><span data-stu-id="59a54-165">3</span></span>
</dt> <dd>

<span data-ttu-id="59a54-166">DIP</span><span class="sxs-lookup"><span data-stu-id="59a54-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-167">4</span><span class="sxs-lookup"><span data-stu-id="59a54-167">4</span></span>
</dt> <dd>

<span data-ttu-id="59a54-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="59a54-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-169">5</span><span class="sxs-lookup"><span data-stu-id="59a54-169">5</span></span>
</dt> <dd>

<span data-ttu-id="59a54-170">SOJ</span><span class="sxs-lookup"><span data-stu-id="59a54-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="59a54-171">6</span><span class="sxs-lookup"><span data-stu-id="59a54-171">6</span></span>
</dt> <dd>

<span data-ttu-id="59a54-172">Proprietario</span><span class="sxs-lookup"><span data-stu-id="59a54-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="59a54-173">7</span><span class="sxs-lookup"><span data-stu-id="59a54-173">7</span></span>
</dt> <dd>

<span data-ttu-id="59a54-174">SIMM</span><span class="sxs-lookup"><span data-stu-id="59a54-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="59a54-175">8</span><span class="sxs-lookup"><span data-stu-id="59a54-175">8</span></span>
</dt> <dd>

<span data-ttu-id="59a54-176">DIMM</span><span class="sxs-lookup"><span data-stu-id="59a54-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="59a54-177">9</span><span class="sxs-lookup"><span data-stu-id="59a54-177">9</span></span>
</dt> <dd>

<span data-ttu-id="59a54-178">TSOP</span><span class="sxs-lookup"><span data-stu-id="59a54-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-179">10</span><span class="sxs-lookup"><span data-stu-id="59a54-179">10</span></span>
</dt> <dd>

<span data-ttu-id="59a54-180">PGA</span><span class="sxs-lookup"><span data-stu-id="59a54-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="59a54-181">11</span><span class="sxs-lookup"><span data-stu-id="59a54-181">11</span></span>
</dt> <dd>

<span data-ttu-id="59a54-182">RIMM</span><span class="sxs-lookup"><span data-stu-id="59a54-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="59a54-183">12</span><span class="sxs-lookup"><span data-stu-id="59a54-183">12</span></span>
</dt> <dd>

<span data-ttu-id="59a54-184">SODIMM</span><span class="sxs-lookup"><span data-stu-id="59a54-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="59a54-185">13</span><span class="sxs-lookup"><span data-stu-id="59a54-185">13</span></span>
</dt> <dd>

<span data-ttu-id="59a54-186">SRIMM</span><span class="sxs-lookup"><span data-stu-id="59a54-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="59a54-187">14</span><span class="sxs-lookup"><span data-stu-id="59a54-187">14</span></span>
</dt> <dd>

<span data-ttu-id="59a54-188">SMD</span><span class="sxs-lookup"><span data-stu-id="59a54-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="59a54-189">15</span><span class="sxs-lookup"><span data-stu-id="59a54-189">15</span></span>
</dt> <dd>

<span data-ttu-id="59a54-190">SSMP</span><span class="sxs-lookup"><span data-stu-id="59a54-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-191">16</span><span class="sxs-lookup"><span data-stu-id="59a54-191">16</span></span>
</dt> <dd>

<span data-ttu-id="59a54-192">QFP</span><span class="sxs-lookup"><span data-stu-id="59a54-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-193">17</span><span class="sxs-lookup"><span data-stu-id="59a54-193">17</span></span>
</dt> <dd>

<span data-ttu-id="59a54-194">TQFP</span><span class="sxs-lookup"><span data-stu-id="59a54-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="59a54-195">18</span><span class="sxs-lookup"><span data-stu-id="59a54-195">18</span></span>
</dt> <dd>

<span data-ttu-id="59a54-196">SOIC</span><span class="sxs-lookup"><span data-stu-id="59a54-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="59a54-197">19</span><span class="sxs-lookup"><span data-stu-id="59a54-197">19</span></span>
</dt> <dd>

<span data-ttu-id="59a54-198">LCC</span><span class="sxs-lookup"><span data-stu-id="59a54-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="59a54-199">20</span><span class="sxs-lookup"><span data-stu-id="59a54-199">20</span></span>
</dt> <dd>

<span data-ttu-id="59a54-200">PLCC</span><span class="sxs-lookup"><span data-stu-id="59a54-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="59a54-201">21</span><span class="sxs-lookup"><span data-stu-id="59a54-201">21</span></span>
</dt> <dd>

<span data-ttu-id="59a54-202">BGA</span><span class="sxs-lookup"><span data-stu-id="59a54-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="59a54-203">22</span><span class="sxs-lookup"><span data-stu-id="59a54-203">22</span></span>
</dt> <dd>

<span data-ttu-id="59a54-204">FPBGA</span><span class="sxs-lookup"><span data-stu-id="59a54-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="59a54-205">23</span><span class="sxs-lookup"><span data-stu-id="59a54-205">23</span></span>
</dt> <dd>

<span data-ttu-id="59a54-206">LGA</span><span class="sxs-lookup"><span data-stu-id="59a54-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="59a54-207">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="59a54-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-208">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="59a54-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59a54-210">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="59a54-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="59a54-211">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="59a54-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="59a54-212">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="59a54-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="59a54-213">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="59a54-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="59a54-214">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="59a54-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-216">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="59a54-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-218">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="59a54-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-219">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="59a54-219">Date and time the object was installed.</span></span> <span data-ttu-id="59a54-220">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="59a54-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="59a54-221">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-222">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="59a54-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-223">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59a54-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-225">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Indirizzi con mapping del dispositivo di memoria DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="59a54-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-226">Posizione della memoria fisica in un interleave.</span><span class="sxs-lookup"><span data-stu-id="59a54-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="59a54-227">Il valore 0 indica che non è Interleaved, 1 indica la prima posizione, 2 indica la seconda posizione e così via.</span><span class="sxs-lookup"><span data-stu-id="59a54-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="59a54-228">Ad esempio, in un'interleave 2:1, un valore pari a 1 indica che la memoria si trova nella posizione uniforme.</span><span class="sxs-lookup"><span data-stu-id="59a54-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="59a54-229">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="59a54-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-232">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="59a54-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-233">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="59a54-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="59a54-234">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="59a54-235">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-236">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="59a54-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59a54-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-239">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| dispositivo di memoria \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="59a54-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-240">Tipo di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="59a54-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="59a54-241">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="59a54-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="59a54-242">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="59a54-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="59a54-243">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="59a54-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="59a54-244">**DRAM sincrona** (3)</span><span class="sxs-lookup"><span data-stu-id="59a54-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="59a54-245">**Memoria DRAM cache** (4)</span><span class="sxs-lookup"><span data-stu-id="59a54-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="59a54-246">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="59a54-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="59a54-247">**Edra** (6)</span><span class="sxs-lookup"><span data-stu-id="59a54-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="59a54-248">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="59a54-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="59a54-249">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="59a54-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="59a54-250">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="59a54-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="59a54-251">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="59a54-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="59a54-252">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="59a54-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="59a54-253">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="59a54-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="59a54-254">**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="59a54-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="59a54-255">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="59a54-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="59a54-256">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="59a54-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="59a54-257">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="59a54-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="59a54-258">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="59a54-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="59a54-259">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="59a54-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="59a54-260">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="59a54-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="59a54-261">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="59a54-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="59a54-262">**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="59a54-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="59a54-263">**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="59a54-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="59a54-264">**Modello**</span><span class="sxs-lookup"><span data-stu-id="59a54-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-265">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-267">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="59a54-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-268">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="59a54-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="59a54-269">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-270">**Nome**</span><span class="sxs-lookup"><span data-stu-id="59a54-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-273">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="59a54-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-274">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="59a54-274">Label by which the object is known.</span></span> <span data-ttu-id="59a54-275">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="59a54-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="59a54-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="59a54-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59a54-280">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="59a54-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="59a54-281">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="59a54-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="59a54-282">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="59a54-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="59a54-283">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-284">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="59a54-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-287">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="59a54-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-288">Numero di parte assegnato dall'organizzazione che ha prodotto o prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="59a54-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="59a54-289">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-290">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="59a54-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-291">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59a54-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-293">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Indirizzi con mapping del dispositivo di memoria DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="59a54-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-294">Posizione della memoria fisica in una riga.</span><span class="sxs-lookup"><span data-stu-id="59a54-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="59a54-295">Se, ad esempio, sono necessari dispositivi di memoria a 2 8 bit per formare una riga a 16 bit, il valore 2 indica che la memoria è il secondo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59a54-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="59a54-296">Il valore 0 non è un valore valido per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="59a54-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="59a54-297">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="59a54-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-298">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="59a54-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59a54-300">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="59a54-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="59a54-301">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-302">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="59a54-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-303">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="59a54-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59a54-305">Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="59a54-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="59a54-306">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="59a54-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="59a54-307">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="59a54-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="59a54-308">Ad esempio, un chip del processore non aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="59a54-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="59a54-309">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-310">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="59a54-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-311">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="59a54-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59a54-313">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="59a54-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="59a54-314">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="59a54-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="59a54-315">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="59a54-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="59a54-316">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="59a54-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="59a54-317">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-318">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="59a54-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-321">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="59a54-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-322">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="59a54-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="59a54-323">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-324">**SKU**</span><span class="sxs-lookup"><span data-stu-id="59a54-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-327">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="59a54-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-328">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="59a54-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="59a54-329">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-330">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="59a54-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-331">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59a54-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-333">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="59a54-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-334">Velocità della memoria fisica, in nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="59a54-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="59a54-335">**Status**</span><span class="sxs-lookup"><span data-stu-id="59a54-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-338">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="59a54-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-339">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="59a54-339">Current status of the object.</span></span> <span data-ttu-id="59a54-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="59a54-341">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="59a54-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="59a54-342">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="59a54-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="59a54-343">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="59a54-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="59a54-344">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="59a54-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="59a54-345">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="59a54-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="59a54-346">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="59a54-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="59a54-347">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="59a54-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="59a54-348">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="59a54-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="59a54-349">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="59a54-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="59a54-350">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="59a54-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="59a54-351">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="59a54-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="59a54-352">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="59a54-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="59a54-353">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="59a54-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="59a54-354">**Tag**</span><span class="sxs-lookup"><span data-stu-id="59a54-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-357">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="59a54-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-358">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="59a54-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="59a54-359">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="59a54-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="59a54-360">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="59a54-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="59a54-361">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="59a54-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="59a54-362">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="59a54-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="59a54-363">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="59a54-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="59a54-364">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59a54-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="59a54-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-366">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59a54-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-368">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo di memoria DMTF \| 002,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="59a54-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="59a54-369">Larghezza totale, in bit, della memoria fisica, inclusi i bit di controllo o di correzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="59a54-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="59a54-370">Se non sono presenti bit per la correzione di errori, il valore in questa proprietà deve corrispondere a quello specificato per la proprietà **DataWidth** .</span><span class="sxs-lookup"><span data-stu-id="59a54-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="59a54-371">**Versione**</span><span class="sxs-lookup"><span data-stu-id="59a54-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a54-372">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59a54-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a54-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59a54-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a54-374">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="59a54-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="59a54-375">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="59a54-375">Version of the physical element.</span></span>

<span data-ttu-id="59a54-376">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59a54-377">Commenti</span><span class="sxs-lookup"><span data-stu-id="59a54-377">Remarks</span></span>

<span data-ttu-id="59a54-378">La classe **CIM \_ PhysicalMemory** è derivata da [**\_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="59a54-379">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="59a54-379">WMI does not implement this class.</span></span> <span data-ttu-id="59a54-380">Per le classi WMI derivate da **CIM \_ PhysicalMemory**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="59a54-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="59a54-381">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="59a54-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="59a54-382">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="59a54-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a54-383">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59a54-383">Requirements</span></span>



| <span data-ttu-id="59a54-384">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a54-384">Requirement</span></span> | <span data-ttu-id="59a54-385">Valore</span><span class="sxs-lookup"><span data-stu-id="59a54-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59a54-386">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59a54-386">Minimum supported client</span></span><br/> | <span data-ttu-id="59a54-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59a54-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59a54-388">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59a54-388">Minimum supported server</span></span><br/> | <span data-ttu-id="59a54-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59a54-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59a54-390">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59a54-390">Namespace</span></span><br/>                | <span data-ttu-id="59a54-391">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="59a54-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59a54-392">MOF</span><span class="sxs-lookup"><span data-stu-id="59a54-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59a54-393"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59a54-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59a54-394">DLL</span><span class="sxs-lookup"><span data-stu-id="59a54-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59a54-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59a54-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59a54-396">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59a54-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a54-397">**\_Chip CIM**</span><span class="sxs-lookup"><span data-stu-id="59a54-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 


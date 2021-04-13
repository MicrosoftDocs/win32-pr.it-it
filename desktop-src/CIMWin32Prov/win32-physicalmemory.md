---
description: Rappresenta un dispositivo di memoria fisica che si trova in un sistema di computer e disponibile per il sistema operativo.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483957"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="68890-103">Win32 \_ PhysicalMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="68890-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="68890-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemory Win32** rappresenta un dispositivo di memoria fisica che si trova in un sistema di computer e disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68890-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="68890-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="68890-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68890-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="68890-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68890-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68890-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
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
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="68890-108">Members</span><span class="sxs-lookup"><span data-stu-id="68890-108">Members</span></span>

<span data-ttu-id="68890-109">La classe **Win32 \_ PhysicalMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="68890-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="68890-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68890-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68890-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68890-111">Properties</span></span>

<span data-ttu-id="68890-112">La classe **Win32 \_ PhysicalMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="68890-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68890-113">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="68890-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-116">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| Attributes")</span><span class="sxs-lookup"><span data-stu-id="68890-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="68890-117">SMBIOS: tipo 17-attributi.</span><span class="sxs-lookup"><span data-stu-id="68890-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="68890-118">Rappresenta il rango.</span><span class="sxs-lookup"><span data-stu-id="68890-118">Represents the RANK.</span></span>

<span data-ttu-id="68890-119">Questo valore deriva dal membro **Attributes** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-120">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68890-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="68890-121">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="68890-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-124">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| dispositivo di memoria \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="68890-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="68890-125">Banca con etichetta fisica in cui si trova la memoria.</span><span class="sxs-lookup"><span data-stu-id="68890-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="68890-126">Esempi: "Bank 0", "Bank A"</span><span class="sxs-lookup"><span data-stu-id="68890-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="68890-127">Questo valore deriva dal membro **Bank Locator** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-128">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-129">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="68890-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-130">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68890-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68890-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-132">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo di memoria DMTF \| 002,5 "), [**unità**](../wmisdk/standard-qualifiers.md) (" byte ")</span><span class="sxs-lookup"><span data-stu-id="68890-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="68890-133">Capacità totale della memoria fisica, in byte.</span><span class="sxs-lookup"><span data-stu-id="68890-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="68890-134">Questo valore deriva dalla struttura del **dispositivo di memoria** nelle informazioni sulla versione di SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="68890-135">Per le versioni SMBIOS 2,1 e 2,6, il valore deriva dal membro **size** .</span><span class="sxs-lookup"><span data-stu-id="68890-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="68890-136">Per SMBIOS versione 2.7 + il valore deriva dal membro di **dimensioni estese** .</span><span class="sxs-lookup"><span data-stu-id="68890-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="68890-137">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="68890-138">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="68890-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="68890-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-142">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="68890-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="68890-143">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="68890-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="68890-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-145">**ConfiguredClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="68890-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-148">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 17 \| velocità di clock di memoria configurata")</span><span class="sxs-lookup"><span data-stu-id="68890-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="68890-149">Velocità di clock configurata del dispositivo di memoria, in megahertz (MHz) o 0, se la velocità è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="68890-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="68890-150">Questo valore deriva dal membro della **velocità di clock della memoria configurata** per la struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-151">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68890-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="68890-152">**ConfiguredVoltage**</span><span class="sxs-lookup"><span data-stu-id="68890-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-155">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| configured Voltage")</span><span class="sxs-lookup"><span data-stu-id="68890-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="68890-156">Tensione configurata per questo dispositivo, in millivolt o 0, se la tensione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="68890-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="68890-157">Questo valore deriva dal membro di **tensione configurato** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-158">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68890-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="68890-159">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68890-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-162">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="68890-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68890-163">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="68890-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="68890-164">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="68890-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="68890-165">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="68890-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68890-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68890-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-169">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo di memoria DMTF \| 002,8 "), [**unità**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="68890-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="68890-170">Larghezza dei dati della memoria fisica, in bit.</span><span class="sxs-lookup"><span data-stu-id="68890-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="68890-171">Una larghezza di dati pari a 0 (zero) e una larghezza totale di 8 (otto) indica che la memoria viene utilizzata esclusivamente per fornire i bit di correzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="68890-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="68890-172">Questo valore deriva dal membro della **larghezza dei dati** della struttura del dispositivo di **memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-173">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-174">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="68890-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-177">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="68890-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="68890-178">Descrizione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="68890-178">Description of an object.</span></span>

<span data-ttu-id="68890-179">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="68890-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-183">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 17 \| dispositivo Locator")</span><span class="sxs-lookup"><span data-stu-id="68890-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="68890-184">Etichetta del socket o della lavagna che possiede la memoria.</span><span class="sxs-lookup"><span data-stu-id="68890-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="68890-185">Esempio: "SIMM 3"</span><span class="sxs-lookup"><span data-stu-id="68890-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="68890-186">Questo valore deriva dal membro del **localizzatore di dispositivi** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="68890-187">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="68890-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-188">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68890-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68890-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-190">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| dispositivo di memoria \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="68890-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="68890-191">Fattore di forma dell'implementazione per il chip.</span><span class="sxs-lookup"><span data-stu-id="68890-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="68890-192">Questo valore deriva dal membro del **fattore di forma** della struttura del dispositivo di **memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-193">Questa proprietà viene ereditata [**dal \_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="68890-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="68890-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="68890-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="68890-195">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="68890-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="68890-196">(1)</span><span class="sxs-lookup"><span data-stu-id="68890-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="68890-197">Altro</span><span class="sxs-lookup"><span data-stu-id="68890-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="68890-198">(2)</span><span class="sxs-lookup"><span data-stu-id="68890-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="68890-199">SIP</span><span class="sxs-lookup"><span data-stu-id="68890-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-200">(3)</span><span class="sxs-lookup"><span data-stu-id="68890-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="68890-201">DIP</span><span class="sxs-lookup"><span data-stu-id="68890-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-202">(4)</span><span class="sxs-lookup"><span data-stu-id="68890-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="68890-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="68890-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-204">(5)</span><span class="sxs-lookup"><span data-stu-id="68890-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="68890-205">SOJ</span><span class="sxs-lookup"><span data-stu-id="68890-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="68890-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="68890-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="68890-207">Proprietario</span><span class="sxs-lookup"><span data-stu-id="68890-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="68890-208">(7)</span><span class="sxs-lookup"><span data-stu-id="68890-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="68890-209">SIMM</span><span class="sxs-lookup"><span data-stu-id="68890-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="68890-210">(8)</span><span class="sxs-lookup"><span data-stu-id="68890-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="68890-211">DIMM</span><span class="sxs-lookup"><span data-stu-id="68890-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="68890-212">(9)</span><span class="sxs-lookup"><span data-stu-id="68890-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="68890-213">TSOP</span><span class="sxs-lookup"><span data-stu-id="68890-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-214">(10)</span><span class="sxs-lookup"><span data-stu-id="68890-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="68890-215">PGA</span><span class="sxs-lookup"><span data-stu-id="68890-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="68890-216">(11)</span><span class="sxs-lookup"><span data-stu-id="68890-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="68890-217">RIMM</span><span class="sxs-lookup"><span data-stu-id="68890-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="68890-218">12</span><span class="sxs-lookup"><span data-stu-id="68890-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="68890-219">SODIMM</span><span class="sxs-lookup"><span data-stu-id="68890-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="68890-220">(13)</span><span class="sxs-lookup"><span data-stu-id="68890-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="68890-221">SRIMM</span><span class="sxs-lookup"><span data-stu-id="68890-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="68890-222">(14)</span><span class="sxs-lookup"><span data-stu-id="68890-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="68890-223">SMD</span><span class="sxs-lookup"><span data-stu-id="68890-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="68890-224">(15)</span><span class="sxs-lookup"><span data-stu-id="68890-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="68890-225">SSMP</span><span class="sxs-lookup"><span data-stu-id="68890-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-226">(16)</span><span class="sxs-lookup"><span data-stu-id="68890-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="68890-227">QFP</span><span class="sxs-lookup"><span data-stu-id="68890-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-228">(17)</span><span class="sxs-lookup"><span data-stu-id="68890-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="68890-229">TQFP</span><span class="sxs-lookup"><span data-stu-id="68890-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="68890-230">(18)</span><span class="sxs-lookup"><span data-stu-id="68890-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="68890-231">SOIC</span><span class="sxs-lookup"><span data-stu-id="68890-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="68890-232">(19)</span><span class="sxs-lookup"><span data-stu-id="68890-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="68890-233">LCC</span><span class="sxs-lookup"><span data-stu-id="68890-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="68890-234">(20)</span><span class="sxs-lookup"><span data-stu-id="68890-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="68890-235">PLCC</span><span class="sxs-lookup"><span data-stu-id="68890-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="68890-236">(21)</span><span class="sxs-lookup"><span data-stu-id="68890-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="68890-237">BGA</span><span class="sxs-lookup"><span data-stu-id="68890-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="68890-238">(22)</span><span class="sxs-lookup"><span data-stu-id="68890-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="68890-239">FPBGA</span><span class="sxs-lookup"><span data-stu-id="68890-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="68890-240">(23)</span><span class="sxs-lookup"><span data-stu-id="68890-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="68890-241">LGA</span><span class="sxs-lookup"><span data-stu-id="68890-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68890-242">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="68890-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-243">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="68890-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68890-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68890-245">Se **true**, questo componente multimediale fisico può essere sostituito con un fisico diverso, ma equivalente, mentre al pacchetto contenitore viene applicata la potenza.</span><span class="sxs-lookup"><span data-stu-id="68890-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="68890-246">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="68890-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="68890-247">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="68890-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="68890-248">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="68890-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68890-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-250">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68890-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68890-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-252">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="68890-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="68890-253">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68890-253">Date and time the object is installed.</span></span> <span data-ttu-id="68890-254">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="68890-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="68890-255">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-256">**InterleaveDataDepth**</span><span class="sxs-lookup"><span data-stu-id="68890-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68890-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68890-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-259">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 20 \| Interleaved data Depth")</span><span class="sxs-lookup"><span data-stu-id="68890-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="68890-260">Numero intero senza segno a 16 bit di righe consecutive di dati a cui è possibile accedere in un singolo trasferimento Interleaved dal dispositivo di memoria.</span><span class="sxs-lookup"><span data-stu-id="68890-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="68890-261">Se il valore è 0 (zero), la memoria non è Interleaved.</span><span class="sxs-lookup"><span data-stu-id="68890-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="68890-262">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="68890-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-263">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-265">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Indirizzi con mapping del dispositivo di memoria DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="68890-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="68890-266">Posizione della memoria fisica in un interleave.</span><span class="sxs-lookup"><span data-stu-id="68890-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="68890-267">Ad esempio, in un'interleave 2:1, il valore "1" indica che la memoria si trova nella posizione "even".</span><span class="sxs-lookup"><span data-stu-id="68890-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="68890-268">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="68890-269">0</span><span class="sxs-lookup"><span data-stu-id="68890-269">0</span></span>
</dt> <dd>

<span data-ttu-id="68890-270">Non interleaved</span><span class="sxs-lookup"><span data-stu-id="68890-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="68890-271">1</span><span class="sxs-lookup"><span data-stu-id="68890-271">1</span></span>
</dt> <dd>

<span data-ttu-id="68890-272">Prima posizione</span><span class="sxs-lookup"><span data-stu-id="68890-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="68890-273">2</span><span class="sxs-lookup"><span data-stu-id="68890-273">2</span></span>
</dt> <dd>

<span data-ttu-id="68890-274">Seconda posizione</span><span class="sxs-lookup"><span data-stu-id="68890-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68890-275">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="68890-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-278">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="68890-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68890-279">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="68890-280">Questo valore deriva dal membro del **produttore** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-281">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-282">**MaxVoltage**</span><span class="sxs-lookup"><span data-stu-id="68890-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-285">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 17 \| massima tensione")</span><span class="sxs-lookup"><span data-stu-id="68890-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="68890-286">La massima tensione operativa per questo dispositivo, in millivolt o 0, se la tensione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="68890-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="68890-287">Questo valore deriva dal membro di **tensione massima** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-288">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68890-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="68890-289">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="68890-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-290">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68890-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68890-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-292">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| dispositivo di memoria \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="68890-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="68890-293">Tipo di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="68890-293">Type of physical memory.</span></span> <span data-ttu-id="68890-294">Si tratta di un valore CIM mappato al valore SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="68890-295">La proprietà **SMBIOSMemoryType** contiene il tipo di memoria SMBIOS non elaborata.</span><span class="sxs-lookup"><span data-stu-id="68890-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="68890-296">Questo valore deriva dal membro del **tipo di memoria** della struttura del dispositivo di **memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-297">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68890-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="68890-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68890-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="68890-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="68890-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="68890-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="68890-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**DRAM sincrona** (3)</span><span class="sxs-lookup"><span data-stu-id="68890-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="68890-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Memoria DRAM cache** (4)</span><span class="sxs-lookup"><span data-stu-id="68890-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="68890-303"><span id="EDO"></span><span id="edo"></span>**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="68890-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="68890-304"><span id="EDRAM"></span><span id="edram"></span>**Edra** (6)</span><span class="sxs-lookup"><span data-stu-id="68890-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="68890-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="68890-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="68890-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="68890-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="68890-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="68890-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="68890-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="68890-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="68890-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="68890-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="68890-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="68890-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="68890-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="68890-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="68890-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="68890-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="68890-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="68890-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="68890-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="68890-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="68890-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="68890-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="68890-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="68890-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="68890-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="68890-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="68890-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="68890-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="68890-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="68890-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="68890-320">DDR2 — potrebbe non essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="68890-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="68890-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="68890-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="68890-322">DDR2-FB-DIMM potrebbe non essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="68890-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="68890-323">24</span><span class="sxs-lookup"><span data-stu-id="68890-323">24</span></span>
</dt> <dd>

<span data-ttu-id="68890-324">DDR3: potrebbe non essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="68890-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="68890-325">25</span><span class="sxs-lookup"><span data-stu-id="68890-325">25</span></span>
</dt> <dd>

<span data-ttu-id="68890-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="68890-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="68890-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span><span class="sxs-lookup"><span data-stu-id="68890-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68890-328">**MinVoltage**</span><span class="sxs-lookup"><span data-stu-id="68890-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-329">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-331">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 20 \| min Voltage")</span><span class="sxs-lookup"><span data-stu-id="68890-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="68890-332">La tensione minima operativa per questo dispositivo, in millivolt o 0, se la tensione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="68890-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="68890-333">Questo valore deriva dal membro di **tensione minima** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-334">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68890-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="68890-335">**Modello**</span><span class="sxs-lookup"><span data-stu-id="68890-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-338">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="68890-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68890-339">Nome dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-339">Name for the physical element.</span></span>

<span data-ttu-id="68890-340">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-341">**Nome**</span><span class="sxs-lookup"><span data-stu-id="68890-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-344">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="68890-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="68890-345">Etichetta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68890-345">Label for the object.</span></span> <span data-ttu-id="68890-346">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="68890-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="68890-347">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="68890-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68890-351">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="68890-352">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="68890-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="68890-353">Se solo i dati del codice a barre sono disponibili e sono univoci oppure possono essere utilizzati come chiave di elemento, questa proprietà è **null** e i dati del codice a barre vengono utilizzati come chiave della classe nella proprietà Tag.</span><span class="sxs-lookup"><span data-stu-id="68890-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="68890-354">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-355">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="68890-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-358">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="68890-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68890-359">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="68890-360">Questo valore deriva dal membro del **numero di parte** della struttura del dispositivo di **memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-361">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-362">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="68890-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-363">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-365">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Indirizzi con mapping del dispositivo di memoria DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="68890-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="68890-366">Posizione della memoria fisica in una riga.</span><span class="sxs-lookup"><span data-stu-id="68890-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="68890-367">Se, ad esempio, sono necessari dispositivi di memoria a 2 8 bit per formare una riga a 16 bit, un valore pari a 2 (due) indica che la memoria è il secondo dispositivo: 0 (zero) è un valore non valido per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="68890-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="68890-368">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-369">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="68890-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-370">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="68890-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68890-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68890-372">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="68890-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="68890-373">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-374">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="68890-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-375">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="68890-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68890-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68890-377">Se è **true**, un componente fisico è rimovibile (se è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente trovato, senza compromettere la funzione della creazione complessiva dei pacchetti).</span><span class="sxs-lookup"><span data-stu-id="68890-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="68890-378">Un componente può comunque essere rimovibile se l'alimentazione deve essere "off" per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="68890-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="68890-379">Se Power può essere "on" e il componente è stato rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="68890-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="68890-380">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="68890-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="68890-381">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="68890-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-382">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="68890-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-383">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="68890-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68890-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68890-385">Se **true**, questo componente multimediale fisico può essere sostituito con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="68890-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="68890-386">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="68890-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="68890-387">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="68890-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="68890-388">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="68890-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="68890-389">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="68890-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-390">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="68890-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-393">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="68890-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68890-394">Numero allocato dal produttore per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="68890-395">Questo valore deriva dal membro del **numero di serie** della struttura del dispositivo di **memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-396">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-397">**SKU**</span><span class="sxs-lookup"><span data-stu-id="68890-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-398">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-400">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="68890-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68890-401">Numero di unità di conservazione per l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="68890-402">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-403">**SMBIOSMemoryType**</span><span class="sxs-lookup"><span data-stu-id="68890-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-404">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-406">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 17 \| Memory \_ Type")</span><span class="sxs-lookup"><span data-stu-id="68890-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="68890-407">Tipo di memoria SMBIOS non elaborata.</span><span class="sxs-lookup"><span data-stu-id="68890-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="68890-408">Il valore della proprietà **MemoryType** è un valore CIM mappato al valore SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="68890-409">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68890-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="68890-410">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="68890-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-411">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68890-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68890-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-413">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("nanosecondi")</span><span class="sxs-lookup"><span data-stu-id="68890-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="68890-414">Velocità della memoria fisica, in nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="68890-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="68890-415">Questo valore deriva dal membro della **velocità** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-416">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-417">**Status**</span><span class="sxs-lookup"><span data-stu-id="68890-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-420">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="68890-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="68890-421">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="68890-421">Current status of the object.</span></span> <span data-ttu-id="68890-422">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="68890-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="68890-423">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="68890-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="68890-424">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="68890-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="68890-425">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="68890-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="68890-426">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="68890-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="68890-427">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="68890-428">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="68890-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="68890-429">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="68890-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="68890-430">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="68890-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68890-431">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="68890-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68890-432">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="68890-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="68890-433">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="68890-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="68890-434">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="68890-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="68890-435">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="68890-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="68890-436">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="68890-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="68890-437">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="68890-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="68890-438">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="68890-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="68890-439">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="68890-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="68890-440">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="68890-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68890-441">**Tag**</span><span class="sxs-lookup"><span data-stu-id="68890-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-444">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="68890-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="68890-445">Identificatore univoco del dispositivo di memoria fisica rappresentato da un'istanza di **Win32 \_ PhysicalMemory**.</span><span class="sxs-lookup"><span data-stu-id="68890-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="68890-446">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="68890-447">Esempio: "memoria fisica 1"</span><span class="sxs-lookup"><span data-stu-id="68890-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="68890-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="68890-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-449">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68890-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68890-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-451">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo di memoria DMTF \| 002,7 "), [**unità**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="68890-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="68890-452">Larghezza totale, in bit, della memoria fisica, inclusi i bit di controllo o di correzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="68890-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="68890-453">Se non sono presenti bit per la correzione di errori, il valore in questa proprietà deve corrispondere a quanto specificato per la proprietà **DataWidth** .</span><span class="sxs-lookup"><span data-stu-id="68890-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="68890-454">Questo valore deriva dal membro della **larghezza totale** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="68890-455">Questa proprietà viene ereditata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="68890-456">**TypeDetail**</span><span class="sxs-lookup"><span data-stu-id="68890-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-457">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68890-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68890-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-459">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 17 \| detail")</span><span class="sxs-lookup"><span data-stu-id="68890-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="68890-460">Tipo di memoria fisica rappresentata.</span><span class="sxs-lookup"><span data-stu-id="68890-460">Type of physical memory represented.</span></span>

<span data-ttu-id="68890-461">Questo valore deriva dal membro **Detail del tipo** della struttura del **dispositivo di memoria** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="68890-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="68890-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (1)</span><span class="sxs-lookup"><span data-stu-id="68890-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68890-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (2)</span><span class="sxs-lookup"><span data-stu-id="68890-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68890-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (4)</span><span class="sxs-lookup"><span data-stu-id="68890-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="68890-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>Con **paging rapido** (8)</span><span class="sxs-lookup"><span data-stu-id="68890-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="68890-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Colonna statica** (16)</span><span class="sxs-lookup"><span data-stu-id="68890-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="68890-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-statico** (32)</span><span class="sxs-lookup"><span data-stu-id="68890-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="68890-468"><span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)</span><span class="sxs-lookup"><span data-stu-id="68890-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="68890-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Sincrono** (128)</span><span class="sxs-lookup"><span data-stu-id="68890-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="68890-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span><span class="sxs-lookup"><span data-stu-id="68890-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="68890-471"><span id="EDO"></span><span id="edo"></span>**Edo** (512)</span><span class="sxs-lookup"><span data-stu-id="68890-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="68890-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**DRAM finestra** (1024)</span><span class="sxs-lookup"><span data-stu-id="68890-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="68890-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Memoria DRAM cache** (2048)</span><span class="sxs-lookup"><span data-stu-id="68890-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="68890-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non volatile** (4096)</span><span class="sxs-lookup"><span data-stu-id="68890-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="68890-475">Non volatile</span><span class="sxs-lookup"><span data-stu-id="68890-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68890-476">**Versione**</span><span class="sxs-lookup"><span data-stu-id="68890-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68890-477">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68890-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68890-478">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68890-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68890-479">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="68890-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68890-480">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="68890-480">Version of the physical element.</span></span>

<span data-ttu-id="68890-481">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68890-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68890-482">Commenti</span><span class="sxs-lookup"><span data-stu-id="68890-482">Remarks</span></span>

<span data-ttu-id="68890-483">La classe **Win32 \_ PhysicalMemory** è derivata da [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="68890-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="68890-484">Esempio</span><span class="sxs-lookup"><span data-stu-id="68890-484">Examples</span></span>

<span data-ttu-id="68890-485">L'esempio relativo a [Get-ComputerInfo-query computer da computer locale/remoto-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell nella raccolta TechNet usa una serie di chiamate a hardware e software, tra cui **Win32 \_ PhysicalMemory**, per visualizzare informazioni su un sistema locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="68890-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="68890-486">L'esempio di PowerShell per il [report del server](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) nella raccolta TechNet usa una serie di chiamate a hardware e software, tra cui **Win32 \_ PhysicalMemory**, per raccogliere informazioni sul server e pubblicarle nel documento di Word.</span><span class="sxs-lookup"><span data-stu-id="68890-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="68890-487">Nell'esempio di codice PowerShell seguente vengono recuperate informazioni sulla memoria fisica del computer locale.</span><span class="sxs-lookup"><span data-stu-id="68890-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="68890-488">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68890-488">Requirements</span></span>



| <span data-ttu-id="68890-489">Requisito</span><span class="sxs-lookup"><span data-stu-id="68890-489">Requirement</span></span> | <span data-ttu-id="68890-490">Valore</span><span class="sxs-lookup"><span data-stu-id="68890-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68890-491">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68890-491">Minimum supported client</span></span><br/> | <span data-ttu-id="68890-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68890-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68890-493">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68890-493">Minimum supported server</span></span><br/> | <span data-ttu-id="68890-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68890-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68890-495">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="68890-495">Namespace</span></span><br/>                | <span data-ttu-id="68890-496">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="68890-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68890-497">MOF</span><span class="sxs-lookup"><span data-stu-id="68890-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68890-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68890-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68890-499">DLL</span><span class="sxs-lookup"><span data-stu-id="68890-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68890-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68890-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68890-501">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68890-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68890-502">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="68890-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="68890-503">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="68890-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

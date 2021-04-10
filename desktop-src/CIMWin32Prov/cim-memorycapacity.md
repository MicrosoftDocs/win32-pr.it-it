---
description: La \_ classe CIM MemoryCapacity rappresenta la memoria che può essere installata su un elemento fisico e le configurazioni minime e massime.
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: Classe CIM_MemoryCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225559"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="5ae00-103">CIM \_ MemoryCapacity (classe)</span><span class="sxs-lookup"><span data-stu-id="5ae00-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="5ae00-104">La classe **CIM \_ MemoryCapacity** rappresenta la memoria che può essere installata su un elemento fisico e le configurazioni minime e massime.</span><span class="sxs-lookup"><span data-stu-id="5ae00-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="5ae00-105">Le informazioni sulla memoria attualmente installata e i requisiti minimi e massimi di un elemento si trovano nelle istanze della classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="5ae00-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ae00-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5ae00-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5ae00-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5ae00-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5ae00-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ae00-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5ae00-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5ae00-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae00-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ae00-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="5ae00-111">Members</span><span class="sxs-lookup"><span data-stu-id="5ae00-111">Members</span></span>

<span data-ttu-id="5ae00-112">La classe **CIM \_ MemoryCapacity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ae00-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="5ae00-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ae00-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ae00-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ae00-114">Properties</span></span>

<span data-ttu-id="5ae00-115">La classe **CIM \_ MemoryCapacity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ae00-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ae00-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5ae00-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae00-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ae00-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae00-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5ae00-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ae00-120">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ae00-120">Short textual description of the object.</span></span>

<span data-ttu-id="5ae00-121">Questa proprietà viene ereditata da [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="5ae00-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ae00-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5ae00-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae00-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ae00-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae00-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ae00-125">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ae00-125">Textual description of the object.</span></span>

<span data-ttu-id="5ae00-126">Questa proprietà viene ereditata da [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="5ae00-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ae00-127">**MaximumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="5ae00-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae00-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ae00-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae00-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-130">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="5ae00-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5ae00-131">Quantità massima di memoria, in kilobyte, che può essere supportata dall'elemento fisico associato.</span><span class="sxs-lookup"><span data-stu-id="5ae00-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="5ae00-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5ae00-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5ae00-133">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="5ae00-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae00-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5ae00-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae00-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-136">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span><span class="sxs-lookup"><span data-stu-id="5ae00-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="5ae00-137">Tipo di memoria, che fa parte della chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ae00-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="5ae00-138">I valori corrispondono all'elenco dei possibili tipi di memoria nella classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="5ae00-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ae00-139">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5ae00-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5ae00-140">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="5ae00-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="5ae00-141">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="5ae00-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="5ae00-142">**DRAM sincrona** (3)</span><span class="sxs-lookup"><span data-stu-id="5ae00-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="5ae00-143">**Memoria DRAM cache** (4)</span><span class="sxs-lookup"><span data-stu-id="5ae00-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="5ae00-144">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="5ae00-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="5ae00-145">**Edra** (6)</span><span class="sxs-lookup"><span data-stu-id="5ae00-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="5ae00-146">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="5ae00-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="5ae00-147">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="5ae00-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="5ae00-148">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="5ae00-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="5ae00-149">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="5ae00-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="5ae00-150">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="5ae00-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="5ae00-151">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="5ae00-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="5ae00-152">**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="5ae00-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="5ae00-153">**EPROM** (14)</span><span class="sxs-lookup"><span data-stu-id="5ae00-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="5ae00-154">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="5ae00-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="5ae00-155">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="5ae00-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="5ae00-156">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="5ae00-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="5ae00-157">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="5ae00-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="5ae00-158">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="5ae00-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="5ae00-159">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="5ae00-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="5ae00-160">**DDR-2** (21)</span><span class="sxs-lookup"><span data-stu-id="5ae00-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ae00-161">**MinimumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="5ae00-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae00-162">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ae00-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae00-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-164">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="5ae00-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5ae00-165">Quantità minima di memoria, in kilobyte, necessaria per il corretto funzionamento dell'elemento fisico associato.</span><span class="sxs-lookup"><span data-stu-id="5ae00-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="5ae00-166">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5ae00-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5ae00-167">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5ae00-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ae00-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ae00-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ae00-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ae00-170">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ae00-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ae00-171">Nome dell'oggetto. funge da parte della chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ae00-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ae00-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ae00-172">Remarks</span></span>

<span data-ttu-id="5ae00-173">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5ae00-173">WMI does not implement this class.</span></span>

<span data-ttu-id="5ae00-174">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5ae00-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5ae00-175">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5ae00-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae00-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ae00-176">Requirements</span></span>



| <span data-ttu-id="5ae00-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae00-177">Requirement</span></span> | <span data-ttu-id="5ae00-178">Valore</span><span class="sxs-lookup"><span data-stu-id="5ae00-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae00-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ae00-179">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae00-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ae00-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ae00-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ae00-181">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae00-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ae00-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ae00-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ae00-183">Namespace</span></span><br/>                | <span data-ttu-id="5ae00-184">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5ae00-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ae00-185">MOF</span><span class="sxs-lookup"><span data-stu-id="5ae00-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ae00-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ae00-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ae00-187">DLL</span><span class="sxs-lookup"><span data-stu-id="5ae00-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ae00-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ae00-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae00-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ae00-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae00-190">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="5ae00-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 


---
description: La \_ relazione CIM DeviceSoftware identifica il software associato a un dispositivo, ad esempio i driver, la configurazione o il software dell'applicazione o il firmware.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: Classe CIM_DeviceSoftware
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523889"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="6ebc6-103">CIM \_ DeviceSoftware (classe)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="6ebc6-104">La relazione **CIM \_ DeviceSoftware** identifica il software associato a un dispositivo, ad esempio i driver, la configurazione o il software dell'applicazione o il firmware.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ebc6-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6ebc6-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6ebc6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6ebc6-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6ebc6-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebc6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ebc6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="6ebc6-110">Members</span><span class="sxs-lookup"><span data-stu-id="6ebc6-110">Members</span></span>

<span data-ttu-id="6ebc6-111">La classe **CIM \_ DeviceSoftware** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6ebc6-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="6ebc6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ebc6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ebc6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ebc6-113">Properties</span></span>

<span data-ttu-id="6ebc6-114">La classe **CIM \_ DeviceSoftware** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ebc6-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ebc6-116">Tipo di dati: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ebc6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="6ebc6-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6ebc6-119">Oggetto [**CIM \_ SoftwareElement**](cim-softwareelement.md) che descrive l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="6ebc6-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ebc6-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ebc6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="6ebc6-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6ebc6-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico che richiede o utilizza il software.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="6ebc6-125">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ebc6-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ebc6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-128">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="6ebc6-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6ebc6-129">Ruolo che il software prende in considerazione sul dispositivo associato.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ebc6-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-131">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ebc6-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-133">Altro.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="6ebc6-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-135">Driver.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="6ebc6-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Software di configurazione** (3)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-137">Software di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="6ebc6-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Software applicativo** (4)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-139">Software applicativo.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="6ebc6-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Strumentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-141">Strumentazione.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="6ebc6-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-143">Firmware.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="6ebc6-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-145">BIOS.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="6ebc6-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**ROM di avvio** (8)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6ebc6-147">ROM di avvio.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ebc6-148">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ebc6-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ebc6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ebc6-151">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**Scopo**")</span><span class="sxs-lookup"><span data-stu-id="6ebc6-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="6ebc6-152">Stringa in formato libero che fornisce ulteriori informazioni per la proprietà **purpose** , ad esempio "software dell'applicazione".</span><span class="sxs-lookup"><span data-stu-id="6ebc6-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ebc6-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ebc6-153">Remarks</span></span>

<span data-ttu-id="6ebc6-154">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-154">WMI does not implement this class.</span></span>

<span data-ttu-id="6ebc6-155">La classe **CIM \_ DeviceSoftware** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6ebc6-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="6ebc6-156">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6ebc6-157">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebc6-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ebc6-158">Requirements</span></span>



| <span data-ttu-id="6ebc6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ebc6-159">Requirement</span></span> | <span data-ttu-id="6ebc6-160">Valore</span><span class="sxs-lookup"><span data-stu-id="6ebc6-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebc6-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ebc6-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6ebc6-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ebc6-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ebc6-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ebc6-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6ebc6-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ebc6-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ebc6-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ebc6-165">Namespace</span></span><br/>                | <span data-ttu-id="6ebc6-166">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6ebc6-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ebc6-167">MOF</span><span class="sxs-lookup"><span data-stu-id="6ebc6-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ebc6-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ebc6-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ebc6-169">DLL</span><span class="sxs-lookup"><span data-stu-id="6ebc6-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ebc6-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ebc6-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebc6-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ebc6-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebc6-172">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


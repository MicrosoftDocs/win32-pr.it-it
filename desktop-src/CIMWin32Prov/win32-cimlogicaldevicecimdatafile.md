---
description: La \_ classe WMI dell'associazione CIMLogicalDeviceCIMDataFile Win32 mette in relazione i dispositivi logici e i file di dati, indicando i file del driver usati dal dispositivo. Questa classe viene utilizzata per individuare i driver di dispositivo utilizzati da un dispositivo.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Classe Win32_CIMLogicalDeviceCIMDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524001"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="e3976-104">Win32 \_ CIMLogicalDeviceCIMDataFile (classe)</span><span class="sxs-lookup"><span data-stu-id="e3976-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="e3976-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ CIMLogicalDeviceCIMDataFile Win32** mette in relazione i dispositivi logici e i file di dati, indicando i file del driver usati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3976-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="e3976-106">Questa classe viene utilizzata per individuare i driver di dispositivo utilizzati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3976-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="e3976-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e3976-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e3976-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e3976-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3976-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3976-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="e3976-110">Members</span><span class="sxs-lookup"><span data-stu-id="e3976-110">Members</span></span>

<span data-ttu-id="e3976-111">La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e3976-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="e3976-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3976-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3976-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3976-113">Properties</span></span>

<span data-ttu-id="e3976-114">La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3976-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3976-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e3976-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3976-116">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e3976-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e3976-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3976-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3976-118">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| CIM \_ CIM LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="e3976-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="e3976-119">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che rappresenta le proprietà del dispositivo logico utilizzato dal file di dati.</span><span class="sxs-lookup"><span data-stu-id="e3976-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="e3976-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="e3976-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3976-121">Tipo di dati **: \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="e3976-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="e3976-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3976-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3976-123">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| DataFile CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="e3976-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="e3976-124">Un file di dati [**CIM \_**](cim-datafile.md) che rappresenta le proprietà del file di dati assegnato al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e3976-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="e3976-125">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="e3976-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3976-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3976-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3976-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3976-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3976-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="e3976-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="e3976-129">Ruolo riprodotto dal file di dati rispetto al dispositivo logico associato.</span><span class="sxs-lookup"><span data-stu-id="e3976-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3976-130">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e3976-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e3976-131">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e3976-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="e3976-132">**Driver** (2)</span><span class="sxs-lookup"><span data-stu-id="e3976-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="e3976-133">**Software di configurazione** (3)</span><span class="sxs-lookup"><span data-stu-id="e3976-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="e3976-134">**Software applicativo** (4)</span><span class="sxs-lookup"><span data-stu-id="e3976-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="e3976-135">**Strumentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="e3976-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="e3976-136">**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="e3976-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3976-137">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="e3976-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3976-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3976-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3976-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3976-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3976-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="e3976-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="e3976-141">Estende il valore della proprietà **purpose** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e3976-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="e3976-142">Esempio: "driver del disco floppy"</span><span class="sxs-lookup"><span data-stu-id="e3976-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3976-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3976-143">Remarks</span></span>

<span data-ttu-id="e3976-144">La classe **Win32 \_ CIMLogicalDeviceCIMDataFile** è derivata dalla [**\_ dipendenza CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e3976-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3976-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3976-145">Requirements</span></span>



| <span data-ttu-id="e3976-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3976-146">Requirement</span></span> | <span data-ttu-id="e3976-147">Valore</span><span class="sxs-lookup"><span data-stu-id="e3976-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3976-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3976-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e3976-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3976-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3976-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3976-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e3976-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3976-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3976-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e3976-152">Namespace</span></span><br/>                | <span data-ttu-id="e3976-153">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e3976-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3976-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e3976-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3976-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3976-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3976-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e3976-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3976-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3976-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3976-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3976-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3976-159">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="e3976-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="e3976-160">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e3976-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 


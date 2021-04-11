---
description: Rappresenta un sistema di computer che esegue Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126273"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="2eabb-103">Win32 \_ ComputerSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="2eabb-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="2eabb-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystem Win32** rappresenta un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="2eabb-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="2eabb-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2eabb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eabb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2eabb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a><span data-ttu-id="2eabb-107">Members</span><span class="sxs-lookup"><span data-stu-id="2eabb-107">Members</span></span>

<span data-ttu-id="2eabb-108">La classe **Win32 \_ ComputerSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2eabb-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="2eabb-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="2eabb-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2eabb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2eabb-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2eabb-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2eabb-111">Methods</span></span>

<span data-ttu-id="2eabb-112">La classe **Win32 \_ ComputerSystem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2eabb-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="2eabb-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="2eabb-113">Method</span></span>                                                                                          | <span data-ttu-id="2eabb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2eabb-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2eabb-115">**JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="2eabb-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="2eabb-116">Aggiunge un computer a un dominio o a un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2eabb-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="2eabb-117">**Rinominare**</span><span class="sxs-lookup"><span data-stu-id="2eabb-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="2eabb-118">Rinomina un computer locale.</span><span class="sxs-lookup"><span data-stu-id="2eabb-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="2eabb-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2eabb-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="2eabb-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-120">Not implemented.</span></span> <span data-ttu-id="2eabb-121">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="2eabb-122">**UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="2eabb-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="2eabb-123">Rimuove un computer da un dominio o un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2eabb-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="2eabb-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2eabb-124">Properties</span></span>

<span data-ttu-id="2eabb-125">La classe **Win32 \_ ComputerSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2eabb-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2eabb-126">**AdminPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="2eabb-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| hardware Security Settings \| AdminPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="2eabb-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-130">Impostazioni di sicurezza hardware del sistema per lo stato della password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="2eabb-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2eabb-131">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2eabb-132">**Abilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2eabb-133">**Non implementato** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-134">**Sconosciuto** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-135">**AutomaticManagedPagefile**</span><span class="sxs-lookup"><span data-stu-id="2eabb-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-139">Se **true**, il file di paging viene gestito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-140">**AutomaticResetBootOption**</span><span class="sxs-lookup"><span data-stu-id="2eabb-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-141">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ computer \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| autoriavvio")</span><span class="sxs-lookup"><span data-stu-id="2eabb-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-144">Se **true**, l'opzione di avvio automatico Reimposta è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2eabb-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-145">**AutomaticResetCapability**</span><span class="sxs-lookup"><span data-stu-id="2eabb-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-149">Se **true**, la reimpostazione automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2eabb-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-150">**BootOptionOnLimit**</span><span class="sxs-lookup"><span data-stu-id="2eabb-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-153">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 \| funzionalità \| opzione di avvio al limite")</span><span class="sxs-lookup"><span data-stu-id="2eabb-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-154">Il limite dell'opzione di avvio è ON.</span><span class="sxs-lookup"><span data-stu-id="2eabb-154">Boot option limit is ON.</span></span> <span data-ttu-id="2eabb-155">Identifica l'azione di sistema quando viene raggiunto il valore **ResetLimit** .</span><span class="sxs-lookup"><span data-stu-id="2eabb-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2eabb-156">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="2eabb-157">**Sistema operativo** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="2eabb-158">**Utilità di sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="2eabb-159">**Non riavviare** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-160">**BootOptionOnWatchDog**</span><span class="sxs-lookup"><span data-stu-id="2eabb-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-163">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (opzione di \| avvio funzionalità di tipo 23 SMBIOS \| \| )</span><span class="sxs-lookup"><span data-stu-id="2eabb-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-164">Tipo di azione di riavvio dopo la scadenza del timer del watchdog.</span><span class="sxs-lookup"><span data-stu-id="2eabb-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2eabb-165">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="2eabb-166">**Sistema operativo** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="2eabb-167">**Utilità di sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="2eabb-168">**Non riavviare** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-169">**BootROMSupported**</span><span class="sxs-lookup"><span data-stu-id="2eabb-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-172">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-173">Se **true**, indica se è supportata una ROM di avvio.</span><span class="sxs-lookup"><span data-stu-id="2eabb-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-174">**BootStatus**</span><span class="sxs-lookup"><span data-stu-id="2eabb-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-175">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-177">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 32 avvio \| informazioni di avvio sistema \| stato")</span><span class="sxs-lookup"><span data-stu-id="2eabb-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-178">Stato e campi dati aggiuntivi che identificano lo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="2eabb-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="2eabb-179">Questo valore deriva dal membro di **stato di avvio** della struttura delle informazioni di avvio del **sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2eabb-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2eabb-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-181">**BootupState**</span><span class="sxs-lookup"><span data-stu-id="2eabb-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-184">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")</span><span class="sxs-lookup"><span data-stu-id="2eabb-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-185">Il sistema è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-185">System is started.</span></span> <span data-ttu-id="2eabb-186">L'avvio alternativo ignora i file di avvio utente chiamati anche SafeBoot.</span><span class="sxs-lookup"><span data-stu-id="2eabb-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="2eabb-187">L'elenco seguente contiene i valori obbligatori:</span><span class="sxs-lookup"><span data-stu-id="2eabb-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="2eabb-188">"Avvio normale"</span><span class="sxs-lookup"><span data-stu-id="2eabb-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="2eabb-189">"Avvio non riuscito"</span><span class="sxs-lookup"><span data-stu-id="2eabb-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="2eabb-190">"Fail-safe with Network Boot"</span><span class="sxs-lookup"><span data-stu-id="2eabb-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="2eabb-191">**Avvio normale** ("avvio normale")</span><span class="sxs-lookup"><span data-stu-id="2eabb-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="2eabb-192">**Avvio non riuscito** ("avvio alternativo")</span><span class="sxs-lookup"><span data-stu-id="2eabb-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="2eabb-193">**Fail-Safe con avvio di rete** ("fail-safe with Network Boot")</span><span class="sxs-lookup"><span data-stu-id="2eabb-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-194">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2eabb-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-197">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2eabb-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-198">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="2eabb-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="2eabb-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-200">**ChassisBootupState**</span><span class="sxs-lookup"><span data-stu-id="2eabb-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-201">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-203">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 3 \| stato di avvio")</span><span class="sxs-lookup"><span data-stu-id="2eabb-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-204">Stato di avvio dello chassis.</span><span class="sxs-lookup"><span data-stu-id="2eabb-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="2eabb-205">Questo valore deriva dal membro **dello stato di avvio** dell'enclosure di **sistema o** dalla struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eabb-206">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-207">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="2eabb-208">**Sicuro** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2eabb-209">**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2eabb-210">**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="2eabb-211">**Non reversibile** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-212">**ChassisSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="2eabb-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-215">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| chassis \| SKU Number")</span><span class="sxs-lookup"><span data-stu-id="2eabb-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-216">Il numero di SKU dello chassis o dell'enclosure sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="2eabb-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="2eabb-217">Questo valore deriva dal membro del **numero di SKU** dell' **enclosure di sistema o** dalla struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2eabb-218">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2eabb-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-219">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2eabb-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-222">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2eabb-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-223">Nome della prima classe concreta nella catena di ereditarietà di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="2eabb-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="2eabb-224">È possibile utilizzare questa proprietà con altre proprietà della classe per identificare tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2eabb-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="2eabb-225">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-226">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="2eabb-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-227">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-228">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-229">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Structures \| Debias [**\_ \_ Information fuso orario**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="2eabb-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-230">Quantità di tempo in cui il sistema informatico viene sfalsato rispetto all'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="2eabb-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-231">**DaylightInEffect**</span><span class="sxs-lookup"><span data-stu-id="2eabb-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-232">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-234">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span><span class="sxs-lookup"><span data-stu-id="2eabb-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-235">Se **true**, la modalità ora legale è impostata su on.</span><span class="sxs-lookup"><span data-stu-id="2eabb-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-236">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2eabb-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-239">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2eabb-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-240">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-240">Description of the object.</span></span>

<span data-ttu-id="2eabb-241">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-242">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="2eabb-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-245">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| presunto GetComputerNameEx \| ComputerNameDnsHostname")</span><span class="sxs-lookup"><span data-stu-id="2eabb-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-246">Nome del computer locale in base al Domain Name Server (DNS).</span><span class="sxs-lookup"><span data-stu-id="2eabb-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-247">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="2eabb-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-250">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**WKSTA \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ LANGROUP")</span><span class="sxs-lookup"><span data-stu-id="2eabb-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-251">Nome del dominio a cui appartiene un computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="2eabb-252">Se il computer non fa parte di un dominio, viene restituito il nome del gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2eabb-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="2eabb-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="2eabb-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-254">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-256">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (DS) Structures \| [**DSROLE \_ Primary \_ Domain \_ info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ computer \_ Role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| ruolo")</span><span class="sxs-lookup"><span data-stu-id="2eabb-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-257">Ruolo di un computer in un gruppo di lavoro di dominio assegnato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="2eabb-258">Un gruppo di lavoro di dominio è una raccolta di computer nella stessa rete.</span><span class="sxs-lookup"><span data-stu-id="2eabb-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="2eabb-259">Una proprietà **DomainRole** , ad esempio, può indicare che un computer è una workstation membro.</span><span class="sxs-lookup"><span data-stu-id="2eabb-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="2eabb-260">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="2eabb-261">**Workstation autonoma** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="2eabb-262">**Workstation membro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="2eabb-263">**Server autonomo** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="2eabb-264">**Server membro** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="2eabb-265">**Controller di dominio di backup** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="2eabb-266">**Controller di dominio primario** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-267">**EnableDaylightSavingsTime**</span><span class="sxs-lookup"><span data-stu-id="2eabb-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-268">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-269">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-270">Consente l'ora legale (DST) in un computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="2eabb-271">Il valore **true** indica che l'ora di sistema passa a un'ora avanti o indietro all'inizio o alla fine dell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="2eabb-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="2eabb-272">Il valore **false** indica che l'ora di sistema non passa a un'ora avanti o indietro all'inizio o alla fine dell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="2eabb-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="2eabb-273">Il valore **null** indica che lo stato dell'ora legale è sconosciuto in un sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-274">**FrontPanelResetStatus**</span><span class="sxs-lookup"><span data-stu-id="2eabb-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-275">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-277">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| hardware Security Settings \| FrontPanelResetStatus")</span><span class="sxs-lookup"><span data-stu-id="2eabb-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-278">Nella tabella seguente sono elencate le impostazioni di sicurezza hardware per il pulsante Reimposta in un computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2eabb-279">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2eabb-280">**Abilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2eabb-281">**Non implementato** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-282">**Sconosciuto** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-283">**HypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="2eabb-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-284">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-286">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-287">Se **true**, è presente un hypervisor.</span><span class="sxs-lookup"><span data-stu-id="2eabb-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="2eabb-288">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2eabb-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-289">**InfraredSupported**</span><span class="sxs-lookup"><span data-stu-id="2eabb-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-290">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-292">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-293">Se **true**, una porta infrarossa (IR) è presente in un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-294">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="2eabb-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-295">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2eabb-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-297">Dati necessari per trovare il dispositivo di caricamento iniziale o il servizio di avvio per richiedere l'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2eabb-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="2eabb-298">Questa proprietà viene ereditata da [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="2eabb-299">**Windows Server 2008 R2:** Questa proprietà è disponibile, ma è vuota.</span><span class="sxs-lookup"><span data-stu-id="2eabb-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2eabb-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-301">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2eabb-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-303">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2eabb-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-304">L'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-304">Object is installed.</span></span> <span data-ttu-id="2eabb-305">Un oggetto non necessita di un valore per indicare che è installato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="2eabb-306">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-307">**KeyboardPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="2eabb-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-308">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-310">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| hardware Security Settings \| KeyboardPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="2eabb-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-311">Impostazioni di sicurezza hardware del sistema per lo stato della password della tastiera.</span><span class="sxs-lookup"><span data-stu-id="2eabb-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2eabb-312">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2eabb-313">**Abilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2eabb-314">**Non implementato** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-315">**Sconosciuto** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-316">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="2eabb-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-319">Voce di matrice della proprietà **InitialLoadInfo** che contiene i dati per avviare il sistema operativo caricato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="2eabb-320">Questa proprietà viene ereditata da [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-321">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="2eabb-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-324">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="2eabb-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-325">Nome di un produttore di computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="2eabb-326">Esempio: Adventure Works</span><span class="sxs-lookup"><span data-stu-id="2eabb-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-327">**Modello**</span><span class="sxs-lookup"><span data-stu-id="2eabb-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-330">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Product Name")</span><span class="sxs-lookup"><span data-stu-id="2eabb-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-331">Nome del prodotto assegnato a un computer da un produttore.</span><span class="sxs-lookup"><span data-stu-id="2eabb-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="2eabb-332">Questa proprietà deve avere un valore.</span><span class="sxs-lookup"><span data-stu-id="2eabb-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-333">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2eabb-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-336">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2eabb-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-337">Chiave di un'istanza di [**\_ sistema CIM**](cim-system.md) in un ambiente aziendale.</span><span class="sxs-lookup"><span data-stu-id="2eabb-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="2eabb-338">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-339">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="2eabb-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-342">Valore del **nome** di sistema del computer generato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2eabb-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="2eabb-343">L' [**oggetto \_ ComputerSystem CIM**](cim-computersystem.md) e i relativi derivati sono oggetti di primo livello del Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="2eabb-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="2eabb-344">Forniscono l'ambito per diversi componenti.</span><span class="sxs-lookup"><span data-stu-id="2eabb-344">They provide the scope for several components.</span></span> <span data-ttu-id="2eabb-345">Sono necessarie chiavi di [**\_ sistema CIM**](cim-system.md) univoche, ma è possibile definire un approccio euristico per creare il nome **\_ ComputerSystem CIM** che genera lo stesso nome ed è indipendente dal protocollo di individuazione.</span><span class="sxs-lookup"><span data-stu-id="2eabb-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="2eabb-346">In questo modo si evitano problemi di inventario e gestione quando lo stesso asset o entità viene individuato più volte, ma non può essere risolto in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="2eabb-347">L'uso di un'euristica è consigliato, ma non obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2eabb-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="2eabb-348">L'euristica è illustrata nella specifica del modello comune CIM V2 e presuppone che le regole documentate vengano usate per determinare e assegnare un nome.</span><span class="sxs-lookup"><span data-stu-id="2eabb-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="2eabb-349">L'elenco di valori **NameFormat** definisce l'ordine di assegnazione di un nome di sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="2eabb-350">Diverse regole sono mappate allo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="2eabb-350">Several rules map to the same value.</span></span>

<span data-ttu-id="2eabb-351">Il valore del [**\_ nome CIM ComputerSystem**](cim-computersystem.md) calcolato mediante l'euristica è il valore chiave del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="2eabb-352">Tuttavia, usare gli alias per assegnare un nome diverso per **CIM \_ ComputerSystem**, che può essere più univoco per l'azienda.</span><span class="sxs-lookup"><span data-stu-id="2eabb-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="2eabb-353">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="2eabb-354">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2eabb-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="2eabb-355">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="2eabb-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="2eabb-356">**Dial** ("dial")</span><span class="sxs-lookup"><span data-stu-id="2eabb-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="2eabb-357">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="2eabb-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="2eabb-358">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="2eabb-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="2eabb-359">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="2eabb-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="2eabb-360">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="2eabb-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="2eabb-361">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="2eabb-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="2eabb-362">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="2eabb-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="2eabb-363">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="2eabb-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="2eabb-364">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="2eabb-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="2eabb-365">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="2eabb-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="2eabb-366">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="2eabb-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="2eabb-367">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eabb-368">**Altro** ("altro")</span><span class="sxs-lookup"><span data-stu-id="2eabb-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-369">**NetworkServerModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="2eabb-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-370">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-372">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ tipo \| SV \_ server di tipo \_ ")</span><span class="sxs-lookup"><span data-stu-id="2eabb-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-373">Se **true**, la modalità server di rete è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2eabb-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-374">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="2eabb-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-375">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2eabb-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-377">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-378">Numero di processori logici disponibili nel computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="2eabb-379">È possibile usare **NumberOfLogicalProcessors** e **NumberOfProcessors** per determinare se il computer è Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="2eabb-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="2eabb-380">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2eabb-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="2eabb-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-382">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2eabb-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-384">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")</span><span class="sxs-lookup"><span data-stu-id="2eabb-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-385">Numero di processori fisici attualmente disponibili in un sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="2eabb-386">Il numero di processori abilitati per un sistema, che non include i processori disabilitati.</span><span class="sxs-lookup"><span data-stu-id="2eabb-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="2eabb-387">Se un sistema di computer dispone di due processori fisici ognuno dei quali contiene due processori logici, il valore di **NumberOfProcessors** è 2 e **NumberOfLogicalProcessors** è 4.</span><span class="sxs-lookup"><span data-stu-id="2eabb-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="2eabb-388">È possibile che i processori siano multicore o che siano processori Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="2eabb-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="2eabb-389">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2eabb-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-390">**OEMLogoBitmap**</span><span class="sxs-lookup"><span data-stu-id="2eabb-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-391">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2eabb-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-393">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-394">Elenco di dati per una bitmap creata dall'OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="2eabb-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-395">**OEMStringArray**</span><span class="sxs-lookup"><span data-stu-id="2eabb-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-396">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2eabb-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-398">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 11 \| OEM Strings")</span><span class="sxs-lookup"><span data-stu-id="2eabb-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-399">Elenco di stringhe in formato libero definite da un OEM.</span><span class="sxs-lookup"><span data-stu-id="2eabb-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="2eabb-400">Ad esempio, un OEM definisce i numeri di parte per i documenti di riferimento di sistema, le informazioni di contatto del produttore e così via.</span><span class="sxs-lookup"><span data-stu-id="2eabb-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-401">**PartOfDomain**</span><span class="sxs-lookup"><span data-stu-id="2eabb-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-402">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-404">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2eabb-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-405">Se **true**, il computer fa parte di un dominio.</span><span class="sxs-lookup"><span data-stu-id="2eabb-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="2eabb-406">Se il valore è **null**, il computer non si trova in un dominio o lo stato è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="2eabb-407">Se si rimuove il computer da un dominio, il valore diventa **false**.</span><span class="sxs-lookup"><span data-stu-id="2eabb-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-408">**PauseAfterReset**</span><span class="sxs-lookup"><span data-stu-id="2eabb-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-409">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="2eabb-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-411">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 \| timeout"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="2eabb-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-412">Tempo di attesa prima dell'avvio di un riavvio in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="2eabb-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="2eabb-413">Viene usato dopo un ciclo di alimentazione del sistema, una reimpostazione del sistema locale o remota e la reimpostazione automatica del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="2eabb-414">Il valore 1 (meno uno) indica che il valore di pausa è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="2eabb-415">**Windows Vista:** Questa proprietà può restituire un numero sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-416">**PCSystemType**</span><span class="sxs-lookup"><span data-stu-id="2eabb-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-417">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-419">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2eabb-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-420">Tipo di computer in uso, ad esempio portatile, desktop o tablet.</span><span class="sxs-lookup"><span data-stu-id="2eabb-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="2eabb-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>Non **specificato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="2eabb-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="2eabb-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Dispositivi mobili** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="2eabb-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="2eabb-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Server aziendale** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="2eabb-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Server Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-427">Server Small Office e Home Office (SOHO)</span><span class="sxs-lookup"><span data-stu-id="2eabb-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="2eabb-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC Appliance** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="2eabb-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Server prestazioni** (7)</span><span class="sxs-lookup"><span data-stu-id="2eabb-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="2eabb-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (8)</span><span class="sxs-lookup"><span data-stu-id="2eabb-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-431">**PCSystemTypeEx**</span><span class="sxs-lookup"><span data-stu-id="2eabb-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-432">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-434">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2eabb-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-435">Tipo di computer in uso, ad esempio portatile, desktop o tablet.</span><span class="sxs-lookup"><span data-stu-id="2eabb-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="2eabb-436">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2eabb-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="2eabb-437">Non **specificato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="2eabb-438">**Desktop** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="2eabb-439">**Dispositivi mobili** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="2eabb-440">**Workstation** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="2eabb-441">**Server aziendale** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="2eabb-442">**Server Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="2eabb-443">**PC Appliance** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="2eabb-444">**Server prestazioni** (7)</span><span class="sxs-lookup"><span data-stu-id="2eabb-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="2eabb-445">**Ardesia** (8)</span><span class="sxs-lookup"><span data-stu-id="2eabb-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="2eabb-446">**Massimo** (9)</span><span class="sxs-lookup"><span data-stu-id="2eabb-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-447">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2eabb-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-448">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-450">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controlli di alimentazione del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2eabb-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-451">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2eabb-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2eabb-452">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="2eabb-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2eabb-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2eabb-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2eabb-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-457">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="2eabb-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2eabb-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-459">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="2eabb-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2eabb-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-461">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2eabb-462">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2eabb-463">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2eabb-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2eabb-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-465">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="2eabb-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2eabb-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="2eabb-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-467">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="2eabb-467">Timed Power-On Supported</span></span>

<span data-ttu-id="2eabb-468">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="2eabb-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-469">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2eabb-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-470">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2eabb-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-471">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-472">Se **true**, il dispositivo può essere gestito dal risparmio energia, ad esempio, un dispositivo può essere messo in modalità di sospensione e così via.</span><span class="sxs-lookup"><span data-stu-id="2eabb-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="2eabb-473">Questa proprietà non indica che attualmente le funzionalità di risparmio energia sono abilitate, ma indica che il dispositivo logico è in grado di gestire il risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2eabb-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="2eabb-474">Questa proprietà viene ereditata da [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-475">**PowerOnPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="2eabb-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-476">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-478">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| hardware Security Settings \| PowerOnPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="2eabb-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-479">Impostazioni di sicurezza hardware del sistema per lo stato della password Power-On.</span><span class="sxs-lookup"><span data-stu-id="2eabb-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2eabb-480">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2eabb-481">**Abilitato** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2eabb-482">**Non implementato** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-483">**Sconosciuto** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-484">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="2eabb-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-485">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-487">Stato di alimentazione corrente di un computer e del sistema operativo associato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="2eabb-488">Gli Stati di risparmio energia hanno i valori seguenti: valore 4 (sconosciuto) indica che il sistema è in modalità di risparmio energia, ma lo stato esatto in questa modalità è sconosciuto. 2 (modalità a basso consumo) indica che il sistema è in uno stato di risparmio energia, ma funziona comunque e può presentare prestazioni ridotte. 3 (standby) indica che il sistema non funziona, ma può essere portato a una potenza completa rapidamente; e 7 (avviso) indica che il sistema del computer è in stato di avviso e in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2eabb-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="2eabb-489">Questa proprietà viene ereditata da [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="2eabb-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potenza completa** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2eabb-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2eabb-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2eabb-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2eabb-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2eabb-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (6** )</span><span class="sxs-lookup"><span data-stu-id="2eabb-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2eabb-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (7)</span><span class="sxs-lookup"><span data-stu-id="2eabb-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="2eabb-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Risparmio energia-ibernazione** (8)</span><span class="sxs-lookup"><span data-stu-id="2eabb-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-499">Ibernazione risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="2eabb-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="2eabb-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Risparmio energia-soft off** (9)</span><span class="sxs-lookup"><span data-stu-id="2eabb-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-501">Risparmio energia Soft disattivato.</span><span class="sxs-lookup"><span data-stu-id="2eabb-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-502">**PowerSupplyState**</span><span class="sxs-lookup"><span data-stu-id="2eabb-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-503">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-505">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 3 \| enclosure di sistema o \| stato alimentatore chassis")</span><span class="sxs-lookup"><span data-stu-id="2eabb-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-506">Stato dell'alimentatore o fornisce al momento dell'ultimo avvio.</span><span class="sxs-lookup"><span data-stu-id="2eabb-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="2eabb-507">Questo valore deriva dal membro **dello stato** di alimentazione dell' **enclosure di sistema o** dalla struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2eabb-508">Nell'elenco seguente vengono identificati i valori per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2eabb-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eabb-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="2eabb-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Sicuro** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2eabb-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2eabb-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="2eabb-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non reversibile** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-515">Irreversibile</span><span class="sxs-lookup"><span data-stu-id="2eabb-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-516">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="2eabb-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-517">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-518">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-519">Informazioni di contatto per il proprietario del sistema primario, ad esempio il numero di telefono, l'indirizzo di posta elettronica e così via.</span><span class="sxs-lookup"><span data-stu-id="2eabb-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="2eabb-520">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-521">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="2eabb-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-522">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-523">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-524">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2eabb-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-525">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="2eabb-525">Name of the primary system owner.</span></span>

<span data-ttu-id="2eabb-526">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-527">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="2eabb-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-528">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-529">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-530">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sicurezza hardware del sistema DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="2eabb-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-531">Se abilitata, il valore è 4 e il sistema del computer può essere reimpostato usando i pulsanti di accensione e ripristino.</span><span class="sxs-lookup"><span data-stu-id="2eabb-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="2eabb-532">Se disabilitato, il valore è 3 e non è consentita la reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="2eabb-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="2eabb-533">Questa proprietà viene ereditata da [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eabb-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2eabb-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2eabb-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2eabb-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Non implementato** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2eabb-539">Irreversibile</span><span class="sxs-lookup"><span data-stu-id="2eabb-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-540">**ResetCount**</span><span class="sxs-lookup"><span data-stu-id="2eabb-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-541">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-543">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 ripristino \| sistema Reimposta \| numero")</span><span class="sxs-lookup"><span data-stu-id="2eabb-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-544">Numero di reimpostazioni automatiche dall'ultima reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="2eabb-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="2eabb-545">Il valore 1 (meno uno) indica che il conteggio è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-546">**ResetLimit**</span><span class="sxs-lookup"><span data-stu-id="2eabb-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-547">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-549">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 Reset \| System Reset \| limite")</span><span class="sxs-lookup"><span data-stu-id="2eabb-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-550">Numero di volte consecutive in cui viene effettuato un tentativo di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="2eabb-551">Il valore 1 (meno uno) indica che il limite è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-552">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="2eabb-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-553">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2eabb-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-554">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-555">Elenco che specifica i ruoli di un sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="2eabb-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="2eabb-556">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-557">**Status**</span><span class="sxs-lookup"><span data-stu-id="2eabb-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-558">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-559">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-560">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2eabb-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-561">Stato corrente di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-561">Current status of an object.</span></span>

<span data-ttu-id="2eabb-562">Per Win32_ComputerSystem, lo stato è sempre "OK".</span><span class="sxs-lookup"><span data-stu-id="2eabb-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="2eabb-563">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="2eabb-564">**SupportContactDescription**</span><span class="sxs-lookup"><span data-stu-id="2eabb-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-565">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2eabb-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-566">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-567">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("informazioni di supporto per Win32API \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| ")</span><span class="sxs-lookup"><span data-stu-id="2eabb-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-568">Elenco delle informazioni di contatto del supporto tecnico per il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2eabb-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-569">**SystemFamily**</span><span class="sxs-lookup"><span data-stu-id="2eabb-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-570">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-571">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-572">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Family")</span><span class="sxs-lookup"><span data-stu-id="2eabb-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-573">Famiglia a cui appartiene un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="2eabb-574">Una famiglia si riferisce a un set di computer simili, ma non identici, da un punto di vista hardware o software.</span><span class="sxs-lookup"><span data-stu-id="2eabb-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="2eabb-575">Questo valore deriva dal membro della **famiglia** della struttura delle **informazioni di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2eabb-576">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2eabb-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-577">**SystemSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="2eabb-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-578">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-579">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-580">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 1 \| informazioni di sistema \| numero SKU")</span><span class="sxs-lookup"><span data-stu-id="2eabb-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-581">Identifica una particolare configurazione del computer per la vendita.</span><span class="sxs-lookup"><span data-stu-id="2eabb-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="2eabb-582">Viene talvolta definito anche un ID prodotto o un numero di ordine di acquisto.</span><span class="sxs-lookup"><span data-stu-id="2eabb-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="2eabb-583">Questo valore deriva dal membro del **numero di SKU** della struttura delle informazioni di **sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2eabb-584">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2eabb-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-585">**SystemStartupDelay**</span><span class="sxs-lookup"><span data-stu-id="2eabb-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-586">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-587">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-588">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilegi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| boot loader \| timeout"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span><span class="sxs-lookup"><span data-stu-id="2eabb-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-589">**SystemStartupDelay** non è più disponibile per l'uso perché Boot.ini non viene usato per configurare l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="2eabb-590">Utilizzare invece le [classi BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornite dal provider WMI dati configurazione di avvio (BCD) o dal comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="2eabb-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-591">**SystemStartupOptions**</span><span class="sxs-lookup"><span data-stu-id="2eabb-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-592">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2eabb-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-593">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-594">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")</span><span class="sxs-lookup"><span data-stu-id="2eabb-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-595">**SystemStartupOptions** non è più disponibile per l'uso perché Boot.ini non viene usato per configurare l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="2eabb-596">Utilizzare invece le [classi BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornite dal provider WMI dati configurazione di avvio (BCD) o dal comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="2eabb-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-597">**SystemStartupSetting**</span><span class="sxs-lookup"><span data-stu-id="2eabb-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-598">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2eabb-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-599">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-600">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilegi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2eabb-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-601">**SystemStartupSetting** non è più disponibile per l'uso perché Boot.ini non viene usato per configurare l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="2eabb-602">Utilizzare invece le [classi BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornite dal provider WMI dati configurazione di avvio (BCD) o dal comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="2eabb-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-603">**SystemType**</span><span class="sxs-lookup"><span data-stu-id="2eabb-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-604">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-605">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-606">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")</span><span class="sxs-lookup"><span data-stu-id="2eabb-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-607">Sistema in esecuzione nel computer basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="2eabb-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="2eabb-608">Questa proprietà deve avere un valore.</span><span class="sxs-lookup"><span data-stu-id="2eabb-608">This property must have a value.</span></span>

<span data-ttu-id="2eabb-609">Nell'elenco seguente vengono identificati alcuni dei valori possibili per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2eabb-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="2eabb-610">"PC basato su x64"</span><span class="sxs-lookup"><span data-stu-id="2eabb-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="2eabb-611">"PC basato su x86"</span><span class="sxs-lookup"><span data-stu-id="2eabb-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="2eabb-612">"PC basato su MIPS"</span><span class="sxs-lookup"><span data-stu-id="2eabb-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="2eabb-613">"PC basato su Alpha"</span><span class="sxs-lookup"><span data-stu-id="2eabb-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="2eabb-614">"Power PC"</span><span class="sxs-lookup"><span data-stu-id="2eabb-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="2eabb-615">"SH-x PC"</span><span class="sxs-lookup"><span data-stu-id="2eabb-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="2eabb-616">"StrongARM PC"</span><span class="sxs-lookup"><span data-stu-id="2eabb-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="2eabb-617">"Intel PC a 64 bit"</span><span class="sxs-lookup"><span data-stu-id="2eabb-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="2eabb-618">"PC Alpha a 64 bit"</span><span class="sxs-lookup"><span data-stu-id="2eabb-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="2eabb-619">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="2eabb-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="2eabb-620">"X86-Nec98 PC"</span><span class="sxs-lookup"><span data-stu-id="2eabb-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="2eabb-621">**PC basato su x86** ("PC basati su x86")</span><span class="sxs-lookup"><span data-stu-id="2eabb-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="2eabb-622">**PC basato su MIPS** ("PC basato su MIPS")</span><span class="sxs-lookup"><span data-stu-id="2eabb-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="2eabb-623">**PC basato su Alpha** ("PC basati su Alpha")</span><span class="sxs-lookup"><span data-stu-id="2eabb-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="2eabb-624">**Power PC** ("Power PC")</span><span class="sxs-lookup"><span data-stu-id="2eabb-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="2eabb-625">**PC SH-x** ("sh-x PC")</span><span class="sxs-lookup"><span data-stu-id="2eabb-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="2eabb-626">**STRONGARM PC** ("StrongARM PC")</span><span class="sxs-lookup"><span data-stu-id="2eabb-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="2eabb-627">**Intel PC a 64 bit** ("PC intel a 64 bit")</span><span class="sxs-lookup"><span data-stu-id="2eabb-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="2eabb-628">**PC basato su x64** ("PC basati su x64")</span><span class="sxs-lookup"><span data-stu-id="2eabb-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-629">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2eabb-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="2eabb-630">**X86-NEC98 PC** ("x86-Nec98 PC")</span><span class="sxs-lookup"><span data-stu-id="2eabb-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-631">**ThermalState**</span><span class="sxs-lookup"><span data-stu-id="2eabb-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-632">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-633">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-634">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 3 \| enclosure di sistema o \| stato termico chassis")</span><span class="sxs-lookup"><span data-stu-id="2eabb-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-635">Stato termico del sistema al momento dell'ultimo avvio.</span><span class="sxs-lookup"><span data-stu-id="2eabb-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="2eabb-636">Questo valore deriva dal membro di **stato termico** dell' **enclosure di sistema o** della struttura dello chassis nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eabb-637">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-638">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="2eabb-639">**Sicuro** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2eabb-640">**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2eabb-641">**Critico** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="2eabb-642">**Non reversibile** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="2eabb-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-644">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2eabb-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-645">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-646">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2eabb-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-647">Dimensioni totali della memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="2eabb-647">Total size of physical memory.</span></span> <span data-ttu-id="2eabb-648">Tenere presente che, in alcune circostanze, questa proprietà non può restituire un valore esatto per la memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="2eabb-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="2eabb-649">Ad esempio, non è accurato se il BIOS utilizza parte della memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="2eabb-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="2eabb-650">Per un valore accurato, usare invece la proprietà **Capacity** in [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="2eabb-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="2eabb-651">Esempio: 67108864</span><span class="sxs-lookup"><span data-stu-id="2eabb-651">Example: 67108864</span></span>

<span data-ttu-id="2eabb-652">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2eabb-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-653">**UserName**</span><span class="sxs-lookup"><span data-stu-id="2eabb-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-654">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-655">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-656">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Functions \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span><span class="sxs-lookup"><span data-stu-id="2eabb-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-657">Nome di un utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="2eabb-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="2eabb-658">Questa proprietà deve avere un valore.</span><span class="sxs-lookup"><span data-stu-id="2eabb-658">This property must have a value.</span></span> <span data-ttu-id="2eabb-659">In una sessione di Servizi terminal, **username** restituisce il nome dell'utente che ha effettuato l'accesso alla console di non l'utente connesso durante la sessione del servizio terminal.</span><span class="sxs-lookup"><span data-stu-id="2eabb-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="2eabb-660">Esempio: SergioMelchiori</span><span class="sxs-lookup"><span data-stu-id="2eabb-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="2eabb-661">**WakeUpType**</span><span class="sxs-lookup"><span data-stu-id="2eabb-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-662">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eabb-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-663">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2eabb-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-664">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 1 \| informazioni di sistema tipo \| di riattivazione")</span><span class="sxs-lookup"><span data-stu-id="2eabb-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-665">Evento che determina l'accensione del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eabb-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="2eabb-666">Questo valore deriva dal membro del **tipo di riattivazione** della struttura delle **informazioni di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2eabb-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2eabb-667">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="2eabb-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eabb-668">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eabb-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eabb-669">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2eabb-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="2eabb-670">**Timer APM** (3)</span><span class="sxs-lookup"><span data-stu-id="2eabb-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="2eabb-671">**Anello modem** (4)</span><span class="sxs-lookup"><span data-stu-id="2eabb-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="2eabb-672">**LAN remota** (5)</span><span class="sxs-lookup"><span data-stu-id="2eabb-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="2eabb-673">**Interruttore di alimentazione** (6)</span><span class="sxs-lookup"><span data-stu-id="2eabb-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="2eabb-674">**PME \# PCI** 7</span><span class="sxs-lookup"><span data-stu-id="2eabb-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="2eabb-675">**Alimentazione CA ripristinata** (8)</span><span class="sxs-lookup"><span data-stu-id="2eabb-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2eabb-676">**Gruppo di lavoro**</span><span class="sxs-lookup"><span data-stu-id="2eabb-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eabb-677">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2eabb-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-678">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2eabb-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2eabb-679">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2eabb-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2eabb-680">Nome del gruppo di lavoro per questo computer.</span><span class="sxs-lookup"><span data-stu-id="2eabb-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="2eabb-681">Se il valore della proprietà **PartOfDomain** è **false**, viene restituito il nome del gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2eabb-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eabb-682">Commenti</span><span class="sxs-lookup"><span data-stu-id="2eabb-682">Remarks</span></span>

<span data-ttu-id="2eabb-683">Per determinare il numero totale di istanze del processore associate a un oggetto di sistema del computer, utilizzare la classe di associazione [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="2eabb-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="2eabb-684">A un'istanza **Win32 \_ ComputerSystem** con più processori fisici sono associate più istanze del [**\_ processore Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="2eabb-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="2eabb-685">Se il valore di **NumberOfLogicalProcessors** è maggiore del valore di **NumberOfProcessors** , il computer è un sistema multicore oppure uno o più processori sono abilitati per l'Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="2eabb-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="2eabb-686">Per ulteriori informazioni, vedere la sezione proprietà e osservazioni di **NumberOfLogicalProcessors** e **NumberOfCores** nel **\_ processore Win32**.</span><span class="sxs-lookup"><span data-stu-id="2eabb-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="2eabb-687">La classe **Win32 \_ ComputerSystem** è derivata da [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2eabb-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2eabb-688">Esempio</span><span class="sxs-lookup"><span data-stu-id="2eabb-688">Examples</span></span>

<span data-ttu-id="2eabb-689">Il seguente [esempio di codice](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) di Scripting Center USA **Win32 \_ ComputerSystem** per recuperare informazioni da un certo numero di sistemi di computer e visualizzarli in un'interfaccia utente grafica.</span><span class="sxs-lookup"><span data-stu-id="2eabb-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="2eabb-690">È possibile trovare uno script di esempio che ottiene dati del sistema operativo e del processore da **Win32 \_ ComputerSystem**, [**\_ processore Win32**](win32-processor.md)e [**\_ OperatingSystem Win32**](win32-operatingsystem.md) negli esempi di argomenti del [**\_ processore Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="2eabb-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="2eabb-691">Nell'esempio VBScript seguente viene descritto come recuperare il nome di dominio del computer locale da istanze di **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="2eabb-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="2eabb-692">Nell'esempio Perl seguente viene descritto come recuperare il nome del computer locale da istanze di **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="2eabb-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="2eabb-693">Nell'esempio Perl seguente viene descritto come recuperare il nome di dominio DNS del computer locale da istanze di **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="2eabb-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="2eabb-694">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2eabb-694">Requirements</span></span>



| <span data-ttu-id="2eabb-695">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eabb-695">Requirement</span></span> | <span data-ttu-id="2eabb-696">Valore</span><span class="sxs-lookup"><span data-stu-id="2eabb-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eabb-697">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eabb-697">Minimum supported client</span></span><br/> | <span data-ttu-id="2eabb-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2eabb-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2eabb-699">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eabb-699">Minimum supported server</span></span><br/> | <span data-ttu-id="2eabb-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eabb-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2eabb-701">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2eabb-701">Namespace</span></span><br/>                | <span data-ttu-id="2eabb-702">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2eabb-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2eabb-703">MOF</span><span class="sxs-lookup"><span data-stu-id="2eabb-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eabb-704"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eabb-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eabb-705">DLL</span><span class="sxs-lookup"><span data-stu-id="2eabb-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eabb-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eabb-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eabb-707">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2eabb-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eabb-708">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="2eabb-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="2eabb-709">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2eabb-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2eabb-710">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="2eabb-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2eabb-711">Attività WMI: hardware del computer</span><span class="sxs-lookup"><span data-stu-id="2eabb-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="2eabb-712">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="2eabb-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 


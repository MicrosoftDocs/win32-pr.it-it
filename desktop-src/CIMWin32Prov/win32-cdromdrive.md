---
description: Rappresenta un'unità CD-ROM in un computer in cui è in esecuzione Windows.
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Classe Win32_CDROMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966273"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="e096d-103">Win32 \_ CDROMDrive (classe)</span><span class="sxs-lookup"><span data-stu-id="e096d-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="e096d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CDROMDrive Win32** rappresenta un'unità CD-ROM in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="e096d-105">Tenere presente che il nome dell'unità non corrisponde alla lettera di unità logica assegnata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="e096d-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e096d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e096d-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e096d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e096d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e096d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="e096d-109">Members</span><span class="sxs-lookup"><span data-stu-id="e096d-109">Members</span></span>

<span data-ttu-id="e096d-110">La classe **Win32 \_ CDROMDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e096d-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="e096d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e096d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e096d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e096d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e096d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e096d-113">Methods</span></span>

<span data-ttu-id="e096d-114">La classe **Win32 \_ CDROMDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e096d-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="e096d-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="e096d-115">Method</span></span>            | <span data-ttu-id="e096d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e096d-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e096d-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="e096d-117">**Reset**</span></span>         | <span data-ttu-id="e096d-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="e096d-118">Not implemented.</span></span> <span data-ttu-id="e096d-119">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ CDROMDrive**](cim-cdromdrive.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="e096d-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="e096d-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e096d-120">**SetPowerState**</span></span> | <span data-ttu-id="e096d-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="e096d-121">Not implemented.</span></span> <span data-ttu-id="e096d-122">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ CDROMDrive**](cim-cdromdrive.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="e096d-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e096d-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e096d-123">Properties</span></span>

<span data-ttu-id="e096d-124">La classe **Win32 \_ CDROMDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e096d-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e096d-125">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="e096d-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e096d-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-129">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-129">Availability and status of the device.</span></span>

<span data-ttu-id="e096d-130">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e096d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e096d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e096d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="e096d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e096d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="e096d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-134">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="e096d-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e096d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="e096d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e096d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="e096d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e096d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="e096d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e096d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="e096d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e096d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="e096d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e096d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="e096d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e096d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="e096d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e096d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="e096d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e096d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="e096d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e096d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="e096d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e096d-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e096d-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="e096d-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="e096d-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e096d-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="e096d-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e096d-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e096d-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="e096d-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e096d-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="e096d-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="e096d-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e096d-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="e096d-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="e096d-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e096d-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="e096d-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="e096d-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e096d-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="e096d-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="e096d-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e096d-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="e096d-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="e096d-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e096d-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-162">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e096d-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-164">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="e096d-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-165">Matrice di funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="e096d-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="e096d-166">Ad esempio, il dispositivo può supportare l'accesso casuale (3), i supporti rimovibili (7) e la pulizia automatica (9).</span><span class="sxs-lookup"><span data-stu-id="e096d-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="e096d-167">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e096d-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e096d-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e096d-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e096d-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="e096d-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="e096d-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="e096d-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="e096d-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="e096d-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="e096d-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="e096d-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="e096d-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="e096d-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="e096d-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="e096d-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="e096d-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-176">Supporta supporti rimovibili</span><span class="sxs-lookup"><span data-stu-id="e096d-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="e096d-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="e096d-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="e096d-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="e096d-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="e096d-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="e096d-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="e096d-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="e096d-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-181">Supporta Dual-Sided supporti</span><span class="sxs-lookup"><span data-stu-id="e096d-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="e096d-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="e096d-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-183">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e096d-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-184">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e096d-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e096d-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-186">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="e096d-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-187">Matrice di spiegazioni più dettagliate per tutte le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="e096d-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="e096d-188">Ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="e096d-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="e096d-189">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-190">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e096d-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-193">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e096d-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-194">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="e096d-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="e096d-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-196">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="e096d-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-199">Algoritmo o strumento usato dal dispositivo per supportare la compressione.</span><span class="sxs-lookup"><span data-stu-id="e096d-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="e096d-200">Se non è possibile o non si desidera descrivere lo schema di compressione (probabilmente perché non è noto), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il dispositivo supporta le funzionalità di compressione; "Compresso" per indicare che il dispositivo supporta le funzionalità di compressione, ma lo schema di compressione non è noto o non è stato divulgato; e "non compressi" per indicare che il dispositivo non supporta le funzionalità di compressione.</span><span class="sxs-lookup"><span data-stu-id="e096d-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="e096d-201">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="e096d-202">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e096d-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="e096d-203">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="e096d-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="e096d-204">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="e096d-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="e096d-205">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="e096d-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="e096d-206">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="e096d-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="e096d-207">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="e096d-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-208">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e096d-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-209">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e096d-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-211">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e096d-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-212">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e096d-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="e096d-213">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e096d-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="e096d-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e096d-215"> (0)</span><span class="sxs-lookup"><span data-stu-id="e096d-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-216">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e096d-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e096d-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="e096d-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e096d-218">(1)</span><span class="sxs-lookup"><span data-stu-id="e096d-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-219">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e096d-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e096d-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e096d-221">(2)</span><span class="sxs-lookup"><span data-stu-id="e096d-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e096d-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="e096d-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e096d-223">(3)</span><span class="sxs-lookup"><span data-stu-id="e096d-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-224">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="e096d-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e096d-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="e096d-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e096d-226">(4)</span><span class="sxs-lookup"><span data-stu-id="e096d-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-227">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e096d-227">Device is not working properly.</span></span> <span data-ttu-id="e096d-228">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e096d-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e096d-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="e096d-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e096d-230">(5)</span><span class="sxs-lookup"><span data-stu-id="e096d-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-231">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="e096d-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e096d-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="e096d-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e096d-233"> (6)</span><span class="sxs-lookup"><span data-stu-id="e096d-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-234">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e096d-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e096d-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="e096d-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e096d-236">(7)</span><span class="sxs-lookup"><span data-stu-id="e096d-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e096d-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="e096d-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e096d-238">(8)</span><span class="sxs-lookup"><span data-stu-id="e096d-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-239">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="e096d-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e096d-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="e096d-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e096d-241">(9)</span><span class="sxs-lookup"><span data-stu-id="e096d-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-242">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e096d-242">Device is not working properly.</span></span> <span data-ttu-id="e096d-243">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e096d-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e096d-245">(10)</span><span class="sxs-lookup"><span data-stu-id="e096d-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-246">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e096d-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e096d-248">(11)</span><span class="sxs-lookup"><span data-stu-id="e096d-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-249">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e096d-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="e096d-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e096d-251">12</span><span class="sxs-lookup"><span data-stu-id="e096d-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-252">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="e096d-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e096d-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e096d-254">(13)</span><span class="sxs-lookup"><span data-stu-id="e096d-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-255">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e096d-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="e096d-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e096d-257">(14)</span><span class="sxs-lookup"><span data-stu-id="e096d-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-258">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="e096d-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e096d-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="e096d-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e096d-260">(15)</span><span class="sxs-lookup"><span data-stu-id="e096d-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-261">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="e096d-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e096d-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e096d-263">(16)</span><span class="sxs-lookup"><span data-stu-id="e096d-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-264">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e096d-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="e096d-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e096d-266">(17)</span><span class="sxs-lookup"><span data-stu-id="e096d-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-267">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e096d-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e096d-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e096d-269">(18)</span><span class="sxs-lookup"><span data-stu-id="e096d-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-270">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e096d-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="e096d-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e096d-272">(19)</span><span class="sxs-lookup"><span data-stu-id="e096d-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e096d-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="e096d-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e096d-274">(20)</span><span class="sxs-lookup"><span data-stu-id="e096d-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-275">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e096d-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e096d-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e096d-277">(21)</span><span class="sxs-lookup"><span data-stu-id="e096d-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-278">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="e096d-278">System failure.</span></span> <span data-ttu-id="e096d-279">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="e096d-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e096d-280">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e096d-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="e096d-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e096d-282">(22)</span><span class="sxs-lookup"><span data-stu-id="e096d-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-283">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e096d-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e096d-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="e096d-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e096d-285">(23)</span><span class="sxs-lookup"><span data-stu-id="e096d-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-286">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="e096d-286">System failure.</span></span> <span data-ttu-id="e096d-287">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="e096d-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e096d-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="e096d-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e096d-289">(24)</span><span class="sxs-lookup"><span data-stu-id="e096d-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-290">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="e096d-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e096d-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e096d-292">(25)</span><span class="sxs-lookup"><span data-stu-id="e096d-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-293">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e096d-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e096d-295">(26)</span><span class="sxs-lookup"><span data-stu-id="e096d-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-296">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e096d-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="e096d-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e096d-298">(27)</span><span class="sxs-lookup"><span data-stu-id="e096d-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-299">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="e096d-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e096d-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="e096d-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e096d-301">(28)</span><span class="sxs-lookup"><span data-stu-id="e096d-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-302">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="e096d-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e096d-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="e096d-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e096d-304">(29)</span><span class="sxs-lookup"><span data-stu-id="e096d-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-305">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e096d-305">Device is disabled.</span></span> <span data-ttu-id="e096d-306">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="e096d-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e096d-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e096d-308">(30)</span><span class="sxs-lookup"><span data-stu-id="e096d-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-309">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e096d-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e096d-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e096d-311">31</span><span class="sxs-lookup"><span data-stu-id="e096d-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-312">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="e096d-312">Device is not working properly.</span></span> <span data-ttu-id="e096d-313">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="e096d-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-314">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e096d-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-315">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e096d-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-317">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e096d-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-318">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e096d-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e096d-319">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-320">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e096d-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-323">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e096d-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e096d-324">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="e096d-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e096d-325">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="e096d-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="e096d-326">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-327">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="e096d-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-328">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e096d-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-330">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="e096d-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-331">Dimensioni del blocco predefinite, in byte, per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="e096d-332">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="e096d-333">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e096d-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-334">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e096d-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-335">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-337">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e096d-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-338">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e096d-338">Description of the object.</span></span>

<span data-ttu-id="e096d-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-340">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e096d-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-343">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetLogicalDriveStrings")</span><span class="sxs-lookup"><span data-stu-id="e096d-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-344">Identificatore univoco per un'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e096d-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="e096d-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-346">**Unità**</span><span class="sxs-lookup"><span data-stu-id="e096d-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-349">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="e096d-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-350">Lettera di unità dell'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e096d-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="e096d-351">Esempio: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="e096d-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="e096d-352">**DriveIntegrity**</span><span class="sxs-lookup"><span data-stu-id="e096d-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-353">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e096d-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-355">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e096d-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-356">Se **true**, i file possono essere letti accuratamente dal dispositivo CD.</span><span class="sxs-lookup"><span data-stu-id="e096d-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="e096d-357">Questa operazione viene eseguita leggendo un blocco di dati due volte e confrontando i dati con se stesso.</span><span class="sxs-lookup"><span data-stu-id="e096d-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-358">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e096d-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-359">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e096d-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-361">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="e096d-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e096d-362">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e096d-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-366">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="e096d-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="e096d-367">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-368">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="e096d-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-369">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-371">Tipo di rilevamento e correzione degli errori supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="e096d-372">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-373">**FileSystemFlags**</span><span class="sxs-lookup"><span data-stu-id="e096d-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-374">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-376">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="e096d-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-377">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="e096d-377">This property is obsolete.</span></span> <span data-ttu-id="e096d-378">Al posto di questa proprietà, usare **FileSystemFlagsEx**.</span><span class="sxs-lookup"><span data-stu-id="e096d-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-379">**FileSystemFlagsEx**</span><span class="sxs-lookup"><span data-stu-id="e096d-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-380">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e096d-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-382">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="e096d-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-383">Flag del file System associati all'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="e096d-384">Questo parametro può essere costituito da qualsiasi combinazione di flag, ma la **\_ \_ compressione dei file FS** e il **volume di FS \_ \_ è \_ compresso** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="e096d-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="e096d-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Ricerca con distinzione tra maiuscole** e minuscole (1)</span><span class="sxs-lookup"><span data-stu-id="e096d-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-386">Il file system supporta i nomi di file con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e096d-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="e096d-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Nomi dei case conservati** (2)</span><span class="sxs-lookup"><span data-stu-id="e096d-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-388">Il file system conserva il caso dei nomi file quando inserisce un nome su un disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="e096d-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode su disco** (4)</span><span class="sxs-lookup"><span data-stu-id="e096d-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-390">Il file system supporta il formato Unicode nei nomi file come appaiono sul disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="e096d-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**ACL permanenti** (8)</span><span class="sxs-lookup"><span data-stu-id="e096d-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-392">Il file system conserva e impone gli elenchi di controllo di accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="e096d-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="e096d-393">Il file system NTFS, ad esempio, consente di mantenere e applicare gli ACL e il file system FAT.</span><span class="sxs-lookup"><span data-stu-id="e096d-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="e096d-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Compressione file** (16)</span><span class="sxs-lookup"><span data-stu-id="e096d-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-395">Il file system supporta la compressione basata su file.</span><span class="sxs-lookup"><span data-stu-id="e096d-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="e096d-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Quote del volume** (32)</span><span class="sxs-lookup"><span data-stu-id="e096d-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-397">Il file system supporta le quote disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="e096d-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supporta file sparse** (64)</span><span class="sxs-lookup"><span data-stu-id="e096d-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-399">Il file system supporta i file di riserva.</span><span class="sxs-lookup"><span data-stu-id="e096d-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="e096d-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supporta i reparse point** (128)</span><span class="sxs-lookup"><span data-stu-id="e096d-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-401">Il file system supporta i reparse point.</span><span class="sxs-lookup"><span data-stu-id="e096d-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="e096d-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supporta l'archiviazione remota** (256)</span><span class="sxs-lookup"><span data-stu-id="e096d-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-403">Il file system supporta l'archiviazione remota dei file.</span><span class="sxs-lookup"><span data-stu-id="e096d-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="e096d-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supporta nomi lunghi** (16384)</span><span class="sxs-lookup"><span data-stu-id="e096d-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-405">Il file system supporta nomi di file con lunghezza superiore a otto caratteri.</span><span class="sxs-lookup"><span data-stu-id="e096d-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="e096d-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume compresso** (32768)</span><span class="sxs-lookup"><span data-stu-id="e096d-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-407">Il volume del disco specificato è un volume compresso, ad esempio, un volume DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="e096d-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="e096d-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Volume di sola lettura** (524289)</span><span class="sxs-lookup"><span data-stu-id="e096d-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-409">Il volume specificato è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e096d-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="e096d-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supporta gli ID oggetto** (65536)</span><span class="sxs-lookup"><span data-stu-id="e096d-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-411">Il file system supporta gli identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="e096d-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="e096d-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supporta la crittografia** (131072)</span><span class="sxs-lookup"><span data-stu-id="e096d-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-413">Il file system supporta il file system crittografato (EFS).</span><span class="sxs-lookup"><span data-stu-id="e096d-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="e096d-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supporta i flussi denominati** (262144)</span><span class="sxs-lookup"><span data-stu-id="e096d-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-415">Il file system supporta i flussi denominati.</span><span class="sxs-lookup"><span data-stu-id="e096d-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="e096d-416">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="e096d-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e096d-417">**Id**</span><span class="sxs-lookup"><span data-stu-id="e096d-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-420">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="e096d-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-421">Lettera di unità che identifica in modo univoco l'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e096d-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="e096d-422">Esempio: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="e096d-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="e096d-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e096d-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-424">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e096d-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-426">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="e096d-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-427">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e096d-427">Date and time the object is installed.</span></span> <span data-ttu-id="e096d-428">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="e096d-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e096d-429">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-430">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e096d-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-431">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e096d-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-433">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e096d-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e096d-434">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-435">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="e096d-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-438">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="e096d-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-439">Produttore dell'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="e096d-440">Esempio: "PLEXTOR"</span><span class="sxs-lookup"><span data-stu-id="e096d-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="e096d-441">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="e096d-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-442">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e096d-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-444">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="e096d-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-445">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="e096d-446">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="e096d-447">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e096d-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-448">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="e096d-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-449">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e096d-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-451">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="e096d-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-452">Lunghezza massima di un componente filename supportato dall'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="e096d-453">Componente del nome file la parte di un nome file tra le barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="e096d-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="e096d-454">Il valore può essere utilizzato per indicare che i nomi lunghi sono supportati dal file system specificato.</span><span class="sxs-lookup"><span data-stu-id="e096d-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="e096d-455">Ad esempio, per un file system FAT che supporta nomi lunghi, la funzione archivia il valore 255, anziché l'indicatore 8,3 precedente.</span><span class="sxs-lookup"><span data-stu-id="e096d-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="e096d-456">I nomi lunghi possono inoltre essere supportati nei sistemi che utilizzano il file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="e096d-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="e096d-457">Esempio: 255</span><span class="sxs-lookup"><span data-stu-id="e096d-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="e096d-458">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="e096d-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-459">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e096d-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-461">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="e096d-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-462">Dimensioni massime, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="e096d-463">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="e096d-464">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e096d-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-465">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="e096d-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-466">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e096d-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-468">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="e096d-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-469">Se **true**, un CD-ROM si trova nell'unità.</span><span class="sxs-lookup"><span data-stu-id="e096d-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-470">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="e096d-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-471">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-473">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="e096d-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-474">Tipo di supporto che può essere usato o accessibile da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="e096d-475">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="e096d-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="e096d-476">**Accesso casuale** ("accesso casuale")</span><span class="sxs-lookup"><span data-stu-id="e096d-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="e096d-477">**Supporta la scrittura** ("supporta la scrittura")</span><span class="sxs-lookup"><span data-stu-id="e096d-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="e096d-478">**Supporti** rimovibili ("supporti rimovibili")</span><span class="sxs-lookup"><span data-stu-id="e096d-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="e096d-479">**CD-ROM** ("CD-ROM")</span><span class="sxs-lookup"><span data-stu-id="e096d-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-480">**MfrAssignedRevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="e096d-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-481">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-483">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK \| KernelModeDrivers \| [**storage \_ Device \_ descrittor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="e096d-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-484">Livello di revisione del firmware assegnato dal produttore.</span><span class="sxs-lookup"><span data-stu-id="e096d-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-485">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="e096d-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-486">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e096d-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-488">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="e096d-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-489">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="e096d-490">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="e096d-491">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e096d-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-492">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e096d-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-493">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-494">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-495">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e096d-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-496">Etichetta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e096d-496">Label for the object.</span></span> <span data-ttu-id="e096d-497">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="e096d-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e096d-498">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-499">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="e096d-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-500">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e096d-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-501">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-502">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="e096d-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="e096d-503">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="e096d-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="e096d-504">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-505">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="e096d-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-506">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e096d-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-508">Numero massimo di supporti che possono essere supportati o inseriti quando il dispositivo di accesso ai supporti supporta più singoli supporti.</span><span class="sxs-lookup"><span data-stu-id="e096d-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="e096d-509">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e096d-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-511">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-513">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e096d-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-514">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e096d-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e096d-515">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e096d-516">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e096d-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e096d-517">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e096d-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-518">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e096d-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-520">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e096d-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e096d-521">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="e096d-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e096d-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e096d-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e096d-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="e096d-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-524">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e096d-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e096d-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="e096d-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e096d-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e096d-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-527">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="e096d-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e096d-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="e096d-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-529">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="e096d-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e096d-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="e096d-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-531">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="e096d-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e096d-532">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="e096d-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e096d-533">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e096d-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e096d-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="e096d-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-535">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="e096d-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e096d-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="e096d-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e096d-537">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="e096d-537">Timed Power-On Supported</span></span>

<span data-ttu-id="e096d-538">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="e096d-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-539">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e096d-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-540">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e096d-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-541">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e096d-542">Se **true**, il dispositivo può essere gestito dal risparmio energia, il che significa che può essere messo in modalità di sospensione e così via.</span><span class="sxs-lookup"><span data-stu-id="e096d-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="e096d-543">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="e096d-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="e096d-544">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-545">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="e096d-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-546">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-547">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-548">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| RevisionLevel")</span><span class="sxs-lookup"><span data-stu-id="e096d-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-549">Livello di revisione del firmware dell'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="e096d-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-551">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e096d-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-552">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-553">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| strutture SCSI Win32API \| [**\_ \_ blocco richieste SCSI**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| PathId")</span><span class="sxs-lookup"><span data-stu-id="e096d-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-554">Numero del bus SCSI per l'unità disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="e096d-555">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="e096d-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e096d-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="e096d-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-557">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-558">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-559">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| strutture SCSI Win32API per \| [**\_ \_ blocchi di richieste SCSI**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ")</span><span class="sxs-lookup"><span data-stu-id="e096d-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-560">Numero di unità logica (LUN) SCSI dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="e096d-561">Il numero di unità logica viene usato per definire quale controller SCSI viene usato in un sistema con più di un controller in uso.</span><span class="sxs-lookup"><span data-stu-id="e096d-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="e096d-562">L'identificatore del dispositivo SCSI è simile, ma è la designazione per più dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="e096d-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="e096d-563">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="e096d-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e096d-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="e096d-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-565">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-566">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-567">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| strutture SCSI Win32API \| [**\_ \_ blocco richieste SCSI**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ScsiStatus")</span><span class="sxs-lookup"><span data-stu-id="e096d-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-568">Numero di porta SCSI dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="e096d-569">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="e096d-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="e096d-570">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="e096d-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-571">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-572">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-573">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| DeviceIoControl \| IOCTL \_ SCSI \_ get \_ Address")</span><span class="sxs-lookup"><span data-stu-id="e096d-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-574">Numero dell'identificatore SCSI dell'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="e096d-575">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="e096d-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e096d-576">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e096d-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-577">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-578">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-579">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="e096d-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-580">Numero fornito dal produttore che identifica i supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="e096d-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="e096d-581">Esempio: WD-WM3493798728.</span><span class="sxs-lookup"><span data-stu-id="e096d-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-582">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="e096d-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-583">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e096d-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-584">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-585">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetDiskFreeSpace"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e096d-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-586">Dimensioni dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="e096d-586">Size of the disk drive.</span></span>

<span data-ttu-id="e096d-587">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e096d-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-588">**Status**</span><span class="sxs-lookup"><span data-stu-id="e096d-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-589">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-590">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-591">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e096d-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-592">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e096d-592">Current status of the object.</span></span> <span data-ttu-id="e096d-593">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="e096d-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e096d-594">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="e096d-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e096d-595">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="e096d-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e096d-596">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="e096d-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e096d-597">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="e096d-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e096d-598">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e096d-599">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e096d-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e096d-600">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e096d-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e096d-601">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="e096d-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e096d-602">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="e096d-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e096d-603">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e096d-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e096d-604">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="e096d-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e096d-605">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e096d-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e096d-606">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="e096d-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e096d-607">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="e096d-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e096d-608">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="e096d-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e096d-609">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="e096d-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e096d-610">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="e096d-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e096d-611">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="e096d-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e096d-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-613">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e096d-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-614">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-615">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e096d-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-616">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e096d-616">State of the logical device.</span></span> <span data-ttu-id="e096d-617">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e096d-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e096d-618">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e096d-619">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e096d-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e096d-620">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="e096d-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e096d-621">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e096d-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e096d-622">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="e096d-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e096d-623">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="e096d-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e096d-624">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e096d-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-625">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-626">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-627">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e096d-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e096d-628">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="e096d-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e096d-629">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-630">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e096d-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-631">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-632">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-633">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e096d-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e096d-634">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="e096d-634">Name of the scoping system.</span></span>

<span data-ttu-id="e096d-635">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e096d-636">**Trasferisci**</span><span class="sxs-lookup"><span data-stu-id="e096d-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-637">Tipo di dati: **real64**</span><span class="sxs-lookup"><span data-stu-id="e096d-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-638">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-639">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("riferimento a \| file Win32API e riferimento all'ora"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte al secondo")</span><span class="sxs-lookup"><span data-stu-id="e096d-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-640">Velocità di trasferimento dell'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e096d-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="e096d-641">Il valore-1 indica che non è possibile determinare la frequenza.</span><span class="sxs-lookup"><span data-stu-id="e096d-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="e096d-642">Quando si verifica questo problema, il CD non si trova nell'unità.</span><span class="sxs-lookup"><span data-stu-id="e096d-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-643">**NomeVolume**</span><span class="sxs-lookup"><span data-stu-id="e096d-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-644">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-645">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-646">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="e096d-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-647">Nome del volume dell'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="e096d-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="e096d-648">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e096d-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e096d-649">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e096d-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e096d-650">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e096d-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e096d-651">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="e096d-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="e096d-652">Numero di serie del volume del supporto nell'unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e096d-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="e096d-653">Esempio: A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="e096d-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e096d-654">Commenti</span><span class="sxs-lookup"><span data-stu-id="e096d-654">Remarks</span></span>

<span data-ttu-id="e096d-655">La classe **Win32 \_ CDROMDrive** è derivata da [**CIM \_ CDROMDrive**](cim-cdromdrive.md) che deriva da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="e096d-656">La classe **CIM \_ MediaAccessDevice** deriva da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e096d-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e096d-657">Esempio</span><span class="sxs-lookup"><span data-stu-id="e096d-657">Examples</span></span>

<span data-ttu-id="e096d-658">Nell'esempio VBScript seguente viene determinato se un CD si trova in un'unità CDROM.</span><span class="sxs-lookup"><span data-stu-id="e096d-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="e096d-659">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e096d-659">Requirements</span></span>



| <span data-ttu-id="e096d-660">Requisito</span><span class="sxs-lookup"><span data-stu-id="e096d-660">Requirement</span></span> | <span data-ttu-id="e096d-661">Valore</span><span class="sxs-lookup"><span data-stu-id="e096d-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e096d-662">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e096d-662">Minimum supported client</span></span><br/> | <span data-ttu-id="e096d-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e096d-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e096d-664">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e096d-664">Minimum supported server</span></span><br/> | <span data-ttu-id="e096d-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e096d-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e096d-666">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e096d-666">Namespace</span></span><br/>                | <span data-ttu-id="e096d-667">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e096d-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e096d-668">MOF</span><span class="sxs-lookup"><span data-stu-id="e096d-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e096d-669"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e096d-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e096d-670">DLL</span><span class="sxs-lookup"><span data-stu-id="e096d-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e096d-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e096d-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e096d-672">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e096d-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e096d-673">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="e096d-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="e096d-674">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e096d-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e096d-675">Attività WMI: hardware del computer</span><span class="sxs-lookup"><span data-stu-id="e096d-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="e096d-676">Attività WMI: dischi e file System</span><span class="sxs-lookup"><span data-stu-id="e096d-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 


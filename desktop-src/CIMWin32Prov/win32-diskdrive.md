---
description: Rappresenta un'unità disco fisica come visualizzato da un computer che esegue il sistema operativo Windows.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Classe Win32_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523985"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="83928-103">Win32 \_ DiskDrive (classe)</span><span class="sxs-lookup"><span data-stu-id="83928-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="83928-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDrive Win32** rappresenta un'unità disco fisica come visualizzato da un computer che esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="83928-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="83928-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="83928-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="83928-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="83928-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83928-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83928-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="83928-108">Members</span><span class="sxs-lookup"><span data-stu-id="83928-108">Members</span></span>

<span data-ttu-id="83928-109">La classe **Win32 \_ DiskDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="83928-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="83928-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="83928-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="83928-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83928-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="83928-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="83928-112">Methods</span></span>

<span data-ttu-id="83928-113">La classe **Win32 \_ DiskDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="83928-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="83928-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="83928-114">Method</span></span>            | <span data-ttu-id="83928-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83928-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83928-116">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="83928-116">**Reset**</span></span>         | <span data-ttu-id="83928-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="83928-117">Not implemented.</span></span> <span data-ttu-id="83928-118">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ DiskDrive**](cim-diskdrive.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="83928-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="83928-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="83928-119">**SetPowerState**</span></span> | <span data-ttu-id="83928-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="83928-120">Not implemented.</span></span> <span data-ttu-id="83928-121">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ DiskDrive**](cim-diskdrive.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="83928-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="83928-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83928-122">Properties</span></span>

<span data-ttu-id="83928-123">La classe **Win32 \_ DiskDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="83928-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83928-124">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="83928-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83928-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-127">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="83928-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="83928-128">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-128">Availability and status of the device.</span></span>

<span data-ttu-id="83928-129">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83928-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="83928-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83928-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="83928-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="83928-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="83928-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83928-133">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="83928-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="83928-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="83928-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="83928-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="83928-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="83928-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="83928-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="83928-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="83928-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="83928-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="83928-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="83928-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="83928-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83928-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="83928-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="83928-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="83928-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="83928-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="83928-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="83928-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="83928-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="83928-144">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="83928-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="83928-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="83928-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="83928-146">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="83928-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="83928-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="83928-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="83928-148">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="83928-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="83928-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="83928-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="83928-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="83928-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="83928-151">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="83928-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="83928-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="83928-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="83928-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="83928-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="83928-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="83928-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="83928-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="83928-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="83928-156">L'unità disco non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="83928-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-157">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="83928-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-158">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-160">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="83928-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83928-161">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="83928-162">Esempio: 512</span><span class="sxs-lookup"><span data-stu-id="83928-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="83928-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="83928-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-164">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="83928-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-166">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="83928-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="83928-167">Matrice di funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="83928-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="83928-168">Ad esempio, il dispositivo può supportare l'accesso casuale (3), i supporti rimovibili (7) e la pulizia automatica (9).</span><span class="sxs-lookup"><span data-stu-id="83928-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="83928-169">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83928-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="83928-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83928-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="83928-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="83928-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="83928-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="83928-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="83928-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="83928-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="83928-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="83928-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="83928-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="83928-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="83928-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="83928-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="83928-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="83928-178">Supporta supporti rimovibili</span><span class="sxs-lookup"><span data-stu-id="83928-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="83928-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="83928-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="83928-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="83928-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="83928-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="83928-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="83928-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="83928-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="83928-183">Supporta Dual-Sided supporti</span><span class="sxs-lookup"><span data-stu-id="83928-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="83928-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="83928-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="83928-185">Espulsione prima dello smontaggio dell'unità non necessaria</span><span class="sxs-lookup"><span data-stu-id="83928-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-186">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="83928-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-187">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="83928-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="83928-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-189">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="83928-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="83928-190">Elenco di spiegazioni più dettagliate per tutte le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="83928-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="83928-191">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="83928-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="83928-192">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-193">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="83928-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-196">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="83928-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="83928-197">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="83928-197">Short description of the object.</span></span>

<span data-ttu-id="83928-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83928-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="83928-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-202">Algoritmo o strumento usato dal dispositivo per supportare la compressione.</span><span class="sxs-lookup"><span data-stu-id="83928-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="83928-203">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="83928-204">Nome dell'algoritmo di compressione o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="83928-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="83928-205">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="83928-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="83928-206">Se il dispositivo supporta o meno le funzionalità di compressione non è noto.</span><span class="sxs-lookup"><span data-stu-id="83928-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="83928-207">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="83928-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="83928-208">Il dispositivo supporta le funzionalità di compressione, ma lo schema di compressione non è noto o non è stato divulgato.</span><span class="sxs-lookup"><span data-stu-id="83928-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="83928-209">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="83928-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="83928-210">Il dispositivo non supporta la compressione.</span><span class="sxs-lookup"><span data-stu-id="83928-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83928-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-212">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-214">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="83928-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83928-215">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="83928-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="83928-216">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="83928-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="83928-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="83928-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="83928-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="83928-219">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="83928-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="83928-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="83928-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="83928-221">(1)</span><span class="sxs-lookup"><span data-stu-id="83928-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="83928-222">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="83928-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83928-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="83928-224">(2)</span><span class="sxs-lookup"><span data-stu-id="83928-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="83928-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="83928-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="83928-226">(3)</span><span class="sxs-lookup"><span data-stu-id="83928-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="83928-227">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="83928-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="83928-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="83928-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="83928-229">(4)</span><span class="sxs-lookup"><span data-stu-id="83928-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="83928-230">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="83928-230">Device is not working properly.</span></span> <span data-ttu-id="83928-231">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="83928-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="83928-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="83928-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="83928-233">(5)</span><span class="sxs-lookup"><span data-stu-id="83928-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="83928-234">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="83928-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="83928-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="83928-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="83928-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="83928-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="83928-237">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="83928-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="83928-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="83928-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="83928-239">(7)</span><span class="sxs-lookup"><span data-stu-id="83928-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="83928-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="83928-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="83928-241">(8)</span><span class="sxs-lookup"><span data-stu-id="83928-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="83928-242">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="83928-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="83928-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="83928-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="83928-244">(9)</span><span class="sxs-lookup"><span data-stu-id="83928-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="83928-245">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="83928-245">Device is not working properly.</span></span> <span data-ttu-id="83928-246">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="83928-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="83928-248">(10)</span><span class="sxs-lookup"><span data-stu-id="83928-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="83928-249">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="83928-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="83928-251">(11)</span><span class="sxs-lookup"><span data-stu-id="83928-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="83928-252">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="83928-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="83928-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="83928-254">12</span><span class="sxs-lookup"><span data-stu-id="83928-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="83928-255">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="83928-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="83928-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="83928-257">(13)</span><span class="sxs-lookup"><span data-stu-id="83928-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="83928-258">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="83928-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="83928-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="83928-260">(14)</span><span class="sxs-lookup"><span data-stu-id="83928-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="83928-261">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="83928-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="83928-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="83928-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="83928-263">(15)</span><span class="sxs-lookup"><span data-stu-id="83928-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="83928-264">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="83928-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="83928-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="83928-266">(16)</span><span class="sxs-lookup"><span data-stu-id="83928-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="83928-267">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="83928-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="83928-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="83928-269">(17)</span><span class="sxs-lookup"><span data-stu-id="83928-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="83928-270">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="83928-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83928-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="83928-272">(18)</span><span class="sxs-lookup"><span data-stu-id="83928-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="83928-273">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="83928-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="83928-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="83928-275">(19)</span><span class="sxs-lookup"><span data-stu-id="83928-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="83928-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="83928-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="83928-277">(20)</span><span class="sxs-lookup"><span data-stu-id="83928-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="83928-278">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="83928-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="83928-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="83928-280">(21)</span><span class="sxs-lookup"><span data-stu-id="83928-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="83928-281">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="83928-281">System failure.</span></span> <span data-ttu-id="83928-282">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="83928-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="83928-283">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="83928-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="83928-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="83928-285">(22)</span><span class="sxs-lookup"><span data-stu-id="83928-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="83928-286">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="83928-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="83928-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="83928-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="83928-288">(23)</span><span class="sxs-lookup"><span data-stu-id="83928-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="83928-289">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="83928-289">System failure.</span></span> <span data-ttu-id="83928-290">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="83928-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="83928-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="83928-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="83928-292">(24)</span><span class="sxs-lookup"><span data-stu-id="83928-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="83928-293">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="83928-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="83928-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="83928-295">(25)</span><span class="sxs-lookup"><span data-stu-id="83928-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="83928-296">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="83928-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="83928-298">(26)</span><span class="sxs-lookup"><span data-stu-id="83928-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="83928-299">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="83928-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="83928-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="83928-301">(27)</span><span class="sxs-lookup"><span data-stu-id="83928-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="83928-302">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="83928-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="83928-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="83928-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="83928-304">(28)</span><span class="sxs-lookup"><span data-stu-id="83928-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="83928-305">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="83928-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="83928-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="83928-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="83928-307">(29)</span><span class="sxs-lookup"><span data-stu-id="83928-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="83928-308">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="83928-308">Device is disabled.</span></span> <span data-ttu-id="83928-309">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="83928-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="83928-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="83928-311">(30)</span><span class="sxs-lookup"><span data-stu-id="83928-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="83928-312">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83928-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83928-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="83928-314">31</span><span class="sxs-lookup"><span data-stu-id="83928-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="83928-315">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="83928-315">Device is not working properly.</span></span> <span data-ttu-id="83928-316">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="83928-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="83928-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-318">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="83928-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83928-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-320">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="83928-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83928-321">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="83928-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="83928-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83928-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-326">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83928-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83928-327">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="83928-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="83928-328">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="83928-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="83928-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-330">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="83928-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-331">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-333">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="83928-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83928-334">Dimensioni del blocco predefinite, in byte, per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="83928-335">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="83928-336">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-337">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="83928-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-340">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="83928-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="83928-341">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="83928-341">Description of the object.</span></span>

<span data-ttu-id="83928-342">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83928-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="83928-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-346">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="83928-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="83928-347">Identificatore univoco dell'unità disco con altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="83928-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="83928-348">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="83928-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-350">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="83928-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83928-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-352">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="83928-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="83928-353">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="83928-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-357">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="83928-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="83928-358">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="83928-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-362">Tipo di rilevamento e correzione degli errori supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="83928-363">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-364">**FirmwareRevision**</span><span class="sxs-lookup"><span data-stu-id="83928-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-365">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-367">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="83928-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="83928-368">Revisione per il firmware dell'unità disco assegnato dal produttore.</span><span class="sxs-lookup"><span data-stu-id="83928-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="83928-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="83928-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-370">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-372">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows 95/98 Functions \| unità \_ \_ informazioni mappa \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="83928-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="83928-373">Numero di unità fisica dell'unità specificata.</span><span class="sxs-lookup"><span data-stu-id="83928-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="83928-374">Questa proprietà viene compilata dalla struttura del [**\_ \_ numero di dispositivi di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) restituita dal codice di controllo del [**\_ \_ \_ \_ numero del dispositivo di archiviazione IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .</span><span class="sxs-lookup"><span data-stu-id="83928-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="83928-375">Il valore 0xFFFFFFFF indica che l'unità specificata non è mappata a un'unità fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="83928-376">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="83928-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="83928-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="83928-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-378">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83928-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83928-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-380">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="83928-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="83928-381">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="83928-381">Date and time the object was installed.</span></span> <span data-ttu-id="83928-382">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="83928-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="83928-383">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83928-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="83928-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-385">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-387">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and Output functions \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="83928-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="83928-388">Tipo di interfaccia dell'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="83928-389">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="83928-389">The values are:</span></span>

<span data-ttu-id="83928-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="83928-390">SCSI</span></span>

<span data-ttu-id="83928-391">HDC</span><span class="sxs-lookup"><span data-stu-id="83928-391">HDC</span></span>

<span data-ttu-id="83928-392">IDE</span><span class="sxs-lookup"><span data-stu-id="83928-392">IDE</span></span>

<span data-ttu-id="83928-393">USB</span><span class="sxs-lookup"><span data-stu-id="83928-393">USB</span></span>

<span data-ttu-id="83928-394">1394</span><span class="sxs-lookup"><span data-stu-id="83928-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="83928-395">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83928-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-396">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-398">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="83928-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="83928-399">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-400">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="83928-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-403">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ computer locale \\ \\ hardware \\ \\ DEVICEMAP SCSI \\ \\ \\ \\ porta SCSI \\ \\ bus \\ \\ di destinazione ID \\ \\ unità logica \\ \\ identificatore", "Win32Registry \| produttore")</span><span class="sxs-lookup"><span data-stu-id="83928-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="83928-404">Nome del produttore dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="83928-405">Esempio: "Seagate"</span><span class="sxs-lookup"><span data-stu-id="83928-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="83928-406">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="83928-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-407">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-409">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="83928-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83928-410">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="83928-411">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="83928-412">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-413">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="83928-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-414">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-416">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="83928-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="83928-417">Dimensioni massime del supporto, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="83928-418">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="83928-419">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-420">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="83928-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-421">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="83928-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83928-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-423">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediaType \| FixedMedia")</span><span class="sxs-lookup"><span data-stu-id="83928-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="83928-424">Se **true**, il supporto per un'unità disco viene caricato, il che significa che il dispositivo ha un file System leggibile ed è accessibile.</span><span class="sxs-lookup"><span data-stu-id="83928-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="83928-425">Per le unità disco fisse, questa proprietà sarà sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="83928-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="83928-426">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="83928-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-427">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-429">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediaType")</span><span class="sxs-lookup"><span data-stu-id="83928-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="83928-430">Tipo di supporto usato o a cui si accede dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="83928-431">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="83928-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="83928-432">**Supporti disco rigido esterno**</span><span class="sxs-lookup"><span data-stu-id="83928-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="83928-433">**Supporti rimovibili** ("supporti rimovibili diversi da floppy")</span><span class="sxs-lookup"><span data-stu-id="83928-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="83928-434">**Disco rigido fisso** ("supporti disco rigido fissi")</span><span class="sxs-lookup"><span data-stu-id="83928-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83928-435">**Unknown** ("format is unknown")</span><span class="sxs-lookup"><span data-stu-id="83928-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-436">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="83928-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-437">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-438">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-439">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="83928-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83928-440">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="83928-441">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="83928-442">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-443">**Modello**</span><span class="sxs-lookup"><span data-stu-id="83928-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-444">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-446">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ computer locale \\ \\ hardware \\ \\ DEVICEMAP SCSI \\ \\ \\ \\ porta SCSI \\ \\ bus \\ \\ di destinazione ID \\ \\ unità logica \\ \\ identificatore", "Win32Registry \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="83928-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="83928-447">Il numero di modello dell'unità disco del produttore.</span><span class="sxs-lookup"><span data-stu-id="83928-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="83928-448">Esempio: "ST32171W"</span><span class="sxs-lookup"><span data-stu-id="83928-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="83928-449">**Nome**</span><span class="sxs-lookup"><span data-stu-id="83928-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-450">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-452">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="83928-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="83928-453">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="83928-453">Label by which the object is known.</span></span> <span data-ttu-id="83928-454">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="83928-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="83928-455">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83928-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-456">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="83928-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-457">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="83928-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83928-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-459">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="83928-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="83928-460">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="83928-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="83928-461">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-462">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="83928-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-463">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-465">Numero massimo di supporti che possono essere supportati o inseriti (quando il dispositivo di accesso multimediale supporta più supporti singoli).</span><span class="sxs-lookup"><span data-stu-id="83928-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="83928-466">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-467">**Partizioni**</span><span class="sxs-lookup"><span data-stu-id="83928-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-468">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-470">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structure \| [**\_ Information**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition")</span><span class="sxs-lookup"><span data-stu-id="83928-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="83928-471">Numero di partizioni in questa unità disco fisica riconosciute dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83928-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="83928-472">Esempio: 2</span><span class="sxs-lookup"><span data-stu-id="83928-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="83928-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="83928-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-476">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="83928-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83928-477">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="83928-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="83928-478">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="83928-479">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="83928-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="83928-480">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83928-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-481">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="83928-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-483">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="83928-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="83928-484">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="83928-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83928-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="83928-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="83928-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="83928-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="83928-487">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="83928-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="83928-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="83928-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="83928-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83928-490">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="83928-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="83928-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="83928-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="83928-492">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="83928-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="83928-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="83928-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="83928-494">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="83928-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="83928-495">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="83928-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="83928-496">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="83928-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="83928-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="83928-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="83928-498">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="83928-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="83928-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="83928-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="83928-500">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="83928-500">Timed Power-On Supported</span></span>

<span data-ttu-id="83928-501">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="83928-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="83928-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-503">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="83928-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83928-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83928-505">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="83928-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="83928-506">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="83928-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="83928-507">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="83928-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-509">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-510">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-511">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PathId")</span><span class="sxs-lookup"><span data-stu-id="83928-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="83928-512">Numero del bus SCSI dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="83928-513">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="83928-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="83928-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="83928-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-515">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83928-516">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-517">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API del \| dispositivo di input e di output del dispositivo \| [**SCSI \_**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| lun")</span><span class="sxs-lookup"><span data-stu-id="83928-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="83928-518">Numero di unità logica (LUN) SCSI dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="83928-519">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="83928-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="83928-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="83928-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-521">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83928-522">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-523">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| NumeroPorta")</span><span class="sxs-lookup"><span data-stu-id="83928-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="83928-524">Numero di porta SCSI dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="83928-525">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="83928-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="83928-526">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="83928-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-527">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83928-528">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-529">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| targetID")</span><span class="sxs-lookup"><span data-stu-id="83928-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="83928-530">Numero identificatore SCSI dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="83928-531">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="83928-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="83928-532">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="83928-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-533">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-534">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-535">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")</span><span class="sxs-lookup"><span data-stu-id="83928-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="83928-536">Numero di settori in ogni traccia per questa unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="83928-537">Esempio: 63</span><span class="sxs-lookup"><span data-stu-id="83928-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="83928-538">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="83928-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-539">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-540">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-541">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="83928-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="83928-542">Numero allocato dal produttore per identificare i supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="83928-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="83928-543">Esempio: WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="83928-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="83928-544">**Firma**</span><span class="sxs-lookup"><span data-stu-id="83928-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-545">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-546">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-547">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| firma [**\_ \_ informazioni layout unità**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| ")</span><span class="sxs-lookup"><span data-stu-id="83928-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="83928-548">Identificazione del disco.</span><span class="sxs-lookup"><span data-stu-id="83928-548">Disk identification.</span></span> <span data-ttu-id="83928-549">Questa proprietà può essere utilizzata per identificare una risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="83928-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="83928-550">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="83928-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-551">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-552">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-553">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="83928-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83928-554">Dimensioni dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-554">Size of the disk drive.</span></span> <span data-ttu-id="83928-555">Viene calcolato moltiplicando il numero totale di cilindri, le tracce in ogni cilindro, i settori in ogni traccia e i byte in ogni settore.</span><span class="sxs-lookup"><span data-stu-id="83928-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="83928-556">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-557">**Status**</span><span class="sxs-lookup"><span data-stu-id="83928-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-558">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-559">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-560">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="83928-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="83928-561">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="83928-561">Current status of the object.</span></span> <span data-ttu-id="83928-562">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="83928-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="83928-563">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="83928-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="83928-564">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="83928-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="83928-565">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="83928-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="83928-566">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="83928-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="83928-567">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83928-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="83928-568">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="83928-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="83928-569">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="83928-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="83928-570">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="83928-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83928-571">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="83928-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83928-572">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="83928-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="83928-573">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="83928-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="83928-574">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="83928-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="83928-575">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="83928-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="83928-576">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="83928-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="83928-577">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="83928-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="83928-578">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="83928-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="83928-579">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="83928-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="83928-580">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="83928-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="83928-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-582">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83928-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83928-583">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-584">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="83928-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="83928-585">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="83928-585">State of the logical device.</span></span> <span data-ttu-id="83928-586">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="83928-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="83928-587">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83928-588">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="83928-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83928-589">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="83928-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="83928-590">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="83928-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="83928-591">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="83928-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="83928-592">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="83928-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83928-593">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83928-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-594">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-595">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-596">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83928-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83928-597">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="83928-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="83928-598">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-599">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="83928-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-600">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83928-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83928-601">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-602">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83928-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83928-603">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="83928-603">Name of the scoping system.</span></span>

<span data-ttu-id="83928-604">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83928-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="83928-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-606">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-607">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-608">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| cilindri [**\_ Geometry disks**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="83928-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="83928-609">Numero totale di cilindri sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="83928-610">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="83928-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="83928-611">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco ad alta capacità.</span><span class="sxs-lookup"><span data-stu-id="83928-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="83928-612">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="83928-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="83928-613">Esempio: 657</span><span class="sxs-lookup"><span data-stu-id="83928-613">Example: 657</span></span>

<span data-ttu-id="83928-614">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="83928-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-616">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-617">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-618">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="83928-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="83928-619">Numero totale di teste sull'unità disco.</span><span class="sxs-lookup"><span data-stu-id="83928-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="83928-620">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="83928-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="83928-621">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco ad alta capacità.</span><span class="sxs-lookup"><span data-stu-id="83928-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="83928-622">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="83928-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="83928-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="83928-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-624">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-625">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-626">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")</span><span class="sxs-lookup"><span data-stu-id="83928-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="83928-627">Numero totale di settori sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="83928-628">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="83928-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="83928-629">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco ad alta capacità.</span><span class="sxs-lookup"><span data-stu-id="83928-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="83928-630">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="83928-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="83928-631">Esempio: 2649024</span><span class="sxs-lookup"><span data-stu-id="83928-631">Example: 2649024</span></span>

<span data-ttu-id="83928-632">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="83928-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-634">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83928-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83928-635">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-636">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="83928-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="83928-637">Numero totale di tracce sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="83928-638">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="83928-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="83928-639">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco ad alta capacità.</span><span class="sxs-lookup"><span data-stu-id="83928-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="83928-640">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="83928-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="83928-641">Esempio: 42048</span><span class="sxs-lookup"><span data-stu-id="83928-641">Example: 42048</span></span>

<span data-ttu-id="83928-642">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83928-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83928-643">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="83928-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83928-644">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83928-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83928-645">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83928-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83928-646">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structures \| [**disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="83928-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="83928-647">Numero di tracce in ogni cilindro sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="83928-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="83928-648">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="83928-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="83928-649">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco ad alta capacità.</span><span class="sxs-lookup"><span data-stu-id="83928-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="83928-650">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="83928-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="83928-651">Esempio: 64</span><span class="sxs-lookup"><span data-stu-id="83928-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83928-652">Commenti</span><span class="sxs-lookup"><span data-stu-id="83928-652">Remarks</span></span>

<span data-ttu-id="83928-653">Le unità disco rigido fisiche sono il supporto di archiviazione primario per informazioni in qualsiasi ambiente di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="83928-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="83928-654">Sebbene le organizzazioni usino spesso dispositivi come le unità nastro e le unità Compact Disc per l'archiviazione dei dati, questi dispositivi non sono adatti per l'archiviazione quotidiana dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="83928-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="83928-655">Solo i dischi rigidi fisici offrono la velocità e la facilità d'uso necessari per l'archiviazione dei dati e per l'esecuzione di applicazioni e del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83928-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="83928-656">Per gestire i dati in modo efficiente, è importante disporre di un inventario dettagliato di tutti i dischi fisici, delle relative funzionalità e delle relative capacità.</span><span class="sxs-lookup"><span data-stu-id="83928-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="83928-657">È possibile utilizzare la classe **Win32 \_ DiskDrive** per derivare questo tipo di inventario.</span><span class="sxs-lookup"><span data-stu-id="83928-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="83928-658">Qualsiasi interfaccia a un'unità disco fisico di Windows è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="83928-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="83928-659">Le funzionalità dell'unità disco visualizzate tramite questo oggetto corrispondono alle caratteristiche logiche e di gestione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="83928-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="83928-660">In alcuni casi, questo potrebbe non riflettere le caratteristiche fisiche effettive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83928-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="83928-661">Qualsiasi oggetto basato su un altro dispositivo logico non è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="83928-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="83928-662">Per motivi di sicurezza, è necessario che un utente che si connette da un computer remoto disponga del privilegio di **\_ \_ connessione SC Manager** abilitato per poter enumerare questa classe.</span><span class="sxs-lookup"><span data-stu-id="83928-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="83928-663">Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](/windows/desktop/Services/service-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="83928-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="83928-664">La classe **Win32 \_ DiskDrive** è derivata da [**CIM \_ DiskDrive**](cim-diskdrive.md) che deriva da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="83928-665">La classe **CIM \_ MediaAccessDevice** deriva da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83928-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="83928-666">Esempio</span><span class="sxs-lookup"><span data-stu-id="83928-666">Examples</span></span>

<span data-ttu-id="83928-667">Il [report inventario server-](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) esempio di codice PowerShell di WMI & CIM sulla raccolta TechNet usa diverse classi, tra cui **Win32 \_ DiskDrive**, per restituire informazioni sullo stato del server.</span><span class="sxs-lookup"><span data-stu-id="83928-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="83928-668">L' [unità della mappa per la lettera di unità usando la \_ proprietà del tipo di interfaccia Win32 DiskDrive](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) esempio di codice di PowerShell esegue il mapping di un'unità a una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="83928-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="83928-669">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83928-669">Requirements</span></span>



| <span data-ttu-id="83928-670">Requisito</span><span class="sxs-lookup"><span data-stu-id="83928-670">Requirement</span></span> | <span data-ttu-id="83928-671">Valore</span><span class="sxs-lookup"><span data-stu-id="83928-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83928-672">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83928-672">Minimum supported client</span></span><br/> | <span data-ttu-id="83928-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83928-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83928-674">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83928-674">Minimum supported server</span></span><br/> | <span data-ttu-id="83928-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83928-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83928-676">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83928-676">Namespace</span></span><br/>                | <span data-ttu-id="83928-677">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="83928-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83928-678">MOF</span><span class="sxs-lookup"><span data-stu-id="83928-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83928-679"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83928-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83928-680">DLL</span><span class="sxs-lookup"><span data-stu-id="83928-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83928-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83928-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83928-682">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83928-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83928-683">**\_DiskDrive CIM**</span><span class="sxs-lookup"><span data-stu-id="83928-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="83928-684">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="83928-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="83928-685">Attività WMI: dischi e file System</span><span class="sxs-lookup"><span data-stu-id="83928-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 


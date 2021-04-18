---
description: La \_ classe CIM DisketteDrive rappresenta le funzionalità e la gestione di un'unità floppy.
ms.assetid: 6c1bf597-ca67-4c37-8f90-d13afee0fab3
ms.tgt_platform: multiple
title: Classe CIM_DisketteDrive (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisketteDrive
- CIM_DisketteDrive.Availability
- CIM_DisketteDrive.Capabilities
- CIM_DisketteDrive.CapabilityDescriptions
- CIM_DisketteDrive.Caption
- CIM_DisketteDrive.CompressionMethod
- CIM_DisketteDrive.ConfigManagerErrorCode
- CIM_DisketteDrive.ConfigManagerUserConfig
- CIM_DisketteDrive.CreationClassName
- CIM_DisketteDrive.DefaultBlockSize
- CIM_DisketteDrive.Description
- CIM_DisketteDrive.DeviceID
- CIM_DisketteDrive.ErrorCleared
- CIM_DisketteDrive.ErrorDescription
- CIM_DisketteDrive.ErrorMethodology
- CIM_DisketteDrive.InstallDate
- CIM_DisketteDrive.LastErrorCode
- CIM_DisketteDrive.MaxBlockSize
- CIM_DisketteDrive.MaxMediaSize
- CIM_DisketteDrive.MinBlockSize
- CIM_DisketteDrive.Name
- CIM_DisketteDrive.NeedsCleaning
- CIM_DisketteDrive.NumberOfMediaSupported
- CIM_DisketteDrive.PNPDeviceID
- CIM_DisketteDrive.PowerManagementCapabilities
- CIM_DisketteDrive.PowerManagementSupported
- CIM_DisketteDrive.Status
- CIM_DisketteDrive.StatusInfo
- CIM_DisketteDrive.SystemCreationClassName
- CIM_DisketteDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62570333225112bf734bf1a70a35f450be9df0ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305030"
---
# <a name="cim_diskettedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="af0b2-103">Classe CIM_DisketteDrive (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="af0b2-103">CIM_DisketteDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="af0b2-104">La classe **CIM \_ DisketteDrive** rappresenta le funzionalità e la gestione di un'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="af0b2-104">The **CIM\_DisketteDrive** class represents the capabilities and management of a diskette drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af0b2-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="af0b2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="af0b2-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="af0b2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="af0b2-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="af0b2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="af0b2-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="af0b2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af0b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af0b2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{F27851CD-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_DisketteDrive : CIM_MediaAccessDevice
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="af0b2-110">Members</span><span class="sxs-lookup"><span data-stu-id="af0b2-110">Members</span></span>

<span data-ttu-id="af0b2-111">La classe **CIM \_ DisketteDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af0b2-111">The **CIM\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="af0b2-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="af0b2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="af0b2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af0b2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="af0b2-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="af0b2-114">Methods</span></span>

<span data-ttu-id="af0b2-115">La classe **CIM \_ DisketteDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="af0b2-115">The **CIM\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="af0b2-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="af0b2-116">Method</span></span>                                                                | <span data-ttu-id="af0b2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af0b2-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af0b2-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="af0b2-118">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="af0b2-119">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="af0b2-120">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="af0b2-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="af0b2-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="af0b2-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="af0b2-122">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="af0b2-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="af0b2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="af0b2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af0b2-124">Properties</span></span>

<span data-ttu-id="af0b2-125">La classe **CIM \_ DisketteDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af0b2-125">The **CIM\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af0b2-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="af0b2-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af0b2-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="af0b2-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-130">Availability and status of the device.</span></span>

<span data-ttu-id="af0b2-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af0b2-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af0b2-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af0b2-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af0b2-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="af0b2-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="af0b2-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="af0b2-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="af0b2-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="af0b2-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="af0b2-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af0b2-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="af0b2-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="af0b2-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="af0b2-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="af0b2-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="af0b2-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="af0b2-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="af0b2-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="af0b2-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="af0b2-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="af0b2-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="af0b2-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="af0b2-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="af0b2-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="af0b2-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="af0b2-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-145">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="af0b2-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="af0b2-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-147">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="af0b2-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="af0b2-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="af0b2-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-149">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="af0b2-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="af0b2-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="af0b2-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="af0b2-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="af0b2-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-152">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="af0b2-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="af0b2-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="af0b2-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-154">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="af0b2-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="af0b2-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="af0b2-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-156">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="af0b2-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="af0b2-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-158">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="af0b2-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="af0b2-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-160">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="af0b2-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="af0b2-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-162">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af0b2-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-164">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="af0b2-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-165">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="af0b2-165">Capabilities of the media access device.</span></span> <span data-ttu-id="af0b2-166">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-166">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af0b2-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af0b2-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-168">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-168">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af0b2-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af0b2-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-170">Altro.</span><span class="sxs-lookup"><span data-stu-id="af0b2-170">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="af0b2-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="af0b2-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-172">Accesso sequenziale.</span><span class="sxs-lookup"><span data-stu-id="af0b2-172">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="af0b2-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="af0b2-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-174">Accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="af0b2-174">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="af0b2-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="af0b2-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-176">Scrittura.</span><span class="sxs-lookup"><span data-stu-id="af0b2-176">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="af0b2-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="af0b2-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-178">Crittografia.</span><span class="sxs-lookup"><span data-stu-id="af0b2-178">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="af0b2-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="af0b2-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-180">Compressione.</span><span class="sxs-lookup"><span data-stu-id="af0b2-180">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="af0b2-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="af0b2-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-182">Supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="af0b2-182">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="af0b2-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="af0b2-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-184">Pulizia manuale.</span><span class="sxs-lookup"><span data-stu-id="af0b2-184">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="af0b2-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="af0b2-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-186">Pulizia automatica.</span><span class="sxs-lookup"><span data-stu-id="af0b2-186">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="af0b2-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="af0b2-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-188">Notifica intelligente.</span><span class="sxs-lookup"><span data-stu-id="af0b2-188">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="af0b2-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="af0b2-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-190">Distingue un dispositivo che può accedere a entrambi i lati del supporto a doppio lato da un dispositivo che legge solo un singolo lato e richiede che il file multimediale venga riattivato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="af0b2-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="af0b2-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-192">Indica che non è necessario che il supporto venga espulso in modo esplicito dal dispositivo prima dell'accesso da parte di un elemento di selezione.</span><span class="sxs-lookup"><span data-stu-id="af0b2-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-193">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="af0b2-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-194">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="af0b2-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-196">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="af0b2-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-197">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="af0b2-197">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="af0b2-198">Ogni voce di questa matrice è correlata alla voce nella matrice di **funzionalità** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="af0b2-198">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="af0b2-199">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-199">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-200">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="af0b2-200">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-203">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="af0b2-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-204">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-204">Short textual description of the object.</span></span>

<span data-ttu-id="af0b2-205">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-206">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="af0b2-206">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-209">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-209">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="af0b2-210">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="af0b2-210">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="af0b2-211">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="af0b2-211">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="af0b2-212">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="af0b2-212">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="af0b2-213">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-213">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="af0b2-214">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="af0b2-214">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-215">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-215">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="af0b2-216">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="af0b2-216">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-217">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="af0b2-217">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="af0b2-218">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="af0b2-218">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-219">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="af0b2-219">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="af0b2-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-221">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af0b2-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-223">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af0b2-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-224">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="af0b2-224">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="af0b2-225">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="af0b2-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="af0b2-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="af0b2-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-228">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="af0b2-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="af0b2-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="af0b2-230">(1)</span><span class="sxs-lookup"><span data-stu-id="af0b2-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-231">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="af0b2-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af0b2-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="af0b2-233">(2)</span><span class="sxs-lookup"><span data-stu-id="af0b2-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="af0b2-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="af0b2-235">(3)</span><span class="sxs-lookup"><span data-stu-id="af0b2-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-236">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="af0b2-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="af0b2-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="af0b2-238">(4)</span><span class="sxs-lookup"><span data-stu-id="af0b2-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-239">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="af0b2-239">Device is not working properly.</span></span> <span data-ttu-id="af0b2-240">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="af0b2-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="af0b2-242">(5)</span><span class="sxs-lookup"><span data-stu-id="af0b2-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-243">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="af0b2-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="af0b2-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="af0b2-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="af0b2-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-246">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="af0b2-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="af0b2-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="af0b2-248">(7)</span><span class="sxs-lookup"><span data-stu-id="af0b2-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="af0b2-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="af0b2-250">(8)</span><span class="sxs-lookup"><span data-stu-id="af0b2-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-251">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="af0b2-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="af0b2-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="af0b2-253">(9)</span><span class="sxs-lookup"><span data-stu-id="af0b2-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-254">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-254">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="af0b2-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="af0b2-256">(10)</span><span class="sxs-lookup"><span data-stu-id="af0b2-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-257">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="af0b2-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="af0b2-259">(11)</span><span class="sxs-lookup"><span data-stu-id="af0b2-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-260">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="af0b2-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="af0b2-262">12</span><span class="sxs-lookup"><span data-stu-id="af0b2-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-263">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="af0b2-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="af0b2-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="af0b2-265">(13)</span><span class="sxs-lookup"><span data-stu-id="af0b2-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-266">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="af0b2-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="af0b2-268">(14)</span><span class="sxs-lookup"><span data-stu-id="af0b2-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-269">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="af0b2-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="af0b2-271">(15)</span><span class="sxs-lookup"><span data-stu-id="af0b2-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-272">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="af0b2-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="af0b2-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="af0b2-274">(16)</span><span class="sxs-lookup"><span data-stu-id="af0b2-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-275">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="af0b2-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="af0b2-277">(17)</span><span class="sxs-lookup"><span data-stu-id="af0b2-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-278">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af0b2-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="af0b2-280">(18)</span><span class="sxs-lookup"><span data-stu-id="af0b2-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-281">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="af0b2-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="af0b2-283">(19)</span><span class="sxs-lookup"><span data-stu-id="af0b2-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="af0b2-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="af0b2-285">(20)</span><span class="sxs-lookup"><span data-stu-id="af0b2-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-286">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="af0b2-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="af0b2-288">(21)</span><span class="sxs-lookup"><span data-stu-id="af0b2-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-289">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="af0b2-289">System failure.</span></span> <span data-ttu-id="af0b2-290">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="af0b2-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="af0b2-291">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="af0b2-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="af0b2-293">(22)</span><span class="sxs-lookup"><span data-stu-id="af0b2-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-294">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="af0b2-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="af0b2-296">(23)</span><span class="sxs-lookup"><span data-stu-id="af0b2-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-297">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="af0b2-297">System failure.</span></span> <span data-ttu-id="af0b2-298">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="af0b2-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="af0b2-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="af0b2-300">(24)</span><span class="sxs-lookup"><span data-stu-id="af0b2-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-301">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="af0b2-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="af0b2-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="af0b2-303">(25)</span><span class="sxs-lookup"><span data-stu-id="af0b2-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-304">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="af0b2-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="af0b2-306">(26)</span><span class="sxs-lookup"><span data-stu-id="af0b2-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-307">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="af0b2-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="af0b2-309">(27)</span><span class="sxs-lookup"><span data-stu-id="af0b2-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-310">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="af0b2-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="af0b2-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="af0b2-312">(28)</span><span class="sxs-lookup"><span data-stu-id="af0b2-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-313">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="af0b2-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="af0b2-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="af0b2-315">(29)</span><span class="sxs-lookup"><span data-stu-id="af0b2-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-316">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="af0b2-316">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="af0b2-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="af0b2-318">(30)</span><span class="sxs-lookup"><span data-stu-id="af0b2-318">(30)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-319">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-319">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af0b2-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="af0b2-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="af0b2-321">31</span><span class="sxs-lookup"><span data-stu-id="af0b2-321">(31)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-322">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="af0b2-322">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-323">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="af0b2-323">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-324">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af0b2-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-326">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af0b2-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-327">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="af0b2-327">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="af0b2-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-329">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="af0b2-329">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-332">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af0b2-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-333">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="af0b2-333">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="af0b2-334">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="af0b2-334">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="af0b2-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-336">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="af0b2-336">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-337">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af0b2-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-339">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="af0b2-339">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-340">D</span><span class="sxs-lookup"><span data-stu-id="af0b2-340">D</span></span>

<span data-ttu-id="af0b2-341">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-341">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="af0b2-342">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-342">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="af0b2-343">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af0b2-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-344">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="af0b2-344">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-347">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="af0b2-347">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-348">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-348">Textual description of the object.</span></span>

<span data-ttu-id="af0b2-349">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-350">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="af0b2-350">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-351">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-353">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af0b2-353">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-354">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-354">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="af0b2-355">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="af0b2-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-357">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af0b2-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-359">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="af0b2-360">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="af0b2-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-362">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-364">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="af0b2-364">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="af0b2-365">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-366">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="af0b2-366">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-369">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-369">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="af0b2-370">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-370">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-371">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="af0b2-371">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-372">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="af0b2-372">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-374">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="af0b2-374">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-375">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-375">Date and time when the object was installed.</span></span> <span data-ttu-id="af0b2-376">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-376">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="af0b2-377">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-378">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="af0b2-378">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-379">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af0b2-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-381">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-381">Last error code reported by the logical device.</span></span>

<span data-ttu-id="af0b2-382">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-383">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="af0b2-383">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-384">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af0b2-384">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-386">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="af0b2-386">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-387">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-387">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="af0b2-388">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-388">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="af0b2-389">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af0b2-389">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-390">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="af0b2-390">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-391">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af0b2-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-393">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="af0b2-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-394">Dimensioni massime, in kilobyte, dei supporti supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-394">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="af0b2-395">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="af0b2-395">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="af0b2-396">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="af0b2-397">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af0b2-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-398">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="af0b2-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-399">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af0b2-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-401">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="af0b2-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-402">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-402">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="af0b2-403">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="af0b2-404">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af0b2-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-405">**Nome**</span><span class="sxs-lookup"><span data-stu-id="af0b2-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-408">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="af0b2-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-409">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-409">Label by which the object is known.</span></span> <span data-ttu-id="af0b2-410">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="af0b2-410">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="af0b2-411">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-412">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="af0b2-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-413">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af0b2-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-415">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="af0b2-415">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="af0b2-416">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà Array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="af0b2-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="af0b2-417">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-418">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="af0b2-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-419">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af0b2-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-421">Quando il dispositivo di accesso multimediale supporta più supporti singoli, questa proprietà definisce il numero massimo che può essere supportato o inserito.</span><span class="sxs-lookup"><span data-stu-id="af0b2-421">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="af0b2-422">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="af0b2-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-426">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af0b2-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-427">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-427">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="af0b2-428">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="af0b2-429">Esempio: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="af0b2-429">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="af0b2-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-431">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af0b2-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-433">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="af0b2-434">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="af0b2-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af0b2-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="af0b2-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="af0b2-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="af0b2-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-437">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af0b2-437">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="af0b2-438"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="af0b2-438"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="af0b2-439"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="af0b2-439"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-440">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="af0b2-440">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="af0b2-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="af0b2-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-442">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="af0b2-442">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="af0b2-443"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="af0b2-443"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-444">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-444">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="af0b2-445">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="af0b2-445">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="af0b2-446">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="af0b2-446">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="af0b2-447"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="af0b2-447"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-448">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="af0b2-448">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="af0b2-449"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="af0b2-449"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="af0b2-450">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="af0b2-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-451">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="af0b2-451">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-452">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="af0b2-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-454">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="af0b2-454">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="af0b2-455">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="af0b2-455">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="af0b2-456">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="af0b2-456">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="af0b2-457">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="af0b2-457">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="af0b2-458">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-459">**Status**</span><span class="sxs-lookup"><span data-stu-id="af0b2-459">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-460">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-462">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="af0b2-462">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-463">Indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af0b2-463">Indicates the current status of the object.</span></span>

<span data-ttu-id="af0b2-464">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-464">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="af0b2-465">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="af0b2-465">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="af0b2-466">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="af0b2-466">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="af0b2-467">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="af0b2-467">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="af0b2-468">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="af0b2-468">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af0b2-469">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="af0b2-469">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="af0b2-470">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="af0b2-470">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="af0b2-471">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="af0b2-471">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="af0b2-472">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="af0b2-472">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="af0b2-473">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="af0b2-473">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="af0b2-474">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="af0b2-474">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="af0b2-475">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="af0b2-475">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="af0b2-476">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="af0b2-476">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="af0b2-477">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="af0b2-477">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-478">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="af0b2-478">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-479">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af0b2-479">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-481">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="af0b2-481">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-482">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="af0b2-482">State of the logical device.</span></span> <span data-ttu-id="af0b2-483">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="af0b2-483">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="af0b2-484">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af0b2-485">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="af0b2-485">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af0b2-486">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="af0b2-486">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="af0b2-487">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="af0b2-487">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="af0b2-488">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="af0b2-488">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af0b2-489">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="af0b2-489">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af0b2-490">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="af0b2-490">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-491">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-493">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af0b2-493">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-494">Proprietà **CreationClassName** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="af0b2-494">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="af0b2-495">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af0b2-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="af0b2-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af0b2-497">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af0b2-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-498">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af0b2-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af0b2-499">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af0b2-499">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af0b2-500">Proprietà **Name** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="af0b2-500">Scoping system's **Name** property.</span></span>

<span data-ttu-id="af0b2-501">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-501">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af0b2-502">Commenti</span><span class="sxs-lookup"><span data-stu-id="af0b2-502">Remarks</span></span>

<span data-ttu-id="af0b2-503">La classe **CIM \_ DisketteDrive** è derivata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-503">The **CIM\_DisketteDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="af0b2-504">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="af0b2-504">WMI does not implement this class.</span></span> <span data-ttu-id="af0b2-505">Per le classi derivate da **CIM \_ DisketteDrive**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="af0b2-505">For classes derived from **CIM\_DisketteDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="af0b2-506">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="af0b2-506">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="af0b2-507">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="af0b2-507">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="af0b2-508">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af0b2-508">Requirements</span></span>



| <span data-ttu-id="af0b2-509">Requisito</span><span class="sxs-lookup"><span data-stu-id="af0b2-509">Requirement</span></span> | <span data-ttu-id="af0b2-510">Valore</span><span class="sxs-lookup"><span data-stu-id="af0b2-510">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af0b2-511">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af0b2-511">Minimum supported client</span></span><br/> | <span data-ttu-id="af0b2-512">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af0b2-512">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af0b2-513">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af0b2-513">Minimum supported server</span></span><br/> | <span data-ttu-id="af0b2-514">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af0b2-514">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af0b2-515">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af0b2-515">Namespace</span></span><br/>                | <span data-ttu-id="af0b2-516">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="af0b2-516">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af0b2-517">MOF</span><span class="sxs-lookup"><span data-stu-id="af0b2-517">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af0b2-518"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af0b2-518"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af0b2-519">DLL</span><span class="sxs-lookup"><span data-stu-id="af0b2-519">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af0b2-520"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af0b2-520"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af0b2-521">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af0b2-521">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af0b2-522">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="af0b2-522">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 


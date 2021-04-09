---
description: La \_ classe CIM TapeDrive rappresenta un'unità nastro nel sistema. Le unità nastro si distinguono principalmente in quanto è possibile accedervi solo in modo sequenziale.
ms.assetid: 8b7f2277-e37d-4597-81bb-d3c8d4966a81
ms.tgt_platform: multiple
title: Classe CIM_TapeDrive (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.Availability
- CIM_TapeDrive.Capabilities
- CIM_TapeDrive.CapabilityDescriptions
- CIM_TapeDrive.Caption
- CIM_TapeDrive.CompressionMethod
- CIM_TapeDrive.ConfigManagerErrorCode
- CIM_TapeDrive.ConfigManagerUserConfig
- CIM_TapeDrive.CreationClassName
- CIM_TapeDrive.DefaultBlockSize
- CIM_TapeDrive.Description
- CIM_TapeDrive.DeviceID
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.ErrorCleared
- CIM_TapeDrive.ErrorDescription
- CIM_TapeDrive.ErrorMethodology
- CIM_TapeDrive.InstallDate
- CIM_TapeDrive.LastErrorCode
- CIM_TapeDrive.MaxBlockSize
- CIM_TapeDrive.MaxMediaSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.MinBlockSize
- CIM_TapeDrive.Name
- CIM_TapeDrive.NeedsCleaning
- CIM_TapeDrive.NumberOfMediaSupported
- CIM_TapeDrive.Padding
- CIM_TapeDrive.PNPDeviceID
- CIM_TapeDrive.PowerManagementCapabilities
- CIM_TapeDrive.PowerManagementSupported
- CIM_TapeDrive.Status
- CIM_TapeDrive.StatusInfo
- CIM_TapeDrive.SystemCreationClassName
- CIM_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 184b855d5989c77292e51e8b477c5392893deccb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878406"
---
# <a name="cim_tapedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="81034-104">Classe CIM_TapeDrive (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="81034-104">CIM_TapeDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="81034-105">La classe **CIM \_ TapeDrive** rappresenta un'unità nastro nel sistema.</span><span class="sxs-lookup"><span data-stu-id="81034-105">The **CIM\_TapeDrive** class represents a tape drive on the system.</span></span> <span data-ttu-id="81034-106">Le unità nastro si distinguono principalmente in quanto è possibile accedervi solo in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="81034-106">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81034-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="81034-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81034-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81034-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81034-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="81034-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="81034-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="81034-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81034-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81034-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_TapeDrive : CIM_MediaAccessDevice
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
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="81034-112">Members</span><span class="sxs-lookup"><span data-stu-id="81034-112">Members</span></span>

<span data-ttu-id="81034-113">La classe **CIM \_ TapeDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="81034-113">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="81034-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="81034-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="81034-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81034-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81034-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="81034-116">Methods</span></span>

<span data-ttu-id="81034-117">La classe **CIM \_ TapeDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="81034-117">The **CIM\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="81034-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="81034-118">Method</span></span>                                                               | <span data-ttu-id="81034-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81034-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81034-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="81034-120">**Reset**</span></span>](reset-method-in-class-cim-tapedrive.md)                 | <span data-ttu-id="81034-121">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="81034-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="81034-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="81034-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="81034-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="81034-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tapedrive.md) | <span data-ttu-id="81034-124">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="81034-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="81034-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="81034-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81034-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81034-126">Properties</span></span>

<span data-ttu-id="81034-127">La classe **CIM \_ TapeDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="81034-127">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81034-128">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="81034-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81034-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81034-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="81034-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="81034-132">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-132">Availability and status of the device.</span></span>

<span data-ttu-id="81034-133">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81034-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="81034-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81034-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="81034-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="81034-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="81034-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="81034-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="81034-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="81034-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="81034-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81034-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="81034-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="81034-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="81034-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="81034-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="81034-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="81034-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="81034-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81034-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="81034-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="81034-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="81034-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="81034-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="81034-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="81034-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="81034-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="81034-147">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="81034-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="81034-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="81034-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="81034-149">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="81034-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="81034-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="81034-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="81034-151">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="81034-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="81034-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="81034-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="81034-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="81034-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="81034-154">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="81034-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="81034-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="81034-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="81034-156">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="81034-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="81034-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="81034-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="81034-158">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="81034-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="81034-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="81034-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="81034-160">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="81034-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="81034-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="81034-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="81034-162">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="81034-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="81034-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-164">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81034-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81034-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-166">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="81034-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="81034-167">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="81034-167">Capabilities of the media access device.</span></span> <span data-ttu-id="81034-168">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-168">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81034-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="81034-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="81034-170">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="81034-170">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81034-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="81034-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="81034-172">Altro.</span><span class="sxs-lookup"><span data-stu-id="81034-172">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="81034-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="81034-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81034-174">Accesso sequenziale.</span><span class="sxs-lookup"><span data-stu-id="81034-174">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="81034-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="81034-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81034-176">Accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="81034-176">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="81034-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="81034-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="81034-178">Scrittura.</span><span class="sxs-lookup"><span data-stu-id="81034-178">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="81034-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="81034-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="81034-180">Crittografia.</span><span class="sxs-lookup"><span data-stu-id="81034-180">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="81034-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="81034-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="81034-182">Compressione.</span><span class="sxs-lookup"><span data-stu-id="81034-182">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="81034-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="81034-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="81034-184">Supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="81034-184">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="81034-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="81034-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="81034-186">Pulizia manuale.</span><span class="sxs-lookup"><span data-stu-id="81034-186">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="81034-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="81034-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="81034-188">Pulizia automatica.</span><span class="sxs-lookup"><span data-stu-id="81034-188">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="81034-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="81034-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="81034-190">Notifica intelligente.</span><span class="sxs-lookup"><span data-stu-id="81034-190">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="81034-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="81034-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="81034-192">Distingue un dispositivo che può accedere a entrambi i lati del supporto a doppio lato da un dispositivo che legge solo un singolo lato e richiede che il file multimediale venga riattivato.</span><span class="sxs-lookup"><span data-stu-id="81034-192">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="81034-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="81034-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="81034-194">Indica che non è necessario che il supporto venga espulso in modo esplicito dal dispositivo prima dell'accesso da parte di un elemento di selezione.</span><span class="sxs-lookup"><span data-stu-id="81034-194">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-195">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="81034-195">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-196">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="81034-196">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81034-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-198">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="81034-198">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="81034-199">Stringhe in formato libero che forniscono spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="81034-199">Free-form strings that provide detailed explanations for the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="81034-200">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="81034-200">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="81034-201">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-202">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="81034-202">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-205">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="81034-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="81034-206">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="81034-206">Short textual description of the object.</span></span>

<span data-ttu-id="81034-207">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81034-207">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-208">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="81034-208">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-211">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="81034-211">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="81034-212">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="81034-212">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="81034-213">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="81034-213">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="81034-214">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="81034-214">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="81034-215">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-215">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="81034-216">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="81034-216">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="81034-217">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="81034-217">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="81034-218">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="81034-218">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="81034-219">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="81034-219">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="81034-220">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="81034-220">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="81034-221">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="81034-221">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-222">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81034-222">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-223">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81034-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81034-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-225">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81034-225">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81034-226">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81034-226">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="81034-227">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-227">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="81034-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="81034-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="81034-229"> (0)</span><span class="sxs-lookup"><span data-stu-id="81034-229">(0)</span></span>


</dt> <dd>

<span data-ttu-id="81034-230">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="81034-230">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="81034-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="81034-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="81034-232">(1)</span><span class="sxs-lookup"><span data-stu-id="81034-232">(1)</span></span>


</dt> <dd>

<span data-ttu-id="81034-233">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="81034-233">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81034-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="81034-235">(2)</span><span class="sxs-lookup"><span data-stu-id="81034-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="81034-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="81034-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="81034-237">(3)</span><span class="sxs-lookup"><span data-stu-id="81034-237">(3)</span></span>


</dt> <dd>

<span data-ttu-id="81034-238">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="81034-238">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="81034-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="81034-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="81034-240">(4)</span><span class="sxs-lookup"><span data-stu-id="81034-240">(4)</span></span>


</dt> <dd>

<span data-ttu-id="81034-241">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="81034-241">Device is not working properly.</span></span> <span data-ttu-id="81034-242">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="81034-242">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="81034-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="81034-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="81034-244">(5)</span><span class="sxs-lookup"><span data-stu-id="81034-244">(5)</span></span>


</dt> <dd>

<span data-ttu-id="81034-245">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="81034-245">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="81034-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="81034-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="81034-247"> (6)</span><span class="sxs-lookup"><span data-stu-id="81034-247">(6)</span></span>


</dt> <dd>

<span data-ttu-id="81034-248">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="81034-248">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="81034-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="81034-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="81034-250">(7)</span><span class="sxs-lookup"><span data-stu-id="81034-250">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="81034-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="81034-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="81034-252">(8)</span><span class="sxs-lookup"><span data-stu-id="81034-252">(8)</span></span>


</dt> <dd>

<span data-ttu-id="81034-253">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="81034-253">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="81034-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="81034-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="81034-255">(9)</span><span class="sxs-lookup"><span data-stu-id="81034-255">(9)</span></span>


</dt> <dd>

<span data-ttu-id="81034-256">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="81034-256">Device is not working properly.</span></span> <span data-ttu-id="81034-257">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-257">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="81034-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="81034-259">(10)</span><span class="sxs-lookup"><span data-stu-id="81034-259">(10)</span></span>


</dt> <dd>

<span data-ttu-id="81034-260">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-260">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="81034-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="81034-262">(11)</span><span class="sxs-lookup"><span data-stu-id="81034-262">(11)</span></span>


</dt> <dd>

<span data-ttu-id="81034-263">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-263">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="81034-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="81034-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="81034-265">12</span><span class="sxs-lookup"><span data-stu-id="81034-265">(12)</span></span>


</dt> <dd>

<span data-ttu-id="81034-266">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="81034-266">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="81034-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="81034-268">(13)</span><span class="sxs-lookup"><span data-stu-id="81034-268">(13)</span></span>


</dt> <dd>

<span data-ttu-id="81034-269">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-269">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="81034-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="81034-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="81034-271">(14)</span><span class="sxs-lookup"><span data-stu-id="81034-271">(14)</span></span>


</dt> <dd>

<span data-ttu-id="81034-272">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="81034-272">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="81034-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="81034-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="81034-274">(15)</span><span class="sxs-lookup"><span data-stu-id="81034-274">(15)</span></span>


</dt> <dd>

<span data-ttu-id="81034-275">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="81034-275">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="81034-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="81034-277">(16)</span><span class="sxs-lookup"><span data-stu-id="81034-277">(16)</span></span>


</dt> <dd>

<span data-ttu-id="81034-278">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-278">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="81034-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="81034-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="81034-280">(17)</span><span class="sxs-lookup"><span data-stu-id="81034-280">(17)</span></span>


</dt> <dd>

<span data-ttu-id="81034-281">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="81034-281">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81034-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="81034-283">(18)</span><span class="sxs-lookup"><span data-stu-id="81034-283">(18)</span></span>


</dt> <dd>

<span data-ttu-id="81034-284">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-284">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="81034-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="81034-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="81034-286">(19)</span><span class="sxs-lookup"><span data-stu-id="81034-286">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="81034-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="81034-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="81034-288">(20)</span><span class="sxs-lookup"><span data-stu-id="81034-288">(20)</span></span>


</dt> <dd>

<span data-ttu-id="81034-289">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="81034-289">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="81034-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="81034-291">(21)</span><span class="sxs-lookup"><span data-stu-id="81034-291">(21)</span></span>


</dt> <dd>

<span data-ttu-id="81034-292">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="81034-292">System failure.</span></span> <span data-ttu-id="81034-293">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="81034-293">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="81034-294">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-294">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="81034-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="81034-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="81034-296">(22)</span><span class="sxs-lookup"><span data-stu-id="81034-296">(22)</span></span>


</dt> <dd>

<span data-ttu-id="81034-297">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="81034-297">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="81034-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="81034-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="81034-299">(23)</span><span class="sxs-lookup"><span data-stu-id="81034-299">(23)</span></span>


</dt> <dd>

<span data-ttu-id="81034-300">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="81034-300">System failure.</span></span> <span data-ttu-id="81034-301">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="81034-301">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="81034-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="81034-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="81034-303">(24)</span><span class="sxs-lookup"><span data-stu-id="81034-303">(24)</span></span>


</dt> <dd>

<span data-ttu-id="81034-304">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="81034-304">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="81034-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="81034-306">(25)</span><span class="sxs-lookup"><span data-stu-id="81034-306">(25)</span></span>


</dt> <dd>

<span data-ttu-id="81034-307">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="81034-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="81034-309">(26)</span><span class="sxs-lookup"><span data-stu-id="81034-309">(26)</span></span>


</dt> <dd>

<span data-ttu-id="81034-310">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-310">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="81034-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="81034-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="81034-312">(27)</span><span class="sxs-lookup"><span data-stu-id="81034-312">(27)</span></span>


</dt> <dd>

<span data-ttu-id="81034-313">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="81034-313">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="81034-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="81034-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="81034-315">(28)</span><span class="sxs-lookup"><span data-stu-id="81034-315">(28)</span></span>


</dt> <dd>

<span data-ttu-id="81034-316">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="81034-316">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="81034-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="81034-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="81034-318">(29)</span><span class="sxs-lookup"><span data-stu-id="81034-318">(29)</span></span>


</dt> <dd>

<span data-ttu-id="81034-319">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="81034-319">Device is disabled.</span></span> <span data-ttu-id="81034-320">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="81034-320">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="81034-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="81034-322">(30)</span><span class="sxs-lookup"><span data-stu-id="81034-322">(30)</span></span>


</dt> <dd>

<span data-ttu-id="81034-323">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-323">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81034-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81034-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="81034-325">31</span><span class="sxs-lookup"><span data-stu-id="81034-325">(31)</span></span>


</dt> <dd>

<span data-ttu-id="81034-326">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="81034-326">Device is not working properly.</span></span> <span data-ttu-id="81034-327">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="81034-327">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-328">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="81034-328">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-329">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="81034-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81034-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-331">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81034-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81034-332">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="81034-332">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="81034-333">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-333">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-334">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81034-334">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-335">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-337">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81034-337">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81034-338">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="81034-338">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="81034-339">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="81034-339">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="81034-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-341">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="81034-341">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81034-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81034-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-344">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="81034-344">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81034-345">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-345">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="81034-346">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-346">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="81034-347">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="81034-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="81034-348">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="81034-348">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-351">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="81034-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="81034-352">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="81034-352">Textual description of the object.</span></span>

<span data-ttu-id="81034-353">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81034-353">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-354">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="81034-354">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-357">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81034-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81034-358">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="81034-358">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="81034-359">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-360">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="81034-360">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-361">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81034-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81034-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-363">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="81034-363">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81034-364">Dimensione, in byte, dell'area designata come fine del nastro.</span><span class="sxs-lookup"><span data-stu-id="81034-364">Size, in bytes, of the area designated as end-of-tape.</span></span> <span data-ttu-id="81034-365">L'accesso in quest'area genera un avviso di fine nastro.</span><span class="sxs-lookup"><span data-stu-id="81034-365">Access in this area generates an end-of-tape warning.</span></span>

</dd> <dt>

<span data-ttu-id="81034-366">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="81034-366">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-367">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="81034-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81034-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-369">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="81034-369">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="81034-370">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-371">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="81034-371">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-372">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-374">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="81034-374">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="81034-375">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-376">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="81034-376">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-377">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-379">Stringa in formato libero che descrive i tipi di rilevamento e correzione degli errori supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-379">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="81034-380">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-380">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-381">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81034-381">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-382">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81034-382">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81034-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-384">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="81034-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="81034-385">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="81034-385">Date and time the object was installed.</span></span> <span data-ttu-id="81034-386">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="81034-386">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="81034-387">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81034-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-388">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81034-388">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-389">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81034-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81034-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-391">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="81034-391">Last error code reported by the logical device.</span></span>

<span data-ttu-id="81034-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-393">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="81034-393">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-394">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81034-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81034-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-396">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="81034-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81034-397">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-397">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="81034-398">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-398">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="81034-399">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="81034-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="81034-400">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="81034-400">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-401">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81034-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81034-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-403">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="81034-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="81034-404">Dimensioni massime, in kilobyte, dei supporti supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-404">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="81034-405">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="81034-405">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="81034-406">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-406">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="81034-407">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="81034-407">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="81034-408">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="81034-408">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-409">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81034-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81034-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-411">Numero massimo di partizioni per l'unità nastro.</span><span class="sxs-lookup"><span data-stu-id="81034-411">Maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="81034-412">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="81034-412">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-413">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81034-413">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81034-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-415">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="81034-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81034-416">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-416">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="81034-417">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="81034-418">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="81034-418">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="81034-419">**Nome**</span><span class="sxs-lookup"><span data-stu-id="81034-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-420">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-422">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="81034-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="81034-423">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="81034-423">Label by which the object is known.</span></span> <span data-ttu-id="81034-424">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="81034-424">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="81034-425">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81034-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-426">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="81034-426">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-427">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="81034-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81034-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-429">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="81034-429">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="81034-430">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà Array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="81034-430">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="81034-431">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-432">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="81034-432">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-433">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81034-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81034-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-435">Quando il dispositivo di accesso multimediale supporta più supporti singoli, questa proprietà definisce il numero massimo che può essere supportato o inserito.</span><span class="sxs-lookup"><span data-stu-id="81034-435">When the media access device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

<span data-ttu-id="81034-436">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-436">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-437">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="81034-437">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-438">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81034-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81034-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-440">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="81034-440">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="81034-441">Numero di byte inseriti tra blocchi su un supporto a nastro.</span><span class="sxs-lookup"><span data-stu-id="81034-441">Number of bytes inserted between blocks on a tape media.</span></span>

</dd> <dt>

<span data-ttu-id="81034-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="81034-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-443">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-445">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81034-445">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81034-446">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="81034-446">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="81034-447">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="81034-448">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="81034-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="81034-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81034-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-450">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81034-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81034-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-452">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="81034-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="81034-453">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="81034-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81034-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="81034-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="81034-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="81034-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="81034-456">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81034-456">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="81034-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="81034-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="81034-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="81034-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81034-459">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="81034-459">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="81034-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="81034-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="81034-461">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="81034-461">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="81034-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="81034-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="81034-463">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="81034-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="81034-464">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="81034-464">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="81034-465">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="81034-465">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="81034-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="81034-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="81034-467">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="81034-467">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="81034-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="81034-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="81034-469">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="81034-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="81034-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-471">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="81034-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81034-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81034-473">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="81034-473">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="81034-474">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="81034-474">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="81034-475">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="81034-475">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="81034-476">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="81034-476">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="81034-477">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-478">**Status**</span><span class="sxs-lookup"><span data-stu-id="81034-478">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-479">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-481">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="81034-481">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="81034-482">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="81034-482">Current status of the object.</span></span> <span data-ttu-id="81034-483">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81034-483">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="81034-484">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="81034-484">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="81034-485">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="81034-485">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="81034-486">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="81034-486">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81034-487">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="81034-487">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81034-488">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="81034-488">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="81034-489">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="81034-489">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="81034-490">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="81034-490">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="81034-491">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="81034-491">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="81034-492">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="81034-492">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="81034-493">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="81034-493">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="81034-494">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="81034-494">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="81034-495">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="81034-495">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="81034-496">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="81034-496">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-497">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="81034-497">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-498">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81034-498">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81034-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-500">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="81034-500">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="81034-501">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="81034-501">State of the logical device.</span></span> <span data-ttu-id="81034-502">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="81034-502">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="81034-503">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81034-504">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="81034-504">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81034-505">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="81034-505">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="81034-506">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="81034-506">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="81034-507">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="81034-507">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81034-508">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="81034-508">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81034-509">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81034-509">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-510">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-511">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-512">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81034-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81034-513">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="81034-513">Scoping system's creation class name.</span></span>

<span data-ttu-id="81034-514">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81034-515">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="81034-515">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81034-516">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81034-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81034-517">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81034-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81034-518">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="81034-518">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="81034-519">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="81034-519">Scoping system's name.</span></span>

<span data-ttu-id="81034-520">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-520">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81034-521">Commenti</span><span class="sxs-lookup"><span data-stu-id="81034-521">Remarks</span></span>

<span data-ttu-id="81034-522">La classe **CIM \_ TapeDrive** è derivata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81034-522">The **CIM\_TapeDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="81034-523">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="81034-523">WMI does not implement this class.</span></span> <span data-ttu-id="81034-524">Per le classi WMI derivate da **CIM \_ TapeDrive**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="81034-524">For WMI classes derived from **CIM\_TapeDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="81034-525">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="81034-525">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81034-526">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="81034-526">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81034-527">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81034-527">Requirements</span></span>



| <span data-ttu-id="81034-528">Requisito</span><span class="sxs-lookup"><span data-stu-id="81034-528">Requirement</span></span> | <span data-ttu-id="81034-529">Valore</span><span class="sxs-lookup"><span data-stu-id="81034-529">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81034-530">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81034-530">Minimum supported client</span></span><br/> | <span data-ttu-id="81034-531">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81034-531">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81034-532">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81034-532">Minimum supported server</span></span><br/> | <span data-ttu-id="81034-533">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81034-533">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81034-534">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81034-534">Namespace</span></span><br/>                | <span data-ttu-id="81034-535">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="81034-535">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81034-536">MOF</span><span class="sxs-lookup"><span data-stu-id="81034-536">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81034-537"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81034-537"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81034-538">DLL</span><span class="sxs-lookup"><span data-stu-id="81034-538">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81034-539"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81034-539"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81034-540">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81034-540">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81034-541">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="81034-541">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 


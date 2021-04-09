---
description: La \_ classe CIM CDROMDrive rappresenta un'unità CD-ROM nel computer.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: Classe CIM_CDROMDrive (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877997"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="607a7-103">Classe CIM_CDROMDrive (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="607a7-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="607a7-104">La classe **CIM \_ CDROMDrive** rappresenta un'unità CD-ROM nel computer.</span><span class="sxs-lookup"><span data-stu-id="607a7-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="607a7-105">Il nome dell'unità non corrisponde alla lettera di unità logica assegnata al dispositivo, che corrisponde al nome del dispositivo di archiviazione logica dipendente dall'unità.</span><span class="sxs-lookup"><span data-stu-id="607a7-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="607a7-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="607a7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="607a7-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="607a7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="607a7-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="607a7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="607a7-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="607a7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="607a7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="607a7-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="607a7-111">Members</span><span class="sxs-lookup"><span data-stu-id="607a7-111">Members</span></span>

<span data-ttu-id="607a7-112">La classe **CIM \_ CDROMDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="607a7-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="607a7-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="607a7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="607a7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="607a7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="607a7-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="607a7-115">Methods</span></span>

<span data-ttu-id="607a7-116">La classe **CIM \_ CDROMDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="607a7-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="607a7-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="607a7-117">Method</span></span>                                                                | <span data-ttu-id="607a7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="607a7-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="607a7-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="607a7-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="607a7-120">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="607a7-121">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="607a7-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="607a7-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="607a7-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="607a7-123">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="607a7-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="607a7-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="607a7-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="607a7-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="607a7-125">Properties</span></span>

<span data-ttu-id="607a7-126">La classe **CIM \_ CDROMDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="607a7-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="607a7-127">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="607a7-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="607a7-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-130">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="607a7-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-131">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-131">Availability and status of the device.</span></span>

<span data-ttu-id="607a7-132">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="607a7-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="607a7-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="607a7-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="607a7-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="607a7-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="607a7-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="607a7-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="607a7-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="607a7-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="607a7-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="607a7-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="607a7-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="607a7-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="607a7-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="607a7-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="607a7-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="607a7-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="607a7-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="607a7-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="607a7-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="607a7-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="607a7-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="607a7-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="607a7-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="607a7-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="607a7-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-146">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="607a7-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="607a7-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="607a7-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-148">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="607a7-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="607a7-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="607a7-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-150">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="607a7-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="607a7-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="607a7-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="607a7-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="607a7-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-153">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="607a7-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="607a7-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="607a7-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-155">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="607a7-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="607a7-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="607a7-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-157">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="607a7-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="607a7-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="607a7-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-159">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="607a7-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="607a7-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="607a7-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-161">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="607a7-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="607a7-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-163">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="607a7-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="607a7-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-165">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="607a7-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-166">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="607a7-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="607a7-167">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="607a7-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="607a7-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-169">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="607a7-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="607a7-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="607a7-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-171">Altro.</span><span class="sxs-lookup"><span data-stu-id="607a7-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="607a7-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="607a7-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-173">Accesso sequenziale.</span><span class="sxs-lookup"><span data-stu-id="607a7-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="607a7-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="607a7-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-175">Accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="607a7-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="607a7-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="607a7-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-177">Scrittura.</span><span class="sxs-lookup"><span data-stu-id="607a7-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="607a7-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="607a7-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-179">Crittografia.</span><span class="sxs-lookup"><span data-stu-id="607a7-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="607a7-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="607a7-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-181">Compressione.</span><span class="sxs-lookup"><span data-stu-id="607a7-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="607a7-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="607a7-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-183">Supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="607a7-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="607a7-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="607a7-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-185">Pulizia manuale.</span><span class="sxs-lookup"><span data-stu-id="607a7-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="607a7-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="607a7-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-187">Pulizia automatica.</span><span class="sxs-lookup"><span data-stu-id="607a7-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="607a7-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="607a7-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-189">Notifica intelligente.</span><span class="sxs-lookup"><span data-stu-id="607a7-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="607a7-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="607a7-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-191">Distingue un dispositivo che può accedere a entrambi i lati del supporto a doppio lato da un dispositivo che legge solo un singolo lato e richiede che il file multimediale venga riattivato.</span><span class="sxs-lookup"><span data-stu-id="607a7-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="607a7-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="607a7-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-193">Indica che non è necessario che il supporto venga espulso in modo esplicito dal dispositivo prima dell'accesso da parte di un elemento di selezione.</span><span class="sxs-lookup"><span data-stu-id="607a7-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-194">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="607a7-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-195">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="607a7-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="607a7-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-197">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="607a7-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-198">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="607a7-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="607a7-199">Ogni voce di questa matrice è correlata alla voce nella matrice di **funzionalità** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="607a7-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="607a7-200">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-201">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="607a7-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-204">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="607a7-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-205">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="607a7-205">A short textual description of the object.</span></span>

<span data-ttu-id="607a7-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="607a7-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-210">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="607a7-211">Se non è possibile descrivere lo schema di compressione (perché è sconosciuto), usare il comando seguente: If, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="607a7-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="607a7-212">Se, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="607a7-212">If , use "Compressed".</span></span> <span data-ttu-id="607a7-213">usare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="607a7-213">, use "Not Compressed".</span></span>

<span data-ttu-id="607a7-214">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="607a7-215">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="607a7-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="607a7-216">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="607a7-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="607a7-217">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="607a7-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="607a7-218">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="607a7-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="607a7-219">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="607a7-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="607a7-220">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="607a7-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-221">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="607a7-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-222">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607a7-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-224">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="607a7-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-225">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="607a7-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="607a7-226">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="607a7-227">**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="607a7-227">**This device is working properly.**</span></span> <span data-ttu-id="607a7-228"> (0)</span><span class="sxs-lookup"><span data-stu-id="607a7-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="607a7-229">**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="607a7-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="607a7-230">(1)</span><span class="sxs-lookup"><span data-stu-id="607a7-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="607a7-231">**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="607a7-232">(2)</span><span class="sxs-lookup"><span data-stu-id="607a7-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="607a7-233">**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="607a7-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="607a7-234">(3)</span><span class="sxs-lookup"><span data-stu-id="607a7-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="607a7-235">**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="607a7-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="607a7-236">(4)</span><span class="sxs-lookup"><span data-stu-id="607a7-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="607a7-237">**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="607a7-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="607a7-238">(5)</span><span class="sxs-lookup"><span data-stu-id="607a7-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="607a7-239">**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="607a7-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="607a7-240"> (6)</span><span class="sxs-lookup"><span data-stu-id="607a7-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="607a7-241">**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="607a7-241">**Cannot filter.**</span></span> <span data-ttu-id="607a7-242">(7)</span><span class="sxs-lookup"><span data-stu-id="607a7-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="607a7-243">**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="607a7-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="607a7-244">(8)</span><span class="sxs-lookup"><span data-stu-id="607a7-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="607a7-245">**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="607a7-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="607a7-246">(9)</span><span class="sxs-lookup"><span data-stu-id="607a7-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="607a7-247">**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-247">**This device cannot start.**</span></span> <span data-ttu-id="607a7-248">(10)</span><span class="sxs-lookup"><span data-stu-id="607a7-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="607a7-249">**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-249">**This device failed.**</span></span> <span data-ttu-id="607a7-250">(11)</span><span class="sxs-lookup"><span data-stu-id="607a7-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="607a7-251">**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="607a7-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="607a7-252">12</span><span class="sxs-lookup"><span data-stu-id="607a7-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="607a7-253">**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="607a7-254">(13)</span><span class="sxs-lookup"><span data-stu-id="607a7-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="607a7-255">**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="607a7-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="607a7-256">(14)</span><span class="sxs-lookup"><span data-stu-id="607a7-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="607a7-257">**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="607a7-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="607a7-258">(15)</span><span class="sxs-lookup"><span data-stu-id="607a7-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="607a7-259">**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="607a7-260">(16)</span><span class="sxs-lookup"><span data-stu-id="607a7-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="607a7-261">**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="607a7-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="607a7-262">(17)</span><span class="sxs-lookup"><span data-stu-id="607a7-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="607a7-263">**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="607a7-264">(18)</span><span class="sxs-lookup"><span data-stu-id="607a7-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="607a7-265">**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="607a7-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="607a7-266">(19)</span><span class="sxs-lookup"><span data-stu-id="607a7-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="607a7-267">**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="607a7-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="607a7-268">(20)</span><span class="sxs-lookup"><span data-stu-id="607a7-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="607a7-269">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="607a7-270">(21)</span><span class="sxs-lookup"><span data-stu-id="607a7-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="607a7-271">**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="607a7-271">**This device is disabled.**</span></span> <span data-ttu-id="607a7-272">(22)</span><span class="sxs-lookup"><span data-stu-id="607a7-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="607a7-273">**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="607a7-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="607a7-274">(23)</span><span class="sxs-lookup"><span data-stu-id="607a7-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="607a7-275">**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="607a7-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="607a7-276">(24)</span><span class="sxs-lookup"><span data-stu-id="607a7-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="607a7-277">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="607a7-278">(25)</span><span class="sxs-lookup"><span data-stu-id="607a7-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="607a7-279">**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="607a7-280">(26)</span><span class="sxs-lookup"><span data-stu-id="607a7-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="607a7-281">**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="607a7-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="607a7-282">(27)</span><span class="sxs-lookup"><span data-stu-id="607a7-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="607a7-283">**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="607a7-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="607a7-284">(28)</span><span class="sxs-lookup"><span data-stu-id="607a7-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="607a7-285">**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="607a7-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="607a7-286">(29)</span><span class="sxs-lookup"><span data-stu-id="607a7-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="607a7-287">**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="607a7-288">(30)</span><span class="sxs-lookup"><span data-stu-id="607a7-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="607a7-289">**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="607a7-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="607a7-290">31</span><span class="sxs-lookup"><span data-stu-id="607a7-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="607a7-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-292">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="607a7-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-294">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="607a7-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-295">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="607a7-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="607a7-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="607a7-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-300">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="607a7-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="607a7-301">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="607a7-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="607a7-302">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="607a7-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="607a7-303">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-304">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="607a7-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-305">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="607a7-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-307">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="607a7-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-308">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="607a7-309">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="607a7-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="607a7-310">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-311">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="607a7-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-314">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="607a7-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-315">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="607a7-315">A textual description of the object.</span></span>

<span data-ttu-id="607a7-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="607a7-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-320">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="607a7-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="607a7-321">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="607a7-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="607a7-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-324">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="607a7-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-326">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="607a7-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="607a7-327">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="607a7-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-331">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="607a7-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="607a7-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-333">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="607a7-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-336">Stringa in formato libero che descrive i tipi di rilevamento e correzione degli errori supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="607a7-337">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="607a7-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-339">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="607a7-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-341">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="607a7-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-342">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="607a7-342">Indicates when the object was installed.</span></span> <span data-ttu-id="607a7-343">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="607a7-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="607a7-344">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="607a7-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-346">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607a7-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-348">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="607a7-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-350">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="607a7-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-351">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="607a7-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-353">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="607a7-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-354">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="607a7-355">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="607a7-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="607a7-356">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-357">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="607a7-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-358">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="607a7-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-360">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="607a7-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-361">Dimensioni massime, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="607a7-362">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="607a7-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="607a7-363">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="607a7-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="607a7-364">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-365">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="607a7-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-366">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="607a7-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-368">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="607a7-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-369">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="607a7-370">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="607a7-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="607a7-371">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-372">**Nome**</span><span class="sxs-lookup"><span data-stu-id="607a7-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-373">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-375">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="607a7-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-376">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="607a7-376">Label by which the object is known.</span></span> <span data-ttu-id="607a7-377">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="607a7-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="607a7-378">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-379">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="607a7-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-380">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="607a7-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-382">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="607a7-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="607a7-383">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà Array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="607a7-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="607a7-384">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-385">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="607a7-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-386">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607a7-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-388">Numero massimo di supporti singoli che possono essere supportati o inseriti.</span><span class="sxs-lookup"><span data-stu-id="607a7-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="607a7-389">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="607a7-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-393">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="607a7-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-394">Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="607a7-395">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="607a7-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="607a7-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-397">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="607a7-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-398">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="607a7-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="607a7-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-400">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="607a7-401">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="607a7-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="607a7-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-403">Le capacità relative al risparmio di energia sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="607a7-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="607a7-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="607a7-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-405">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="607a7-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="607a7-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="607a7-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-407">Le capacità correlate all'alimentazione sono state disabilitate.</span><span class="sxs-lookup"><span data-stu-id="607a7-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="607a7-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="607a7-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-409">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="607a7-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="607a7-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="607a7-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-411">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="607a7-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="607a7-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="607a7-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-413">Il metodo **SetPowerState** è supportato.</span><span class="sxs-lookup"><span data-stu-id="607a7-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="607a7-414">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="607a7-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="607a7-415">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="607a7-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="607a7-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="607a7-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-417">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="607a7-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="607a7-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="607a7-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="607a7-419">Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="607a7-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-420">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="607a7-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-421">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="607a7-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="607a7-423">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="607a7-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="607a7-424">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="607a7-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="607a7-425">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="607a7-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="607a7-426">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="607a7-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="607a7-427">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-428">**Status**</span><span class="sxs-lookup"><span data-stu-id="607a7-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-429">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-431">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="607a7-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-432">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="607a7-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="607a7-433">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="607a7-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="607a7-434">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="607a7-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="607a7-435">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="607a7-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="607a7-436">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="607a7-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="607a7-437">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="607a7-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="607a7-438">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="607a7-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="607a7-439">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="607a7-440">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="607a7-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="607a7-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="607a7-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="607a7-442">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="607a7-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="607a7-443">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="607a7-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="607a7-444">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="607a7-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="607a7-445">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="607a7-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="607a7-446">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="607a7-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="607a7-447">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="607a7-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="607a7-448">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="607a7-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="607a7-449">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="607a7-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="607a7-450">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="607a7-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="607a7-451">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="607a7-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="607a7-452">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="607a7-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="607a7-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-454">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="607a7-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-456">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="607a7-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="607a7-457">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="607a7-457">State of the logical device.</span></span> <span data-ttu-id="607a7-458">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="607a7-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="607a7-459">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="607a7-460">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="607a7-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="607a7-461">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="607a7-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="607a7-462">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="607a7-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="607a7-463">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="607a7-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="607a7-464">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="607a7-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="607a7-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="607a7-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-466">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-468">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="607a7-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="607a7-469">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="607a7-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="607a7-470">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="607a7-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="607a7-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="607a7-472">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="607a7-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="607a7-473">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="607a7-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="607a7-474">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="607a7-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="607a7-475">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="607a7-475">The scoping system's name.</span></span>

<span data-ttu-id="607a7-476">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="607a7-477">Commenti</span><span class="sxs-lookup"><span data-stu-id="607a7-477">Remarks</span></span>

<span data-ttu-id="607a7-478">La classe **CIM \_ CDROMDrive** è derivata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="607a7-479">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="607a7-479">WMI does not implement this class.</span></span> <span data-ttu-id="607a7-480">Per ulteriori informazioni sulle classi derivate da **CIM \_ CDROMDrive**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="607a7-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="607a7-481">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="607a7-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="607a7-482">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="607a7-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="607a7-483">Requisiti</span><span class="sxs-lookup"><span data-stu-id="607a7-483">Requirements</span></span>



| <span data-ttu-id="607a7-484">Requisito</span><span class="sxs-lookup"><span data-stu-id="607a7-484">Requirement</span></span> | <span data-ttu-id="607a7-485">Valore</span><span class="sxs-lookup"><span data-stu-id="607a7-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="607a7-486">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607a7-486">Minimum supported client</span></span><br/> | <span data-ttu-id="607a7-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="607a7-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="607a7-488">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607a7-488">Minimum supported server</span></span><br/> | <span data-ttu-id="607a7-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="607a7-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="607a7-490">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="607a7-490">Namespace</span></span><br/>                | <span data-ttu-id="607a7-491">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="607a7-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="607a7-492">MOF</span><span class="sxs-lookup"><span data-stu-id="607a7-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="607a7-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="607a7-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="607a7-494">DLL</span><span class="sxs-lookup"><span data-stu-id="607a7-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="607a7-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="607a7-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607a7-496">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="607a7-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607a7-497">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="607a7-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 


---
description: La \_ classe CIM DiskDrive rappresenta un'unità disco fisica visualizzata dal sistema operativo.
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: Classe CIM_DiskDrive (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225722"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="1fc1b-103">Classe CIM_DiskDrive (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1fc1b-104">La classe **CIM \_ DiskDrive** rappresenta un'unità disco fisica visualizzata dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="1fc1b-105">Le funzionalità dell'unità disco corrispondono alle caratteristiche logiche e di gestione dell'unità e, in alcuni casi, potrebbero non riflettere le caratteristiche fisiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="1fc1b-106">Un'interfaccia a un'unità fisica è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="1fc1b-107">Tuttavia, un oggetto basato su un altro dispositivo logico non è un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fc1b-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1fc1b-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1fc1b-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1fc1b-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc1b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fc1b-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="1fc1b-113">Members</span><span class="sxs-lookup"><span data-stu-id="1fc1b-113">Members</span></span>

<span data-ttu-id="1fc1b-114">La classe **CIM \_ DiskDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1fc1b-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="1fc1b-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fc1b-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="1fc1b-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1fc1b-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1fc1b-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fc1b-117">Methods</span></span>

<span data-ttu-id="1fc1b-118">La classe **CIM \_ DiskDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="1fc1b-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="1fc1b-119">Method</span></span>                                                                | <span data-ttu-id="1fc1b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fc1b-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fc1b-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="1fc1b-122">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="1fc1b-123">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="1fc1b-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="1fc1b-125">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1fc1b-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1fc1b-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1fc1b-127">Properties</span></span>

<span data-ttu-id="1fc1b-128">La classe **CIM \_ DiskDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fc1b-129">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-132">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-133">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-133">Availability and status of the device.</span></span>

<span data-ttu-id="1fc1b-134">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1fc1b-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-136">Altro.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fc1b-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-138">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1fc1b-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-140">Esecuzione/potenza piena.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1fc1b-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-142">Avviso.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1fc1b-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-144">Test.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1fc1b-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-146">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1fc1b-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="1fc1b-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-148">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1fc1b-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="1fc1b-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1fc1b-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-152">Fuori servizio.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1fc1b-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-154">Danneggiato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1fc1b-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-156">Non installato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1fc1b-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-158">Errore di installazione.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1fc1b-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-160">Il dispositivo è noto in modalità di risparmio energia, ma lo stato esatto in questa modalità è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1fc1b-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-162">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1fc1b-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-164">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa "rapidamente".</span><span class="sxs-lookup"><span data-stu-id="1fc1b-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1fc1b-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-166">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1fc1b-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-168">Il dispositivo è in uno stato di avviso e anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1fc1b-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-170">(sospeso)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1fc1b-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-172">Non pronto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1fc1b-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-174">Non configurata.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1fc1b-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-176">L'unità disco non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-177">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-178">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-180">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-181">Funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-181">Capabilities of the media access device.</span></span> <span data-ttu-id="1fc1b-182">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fc1b-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-184">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1fc1b-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-186">Altro.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="1fc1b-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-188">Accesso sequenziale.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="1fc1b-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-190">Accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="1fc1b-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-192">Scrittura.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="1fc1b-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-194">Crittografia.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="1fc1b-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-196">Compressione.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="1fc1b-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-198">Supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="1fc1b-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-200">Pulizia manuale.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="1fc1b-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-202">Pulizia automatica.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="1fc1b-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-204">Notifica intelligente.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="1fc1b-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-206">Distingue un dispositivo che può accedere a entrambi i lati del supporto a doppio lato da un dispositivo che legge solo un singolo lato e richiede che il file multimediale venga riattivato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="1fc1b-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-208">Indica che non è necessario che il supporto venga espulso in modo esplicito dal dispositivo prima dell'accesso da parte di un elemento di selezione.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-209">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-210">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-212">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-213">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="1fc1b-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="1fc1b-214">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="1fc1b-215">Ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="1fc1b-216">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-219">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-220">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-220">Short textual description of the object.</span></span>

<span data-ttu-id="1fc1b-221">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-222">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-225">Stringa in formato libero che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="1fc1b-226">Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown".</span><span class="sxs-lookup"><span data-stu-id="1fc1b-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="1fc1b-227">Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso".</span><span class="sxs-lookup"><span data-stu-id="1fc1b-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="1fc1b-228">Se il file logico non è compresso, utilizzare "non compresso".</span><span class="sxs-lookup"><span data-stu-id="1fc1b-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="1fc1b-229">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="1fc1b-230">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-231">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="1fc1b-232">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-233">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="1fc1b-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="1fc1b-234">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-235">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="1fc1b-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-236">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-237">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-239">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-240">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="1fc1b-241">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1fc1b-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1fc1b-243"> (0)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-244">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1fc1b-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1fc1b-246">(1)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-247">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1fc1b-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1fc1b-249">(2)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1fc1b-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1fc1b-251">(3)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-252">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1fc1b-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1fc1b-254">(4)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-255">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-255">Device is not working properly.</span></span> <span data-ttu-id="1fc1b-256">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1fc1b-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1fc1b-258">(5)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-259">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1fc1b-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1fc1b-261"> (6)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-262">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1fc1b-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1fc1b-264">(7)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1fc1b-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1fc1b-266">(8)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-267">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1fc1b-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1fc1b-269">(9)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-270">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1fc1b-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1fc1b-272">(10)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-273">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1fc1b-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1fc1b-275">(11)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-276">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1fc1b-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1fc1b-278">12</span><span class="sxs-lookup"><span data-stu-id="1fc1b-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-279">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1fc1b-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1fc1b-281">(13)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-282">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1fc1b-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1fc1b-284">(14)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-285">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1fc1b-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1fc1b-287">(15)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-288">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1fc1b-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1fc1b-290">(16)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-291">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1fc1b-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1fc1b-293">(17)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-294">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1fc1b-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1fc1b-296">(18)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-297">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1fc1b-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1fc1b-299">(19)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1fc1b-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1fc1b-301">(20)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-302">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1fc1b-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1fc1b-304">(21)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-305">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-305">System failure.</span></span> <span data-ttu-id="1fc1b-306">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1fc1b-307">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1fc1b-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1fc1b-309">(22)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-310">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1fc1b-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1fc1b-312">(23)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-313">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-313">System failure.</span></span> <span data-ttu-id="1fc1b-314">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1fc1b-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1fc1b-316">(24)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-317">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1fc1b-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1fc1b-319">(25)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-320">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1fc1b-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1fc1b-322">(26)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-323">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1fc1b-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1fc1b-325">(27)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-326">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1fc1b-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1fc1b-328">(28)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-329">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1fc1b-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1fc1b-331">(29)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-332">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1fc1b-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1fc1b-334">(30)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-335">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1fc1b-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1fc1b-337">31</span><span class="sxs-lookup"><span data-stu-id="1fc1b-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-338">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-339">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-340">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-342">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-343">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1fc1b-344">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-345">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-348">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-349">Nome della classe (o sottoclasse) utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="1fc1b-350">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1fc1b-351">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-352">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-353">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-355">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-356">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="1fc1b-357">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="1fc1b-358">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-359">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-362">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-363">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-363">Textual description of the object.</span></span>

<span data-ttu-id="1fc1b-364">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-365">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-366">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-368">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-369">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1fc1b-370">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-371">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-372">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-374">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è deselezionato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="1fc1b-375">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-377">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-379">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1fc1b-380">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-381">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-384">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="1fc1b-385">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-387">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-389">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-390">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-390">Date and time when the object was installed.</span></span> <span data-ttu-id="1fc1b-391">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1fc1b-392">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-394">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-396">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1fc1b-397">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-398">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-399">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-401">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-402">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="1fc1b-403">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="1fc1b-404">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-405">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-406">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-408">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-409">Dimensioni massime, in kilobyte, dei supporti supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="1fc1b-410">I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="1fc1b-411">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="1fc1b-412">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-413">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-414">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-416">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-417">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="1fc1b-418">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="1fc1b-419">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-420">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-423">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-424">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-424">Label by which the object is known.</span></span> <span data-ttu-id="1fc1b-425">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1fc1b-426">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-427">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-428">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-430">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="1fc1b-431">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà Array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="1fc1b-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="1fc1b-432">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-433">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-434">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-436">Quando il dispositivo di accesso multimediale supporta più supporti singoli, questa proprietà definisce il numero massimo che può essere supportato o inserito.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="1fc1b-437">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-441">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-442">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1fc1b-443">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1fc1b-444">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1fc1b-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-445">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-446">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-448">Funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="1fc1b-449">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fc1b-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-451">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1fc1b-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-453">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1fc1b-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-455">Disattivato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1fc1b-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-457">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1fc1b-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-459">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1fc1b-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-461">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1fc1b-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-463">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="1fc1b-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1fc1b-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1fc1b-465">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-466">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-467">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-468">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-469">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1fc1b-470">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1fc1b-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1fc1b-471">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1fc1b-472">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1fc1b-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="1fc1b-473">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-474">**Status**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-475">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-477">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-478">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-478">Current status of the object.</span></span>

<span data-ttu-id="1fc1b-479">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1fc1b-480">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1fc1b-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1fc1b-481">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1fc1b-482">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1fc1b-483">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="1fc1b-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fc1b-484">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1fc1b-485">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1fc1b-486">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1fc1b-487">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1fc1b-488">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1fc1b-489">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1fc1b-490">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1fc1b-491">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1fc1b-492">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-494">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-495">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-496">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1fc1b-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-497">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-497">State of the logical device.</span></span> <span data-ttu-id="1fc1b-498">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1fc1b-499">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1fc1b-500">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fc1b-501">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1fc1b-502">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1fc1b-503">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1fc1b-504">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1fc1b-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-506">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-508">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-509">Proprietà **CreationClassName** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="1fc1b-510">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc1b-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc1b-512">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1fc1b-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc1b-514">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1fc1b-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1fc1b-515">Proprietà **Name** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="1fc1b-516">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fc1b-517">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fc1b-517">Remarks</span></span>

<span data-ttu-id="1fc1b-518">La classe **CIM \_ DiskDrive** è derivata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1b-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="1fc1b-519">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-519">WMI does not implement this class.</span></span> <span data-ttu-id="1fc1b-520">Vedere [le classi Win32](win32-provider.md) per le classi derivate da **CIM \_ DiskDrive**.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="1fc1b-521">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1fc1b-522">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1fc1b-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc1b-523">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fc1b-523">Requirements</span></span>



| <span data-ttu-id="1fc1b-524">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc1b-524">Requirement</span></span> | <span data-ttu-id="1fc1b-525">Valore</span><span class="sxs-lookup"><span data-stu-id="1fc1b-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc1b-526">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fc1b-526">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc1b-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fc1b-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fc1b-528">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fc1b-528">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc1b-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fc1b-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fc1b-530">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1fc1b-530">Namespace</span></span><br/>                | <span data-ttu-id="1fc1b-531">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1fc1b-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1fc1b-532">MOF</span><span class="sxs-lookup"><span data-stu-id="1fc1b-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fc1b-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fc1b-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fc1b-534">DLL</span><span class="sxs-lookup"><span data-stu-id="1fc1b-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc1b-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc1b-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc1b-536">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fc1b-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc1b-537">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1fc1b-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 


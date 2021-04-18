---
description: La \_ classe CIM volumet rappresenta un intervallo contiguo di blocchi logici presentati all'ambiente operativo per la lettura e la scrittura di dati utente.
ms.assetid: f0350185-6210-4f95-a2a2-23de61b1af1f
ms.tgt_platform: multiple
title: Classe CIM_VolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolumeSet
- CIM_VolumeSet.Access
- CIM_VolumeSet.Availability
- CIM_VolumeSet.BlockSize
- CIM_VolumeSet.Caption
- CIM_VolumeSet.ConfigManagerErrorCode
- CIM_VolumeSet.ConfigManagerUserConfig
- CIM_VolumeSet.CreationClassName
- CIM_VolumeSet.Description
- CIM_VolumeSet.DeviceID
- CIM_VolumeSet.ErrorCleared
- CIM_VolumeSet.ErrorDescription
- CIM_VolumeSet.ErrorMethodology
- CIM_VolumeSet.InstallDate
- CIM_VolumeSet.LastErrorCode
- CIM_VolumeSet.Name
- CIM_VolumeSet.NumberOfBlocks
- CIM_VolumeSet.PNPDeviceID
- CIM_VolumeSet.PowerManagementCapabilities
- CIM_VolumeSet.PowerManagementSupported
- CIM_VolumeSet.PSExtentInterleaveDepth
- CIM_VolumeSet.PSExtentStripeLength
- CIM_VolumeSet.Purpose
- CIM_VolumeSet.Status
- CIM_VolumeSet.StatusInfo
- CIM_VolumeSet.SystemCreationClassName
- CIM_VolumeSet.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ee8cd96381901250c9a15e544ee1963470565b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304530"
---
# <a name="cim_volumeset-class"></a><span data-ttu-id="920af-103">\_Classe di volumi CIM</span><span class="sxs-lookup"><span data-stu-id="920af-103">CIM\_VolumeSet class</span></span>

<span data-ttu-id="920af-104">La classe **CIM \_ volumet** rappresenta un intervallo contiguo di blocchi logici presentati all'ambiente operativo per la lettura e la scrittura di dati utente.</span><span class="sxs-lookup"><span data-stu-id="920af-104">The **CIM\_VolumeSet** class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span> <span data-ttu-id="920af-105">I set di volumi non devono sovrapporsi tra loro e sono basati su uno o più extent fisici, extent dello spazio protetto o extent aggregati (tutti dello stesso tipo).</span><span class="sxs-lookup"><span data-stu-id="920af-105">Volume sets should not overlap one another and are based on one or more physical extents, protected space extents, or aggregate extents (all of the same type).</span></span> <span data-ttu-id="920af-106">Per le associazioni basate su è necessario creare un'istanza o sottoclassare secondo le esigenze.</span><span class="sxs-lookup"><span data-stu-id="920af-106">The based-on associations should be instantiated or subclassed as needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="920af-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="920af-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="920af-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="920af-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="920af-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="920af-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="920af-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="920af-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="920af-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="920af-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{35E25AA5-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VolumeSet : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   PSExtentInterleaveDepth;
  uint64   PSExtentStripeLength;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="920af-112">Members</span><span class="sxs-lookup"><span data-stu-id="920af-112">Members</span></span>

<span data-ttu-id="920af-113">La classe **CIM del \_ volumet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="920af-113">The **CIM\_VolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="920af-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="920af-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="920af-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="920af-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="920af-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="920af-116">Methods</span></span>

<span data-ttu-id="920af-117">La classe **CIM del \_ volumet** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="920af-117">The **CIM\_VolumeSet** class has these methods.</span></span>



| <span data-ttu-id="920af-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="920af-118">Method</span></span>                                                               | <span data-ttu-id="920af-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="920af-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="920af-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="920af-120">**Reset**</span></span>](reset-method-in-class-cim-volumeset.md)                 | <span data-ttu-id="920af-121">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="920af-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="920af-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="920af-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="920af-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="920af-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volumeset.md) | <span data-ttu-id="920af-124">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="920af-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="920af-125">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="920af-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="920af-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="920af-126">Properties</span></span>

<span data-ttu-id="920af-127">La classe **CIM del \_ volumet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="920af-127">The **CIM\_VolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="920af-128">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="920af-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="920af-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="920af-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-131">Proprietà di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="920af-131">Read/write properties of the media.</span></span>

<span data-ttu-id="920af-132">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="920af-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="920af-133">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="920af-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="920af-134">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="920af-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="920af-135">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="920af-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="920af-136">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="920af-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="920af-137">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="920af-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="920af-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="920af-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="920af-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="920af-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-141">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="920af-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="920af-142">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-142">Availability and status of the device.</span></span>

<span data-ttu-id="920af-143">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="920af-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="920af-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="920af-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="920af-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="920af-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="920af-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="920af-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="920af-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="920af-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="920af-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="920af-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="920af-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="920af-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="920af-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="920af-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="920af-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="920af-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="920af-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="920af-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="920af-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="920af-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="920af-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="920af-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="920af-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="920af-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="920af-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="920af-157">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="920af-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="920af-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="920af-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="920af-159">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="920af-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="920af-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="920af-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="920af-161">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="920af-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="920af-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="920af-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="920af-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="920af-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="920af-164">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="920af-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="920af-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="920af-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="920af-166">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="920af-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="920af-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="920af-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="920af-168">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="920af-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="920af-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="920af-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="920af-170">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="920af-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="920af-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="920af-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="920af-172">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="920af-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="920af-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="920af-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-174">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="920af-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="920af-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-176">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="920af-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="920af-177">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="920af-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="920af-178">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="920af-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="920af-179">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="920af-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="920af-180">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="920af-180">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="920af-181">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="920af-181">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="920af-182">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="920af-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-185">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="920af-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="920af-186">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="920af-186">Short textual description of the object.</span></span>

<span data-ttu-id="920af-187">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="920af-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="920af-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-189">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="920af-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="920af-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-191">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="920af-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="920af-192">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="920af-192">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="920af-193">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="920af-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="920af-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="920af-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="920af-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="920af-196">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="920af-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="920af-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="920af-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="920af-198">(1)</span><span class="sxs-lookup"><span data-stu-id="920af-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="920af-199">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="920af-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="920af-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="920af-201">(2)</span><span class="sxs-lookup"><span data-stu-id="920af-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="920af-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="920af-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="920af-203">(3)</span><span class="sxs-lookup"><span data-stu-id="920af-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="920af-204">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="920af-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="920af-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="920af-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="920af-206">(4)</span><span class="sxs-lookup"><span data-stu-id="920af-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="920af-207">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="920af-207">Device is not working properly.</span></span> <span data-ttu-id="920af-208">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="920af-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="920af-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="920af-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="920af-210">(5)</span><span class="sxs-lookup"><span data-stu-id="920af-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="920af-211">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="920af-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="920af-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="920af-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="920af-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="920af-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="920af-214">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="920af-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="920af-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="920af-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="920af-216">(7)</span><span class="sxs-lookup"><span data-stu-id="920af-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="920af-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="920af-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="920af-218">(8)</span><span class="sxs-lookup"><span data-stu-id="920af-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="920af-219">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="920af-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="920af-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="920af-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="920af-221">(9)</span><span class="sxs-lookup"><span data-stu-id="920af-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="920af-222">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="920af-222">Device is not working properly.</span></span> <span data-ttu-id="920af-223">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="920af-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="920af-225">(10)</span><span class="sxs-lookup"><span data-stu-id="920af-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="920af-226">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="920af-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="920af-228">(11)</span><span class="sxs-lookup"><span data-stu-id="920af-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="920af-229">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="920af-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="920af-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="920af-231">12</span><span class="sxs-lookup"><span data-stu-id="920af-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="920af-232">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="920af-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="920af-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="920af-234">(13)</span><span class="sxs-lookup"><span data-stu-id="920af-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="920af-235">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="920af-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="920af-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="920af-237">(14)</span><span class="sxs-lookup"><span data-stu-id="920af-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="920af-238">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="920af-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="920af-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="920af-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="920af-240">(15)</span><span class="sxs-lookup"><span data-stu-id="920af-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="920af-241">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="920af-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="920af-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="920af-243">(16)</span><span class="sxs-lookup"><span data-stu-id="920af-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="920af-244">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="920af-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="920af-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="920af-246">(17)</span><span class="sxs-lookup"><span data-stu-id="920af-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="920af-247">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="920af-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="920af-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="920af-249">(18)</span><span class="sxs-lookup"><span data-stu-id="920af-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="920af-250">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="920af-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="920af-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="920af-252">(19)</span><span class="sxs-lookup"><span data-stu-id="920af-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="920af-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="920af-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="920af-254">(20)</span><span class="sxs-lookup"><span data-stu-id="920af-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="920af-255">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="920af-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="920af-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="920af-257">(21)</span><span class="sxs-lookup"><span data-stu-id="920af-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="920af-258">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="920af-258">System failure.</span></span> <span data-ttu-id="920af-259">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="920af-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="920af-260">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="920af-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="920af-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="920af-262">(22)</span><span class="sxs-lookup"><span data-stu-id="920af-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="920af-263">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="920af-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="920af-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="920af-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="920af-265">(23)</span><span class="sxs-lookup"><span data-stu-id="920af-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="920af-266">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="920af-266">System failure.</span></span> <span data-ttu-id="920af-267">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="920af-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="920af-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="920af-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="920af-269">(24)</span><span class="sxs-lookup"><span data-stu-id="920af-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="920af-270">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="920af-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="920af-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="920af-272">(25)</span><span class="sxs-lookup"><span data-stu-id="920af-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="920af-273">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="920af-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="920af-275">(26)</span><span class="sxs-lookup"><span data-stu-id="920af-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="920af-276">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="920af-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="920af-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="920af-278">(27)</span><span class="sxs-lookup"><span data-stu-id="920af-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="920af-279">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="920af-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="920af-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="920af-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="920af-281">(28)</span><span class="sxs-lookup"><span data-stu-id="920af-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="920af-282">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="920af-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="920af-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="920af-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="920af-284">(29)</span><span class="sxs-lookup"><span data-stu-id="920af-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="920af-285">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="920af-285">Device is disabled.</span></span> <span data-ttu-id="920af-286">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="920af-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="920af-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="920af-288">(30)</span><span class="sxs-lookup"><span data-stu-id="920af-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="920af-289">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="920af-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="920af-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="920af-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="920af-291">31</span><span class="sxs-lookup"><span data-stu-id="920af-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="920af-292">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="920af-292">Device is not working properly.</span></span> <span data-ttu-id="920af-293">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="920af-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="920af-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="920af-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-295">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="920af-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="920af-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-297">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="920af-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="920af-298">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="920af-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="920af-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="920af-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-303">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="920af-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="920af-304">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="920af-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="920af-305">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="920af-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="920af-306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-307">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="920af-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-310">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="920af-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="920af-311">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="920af-311">Textual description of the object.</span></span>

<span data-ttu-id="920af-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="920af-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="920af-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-316">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="920af-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="920af-317">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="920af-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="920af-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="920af-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-320">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="920af-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="920af-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-322">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="920af-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="920af-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="920af-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-327">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="920af-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="920af-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="920af-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-332">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="920af-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="920af-333">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="920af-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="920af-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-335">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="920af-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="920af-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-337">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="920af-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="920af-338">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="920af-338">Date and time the object was installed.</span></span> <span data-ttu-id="920af-339">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="920af-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="920af-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="920af-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="920af-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-342">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="920af-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="920af-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-344">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="920af-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="920af-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-346">**Nome**</span><span class="sxs-lookup"><span data-stu-id="920af-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-349">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="920af-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="920af-350">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="920af-350">Label by which the object is known.</span></span> <span data-ttu-id="920af-351">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="920af-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="920af-352">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="920af-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="920af-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-354">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="920af-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="920af-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-356">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="920af-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="920af-357">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="920af-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="920af-358">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="920af-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="920af-359">Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="920af-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="920af-360">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="920af-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="920af-361">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="920af-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="920af-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="920af-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-363">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-365">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="920af-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="920af-366">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="920af-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="920af-367">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="920af-368">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="920af-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="920af-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="920af-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-370">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="920af-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="920af-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-372">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="920af-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="920af-373">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="920af-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="920af-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="920af-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="920af-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="920af-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="920af-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="920af-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="920af-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="920af-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="920af-378">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="920af-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="920af-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="920af-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="920af-380">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="920af-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="920af-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="920af-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="920af-382">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="920af-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="920af-383">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="920af-383">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="920af-384">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="920af-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="920af-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="920af-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="920af-386">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="920af-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="920af-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="920af-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="920af-388">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="920af-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="920af-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="920af-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-390">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="920af-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="920af-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-392">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="920af-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="920af-393">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="920af-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="920af-394">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="920af-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="920af-395">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="920af-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="920af-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-397">**PSExtentInterleaveDepth**</span><span class="sxs-lookup"><span data-stu-id="920af-397">**PSExtentInterleaveDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-398">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="920af-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="920af-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-400">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Set di volumi DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="920af-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="920af-401">Numero di extent dello spazio protetto a cui eseguire lo striping come set collettivo.</span><span class="sxs-lookup"><span data-stu-id="920af-401">Number of protected space extents to stripe as a collective set.</span></span> <span data-ttu-id="920af-402">In SCC, questo valore viene definito come il numero di strip da contare prima di continuare a eseguire il mapping al successivo set contiguo di extent, oltre lo stripe corrente.</span><span class="sxs-lookup"><span data-stu-id="920af-402">In SCC, this value is defined as the number of stripes to count before continuing to map into the next contiguous set of extents, beyond the current stripe.</span></span>

<span data-ttu-id="920af-403">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="920af-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="920af-404">**PSExtentStripeLength**</span><span class="sxs-lookup"><span data-stu-id="920af-404">**PSExtentStripeLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-405">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="920af-405">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="920af-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-407">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Set di volumi DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="920af-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="920af-408">Numero di extent dello spazio protetto contigui conteggiati prima di eseguire il loop fino al primo extent dello spazio protetto della striscia corrente.</span><span class="sxs-lookup"><span data-stu-id="920af-408">Number of contiguous protected space extents counted before looping back to the first protected space extent of the current stripe.</span></span> <span data-ttu-id="920af-409">Si tratta del numero di extent che formano il stripe di dati utente.</span><span class="sxs-lookup"><span data-stu-id="920af-409">It is the number of extents forming the user data stripe.</span></span>

<span data-ttu-id="920af-410">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="920af-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="920af-411">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="920af-411">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="920af-414">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="920af-414">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="920af-415">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="920af-415">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-416">**Status**</span><span class="sxs-lookup"><span data-stu-id="920af-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-417">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-419">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="920af-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="920af-420">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="920af-420">Current status of the object.</span></span> <span data-ttu-id="920af-421">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="920af-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="920af-422">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="920af-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="920af-423">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="920af-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="920af-424">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="920af-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="920af-425">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="920af-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="920af-426">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="920af-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="920af-427">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="920af-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="920af-428">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="920af-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="920af-429">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="920af-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="920af-430">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="920af-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="920af-431">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="920af-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="920af-432">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="920af-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="920af-433">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="920af-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="920af-434">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="920af-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="920af-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="920af-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-436">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="920af-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="920af-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-438">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="920af-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="920af-439">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="920af-439">State of the logical device.</span></span> <span data-ttu-id="920af-440">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="920af-440">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="920af-441">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="920af-442">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="920af-442">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="920af-443">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="920af-443">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="920af-444">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="920af-444">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="920af-445">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="920af-445">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="920af-446">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="920af-446">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="920af-447">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="920af-447">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-450">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="920af-450">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="920af-451">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="920af-451">Scoping system's creation class name.</span></span>

<span data-ttu-id="920af-452">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="920af-453">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="920af-453">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="920af-454">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="920af-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="920af-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="920af-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="920af-456">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="920af-456">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="920af-457">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="920af-457">Scoping system's name.</span></span>

<span data-ttu-id="920af-458">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="920af-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="920af-459">Commenti</span><span class="sxs-lookup"><span data-stu-id="920af-459">Remarks</span></span>

<span data-ttu-id="920af-460">La classe **CIM del \_ volume** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="920af-460">The **CIM\_VolumeSet** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="920af-461">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="920af-461">WMI does not implement this class.</span></span>

<span data-ttu-id="920af-462">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="920af-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="920af-463">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="920af-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="920af-464">Requisiti</span><span class="sxs-lookup"><span data-stu-id="920af-464">Requirements</span></span>



| <span data-ttu-id="920af-465">Requisito</span><span class="sxs-lookup"><span data-stu-id="920af-465">Requirement</span></span> | <span data-ttu-id="920af-466">Valore</span><span class="sxs-lookup"><span data-stu-id="920af-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="920af-467">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="920af-467">Minimum supported client</span></span><br/> | <span data-ttu-id="920af-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="920af-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="920af-469">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="920af-469">Minimum supported server</span></span><br/> | <span data-ttu-id="920af-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="920af-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="920af-471">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="920af-471">Namespace</span></span><br/>                | <span data-ttu-id="920af-472">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="920af-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="920af-473">MOF</span><span class="sxs-lookup"><span data-stu-id="920af-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="920af-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="920af-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="920af-475">DLL</span><span class="sxs-lookup"><span data-stu-id="920af-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="920af-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="920af-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="920af-477">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="920af-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="920af-478">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="920af-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 


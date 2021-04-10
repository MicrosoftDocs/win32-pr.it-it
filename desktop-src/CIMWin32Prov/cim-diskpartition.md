---
description: La \_ classe CIM DiskPartition rappresenta un intervallo contiguo di blocchi logici identificabili dal sistema operativo mediante i campi tipo e sottotipo della partizione.
ms.assetid: 22a0e5be-c66b-40a2-9a7a-047d2edc0278
ms.tgt_platform: multiple
title: Classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition
- CIM_DiskPartition.Access
- CIM_DiskPartition.Availability
- CIM_DiskPartition.BlockSize
- CIM_DiskPartition.Bootable
- CIM_DiskPartition.Caption
- CIM_DiskPartition.ConfigManagerErrorCode
- CIM_DiskPartition.ConfigManagerUserConfig
- CIM_DiskPartition.CreationClassName
- CIM_DiskPartition.Description
- CIM_DiskPartition.DeviceID
- CIM_DiskPartition.ErrorCleared
- CIM_DiskPartition.ErrorDescription
- CIM_DiskPartition.ErrorMethodology
- CIM_DiskPartition.InstallDate
- CIM_DiskPartition.LastErrorCode
- CIM_DiskPartition.Name
- CIM_DiskPartition.NumberOfBlocks
- CIM_DiskPartition.PNPDeviceID
- CIM_DiskPartition.PowerManagementCapabilities
- CIM_DiskPartition.PowerManagementSupported
- CIM_DiskPartition.PrimaryPartition
- CIM_DiskPartition.Purpose
- CIM_DiskPartition.Status
- CIM_DiskPartition.StatusInfo
- CIM_DiskPartition.SystemCreationClassName
- CIM_DiskPartition.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d1761e140813c26e67594872df5a8d2f7361768b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878041"
---
# <a name="cim_diskpartition-class"></a><span data-ttu-id="a1323-103">CIM \_ DiskPartition (classe)</span><span class="sxs-lookup"><span data-stu-id="a1323-103">CIM\_DiskPartition class</span></span>

<span data-ttu-id="a1323-104">La classe **CIM \_ DiskPartition** rappresenta un intervallo contiguo di blocchi logici identificabili dal sistema operativo mediante i campi tipo e sottotipo della partizione.</span><span class="sxs-lookup"><span data-stu-id="a1323-104">The **CIM\_DiskPartition** class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="a1323-105">Le partizioni disco devono essere realizzate direttamente da supporti fisici (indicati dall'associazione [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) ) o basate su volumi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1323-105">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1323-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a1323-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a1323-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a1323-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a1323-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a1323-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a1323-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a1323-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1323-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1323-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C541-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskPartition : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  boolean  Bootable;
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
  boolean  PrimaryPartition;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a1323-111">Members</span><span class="sxs-lookup"><span data-stu-id="a1323-111">Members</span></span>

<span data-ttu-id="a1323-112">La classe **CIM \_ DiskPartition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a1323-112">The **CIM\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="a1323-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a1323-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a1323-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a1323-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a1323-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="a1323-115">Methods</span></span>

<span data-ttu-id="a1323-116">La classe **CIM \_ DiskPartition** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a1323-116">The **CIM\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="a1323-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="a1323-117">Method</span></span>                                                                   | <span data-ttu-id="a1323-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1323-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1323-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a1323-119">**Reset**</span></span>](reset-method-in-class-cim-diskpartition.md)                 | <span data-ttu-id="a1323-120">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1323-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="a1323-121">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a1323-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a1323-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a1323-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-diskpartition.md) | <span data-ttu-id="a1323-123">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="a1323-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a1323-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a1323-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a1323-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a1323-125">Properties</span></span>

<span data-ttu-id="a1323-126">La classe **CIM \_ DiskPartition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a1323-126">The **CIM\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1323-127">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="a1323-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1323-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-130">Specifica se i supporti sono leggibili, scrivibili o entrambi, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="a1323-130">Specifies whether the media is readable, writeable, or both, for example.</span></span> <span data-ttu-id="a1323-131">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1323-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a1323-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-133">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a1323-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="a1323-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="a1323-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-135">Leggibile.</span><span class="sxs-lookup"><span data-stu-id="a1323-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="a1323-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="a1323-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-137">Scrivibile.</span><span class="sxs-lookup"><span data-stu-id="a1323-137">Writeable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="a1323-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="a1323-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-139">Lettura/scrittura supportata.</span><span class="sxs-lookup"><span data-stu-id="a1323-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="a1323-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="a1323-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-141">Scrivere una sola volta.</span><span class="sxs-lookup"><span data-stu-id="a1323-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1323-142">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="a1323-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1323-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-145">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a1323-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-146">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-146">Availability and status of the device.</span></span>

<span data-ttu-id="a1323-147">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a1323-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a1323-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1323-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a1323-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a1323-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a1323-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a1323-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a1323-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a1323-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="a1323-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a1323-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="a1323-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a1323-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="a1323-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a1323-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="a1323-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a1323-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a1323-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a1323-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="a1323-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a1323-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="a1323-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a1323-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="a1323-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a1323-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="a1323-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-161">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a1323-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a1323-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="a1323-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-163">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="a1323-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a1323-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a1323-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-165">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a1323-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a1323-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="a1323-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a1323-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a1323-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-168">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a1323-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a1323-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a1323-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-170">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="a1323-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a1323-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a1323-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-172">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="a1323-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a1323-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="a1323-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-174">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="a1323-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a1323-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a1323-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-176">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="a1323-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1323-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="a1323-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-178">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1323-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-180">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="a1323-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-181">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1323-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="a1323-182">Se si tratta di una dimensione di blocco variabile, è necessario specificare la dimensione massima del blocco, in byte.</span><span class="sxs-lookup"><span data-stu-id="a1323-182">If it is a variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="a1323-183">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere il valore 1.</span><span class="sxs-lookup"><span data-stu-id="a1323-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter the value 1.</span></span>

<span data-ttu-id="a1323-184">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="a1323-185">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a1323-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-186">**Avviabile**</span><span class="sxs-lookup"><span data-stu-id="a1323-186">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-187">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1323-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-189">Se **true**, la partizione del disco viene etichettata come avviabile.</span><span class="sxs-lookup"><span data-stu-id="a1323-189">If **TRUE**, the disk partition is labeled as bootable.</span></span> <span data-ttu-id="a1323-190">Ciò non significa che un sistema operativo sia caricato nella partizione.</span><span class="sxs-lookup"><span data-stu-id="a1323-190">This does not mean that an operating system is loaded on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="a1323-191">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a1323-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-194">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a1323-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-195">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1323-195">Short textual description of the object.</span></span>

<span data-ttu-id="a1323-196">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-197">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a1323-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-198">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1323-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-200">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a1323-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-201">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a1323-201">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="a1323-202">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a1323-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a1323-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a1323-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="a1323-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-205">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a1323-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a1323-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="a1323-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a1323-207">(1)</span><span class="sxs-lookup"><span data-stu-id="a1323-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-208">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="a1323-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a1323-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a1323-210">(2)</span><span class="sxs-lookup"><span data-stu-id="a1323-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a1323-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="a1323-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a1323-212">(3)</span><span class="sxs-lookup"><span data-stu-id="a1323-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-213">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="a1323-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a1323-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a1323-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a1323-215">(4)</span><span class="sxs-lookup"><span data-stu-id="a1323-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-216">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="a1323-216">Device is not working properly.</span></span> <span data-ttu-id="a1323-217">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="a1323-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a1323-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="a1323-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a1323-219">(5)</span><span class="sxs-lookup"><span data-stu-id="a1323-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-220">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="a1323-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a1323-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="a1323-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a1323-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="a1323-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-223">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a1323-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a1323-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="a1323-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a1323-225">(7)</span><span class="sxs-lookup"><span data-stu-id="a1323-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a1323-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="a1323-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a1323-227">(8)</span><span class="sxs-lookup"><span data-stu-id="a1323-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-228">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="a1323-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a1323-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="a1323-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a1323-230">(9)</span><span class="sxs-lookup"><span data-stu-id="a1323-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-231">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-231">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a1323-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a1323-233">(10)</span><span class="sxs-lookup"><span data-stu-id="a1323-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-234">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a1323-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a1323-236">(11)</span><span class="sxs-lookup"><span data-stu-id="a1323-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-237">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a1323-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="a1323-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a1323-239">12</span><span class="sxs-lookup"><span data-stu-id="a1323-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-240">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="a1323-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a1323-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a1323-242">(13)</span><span class="sxs-lookup"><span data-stu-id="a1323-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-243">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a1323-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="a1323-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a1323-245">(14)</span><span class="sxs-lookup"><span data-stu-id="a1323-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-246">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="a1323-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a1323-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="a1323-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a1323-248">(15)</span><span class="sxs-lookup"><span data-stu-id="a1323-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-249">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="a1323-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a1323-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a1323-251">(16)</span><span class="sxs-lookup"><span data-stu-id="a1323-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-252">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a1323-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="a1323-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a1323-254">(17)</span><span class="sxs-lookup"><span data-stu-id="a1323-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-255">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a1323-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a1323-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a1323-257">(18)</span><span class="sxs-lookup"><span data-stu-id="a1323-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-258">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a1323-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="a1323-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a1323-260">(19)</span><span class="sxs-lookup"><span data-stu-id="a1323-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a1323-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="a1323-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a1323-262">(20)</span><span class="sxs-lookup"><span data-stu-id="a1323-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-263">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="a1323-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a1323-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a1323-265">(21)</span><span class="sxs-lookup"><span data-stu-id="a1323-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-266">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="a1323-266">System failure.</span></span> <span data-ttu-id="a1323-267">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a1323-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a1323-268">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a1323-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="a1323-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a1323-270">(22)</span><span class="sxs-lookup"><span data-stu-id="a1323-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-271">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a1323-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a1323-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="a1323-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a1323-273">(23)</span><span class="sxs-lookup"><span data-stu-id="a1323-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-274">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="a1323-274">System failure.</span></span> <span data-ttu-id="a1323-275">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a1323-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a1323-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="a1323-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a1323-277">(24)</span><span class="sxs-lookup"><span data-stu-id="a1323-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-278">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="a1323-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a1323-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a1323-280">(25)</span><span class="sxs-lookup"><span data-stu-id="a1323-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-281">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a1323-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a1323-283">(26)</span><span class="sxs-lookup"><span data-stu-id="a1323-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-284">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a1323-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="a1323-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a1323-286">(27)</span><span class="sxs-lookup"><span data-stu-id="a1323-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-287">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="a1323-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a1323-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="a1323-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a1323-289">(28)</span><span class="sxs-lookup"><span data-stu-id="a1323-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-290">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="a1323-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a1323-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="a1323-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a1323-292">(29)</span><span class="sxs-lookup"><span data-stu-id="a1323-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-293">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="a1323-293">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a1323-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a1323-295">(30)</span><span class="sxs-lookup"><span data-stu-id="a1323-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-296">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1323-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a1323-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a1323-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a1323-298">31</span><span class="sxs-lookup"><span data-stu-id="a1323-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-299">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="a1323-299">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1323-300">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a1323-300">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-301">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1323-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-303">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a1323-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-304">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a1323-304">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a1323-305">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-306">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1323-306">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-309">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a1323-309">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a1323-310">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a1323-310">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a1323-311">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a1323-311">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a1323-312">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-313">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a1323-313">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-316">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a1323-316">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-317">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1323-317">Textual description of the object.</span></span>

<span data-ttu-id="a1323-318">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-319">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a1323-319">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-322">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a1323-322">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a1323-323">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1323-323">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a1323-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a1323-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-326">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1323-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-328">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="a1323-328">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a1323-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a1323-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-333">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="a1323-333">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a1323-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-335">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="a1323-335">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-338">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1323-338">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="a1323-339">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-339">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-340">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a1323-340">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-341">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1323-341">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-343">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a1323-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-344">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1323-344">Date and time the object was installed.</span></span> <span data-ttu-id="a1323-345">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="a1323-345">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a1323-346">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a1323-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-348">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1323-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-350">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1323-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a1323-351">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-352">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a1323-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-355">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a1323-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-356">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a1323-356">Label by which the object is known.</span></span> <span data-ttu-id="a1323-357">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a1323-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a1323-358">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-359">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="a1323-359">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-360">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1323-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-362">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="a1323-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-363">Numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1323-363">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="a1323-364">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a1323-364">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="a1323-365">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1323-365">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="a1323-366">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-366">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="a1323-367">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a1323-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-368">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a1323-368">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-369">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-371">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a1323-371">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-372">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1323-372">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="a1323-373">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a1323-374">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a1323-374">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a1323-375">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a1323-375">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-376">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1323-376">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1323-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-378">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1323-378">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a1323-379">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="a1323-379">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1323-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a1323-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a1323-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a1323-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a1323-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="a1323-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a1323-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a1323-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-384">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="a1323-384">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a1323-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a1323-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-386">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="a1323-386">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a1323-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a1323-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-388">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="a1323-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a1323-389">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="a1323-389">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a1323-390">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a1323-390">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a1323-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="a1323-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-392">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="a1323-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a1323-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="a1323-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a1323-394">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="a1323-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1323-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a1323-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-396">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1323-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-398">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="a1323-398">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a1323-399">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a1323-399">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a1323-400">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a1323-400">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a1323-401">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a1323-401">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="a1323-402">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-403">**Partizione primaria**</span><span class="sxs-lookup"><span data-stu-id="a1323-403">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-404">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1323-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-406">Se **true**, la partizione del disco viene etichettata come partizione primaria per un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="a1323-406">If **TRUE**, the disk partition is labeled as the primary partition for a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a1323-407">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="a1323-407">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-408">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1323-410">Descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a1323-410">Describes the media and its use.</span></span>

<span data-ttu-id="a1323-411">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-411">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-412">**Status**</span><span class="sxs-lookup"><span data-stu-id="a1323-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-413">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-415">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a1323-415">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-416">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1323-416">Current status of the object.</span></span>

<span data-ttu-id="a1323-417">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-417">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a1323-418">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1323-418">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a1323-419">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a1323-419">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a1323-420">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a1323-420">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a1323-421">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a1323-421">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1323-422">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a1323-422">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a1323-423">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a1323-423">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a1323-424">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a1323-424">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a1323-425">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a1323-425">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a1323-426">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a1323-426">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a1323-427">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a1323-427">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a1323-428">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a1323-428">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a1323-429">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a1323-429">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a1323-430">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a1323-430">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1323-431">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a1323-431">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-432">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1323-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-433">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-434">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a1323-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a1323-435">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a1323-435">State of the logical device.</span></span> <span data-ttu-id="a1323-436">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="a1323-436">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a1323-437">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a1323-438">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a1323-438">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1323-439">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a1323-439">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a1323-440">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a1323-440">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a1323-441">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="a1323-441">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a1323-442">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="a1323-442">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1323-443">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1323-443">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-444">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-446">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a1323-446">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a1323-447">Proprietà **CreationClassName** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a1323-447">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="a1323-448">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1323-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a1323-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1323-450">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a1323-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1323-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a1323-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1323-452">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a1323-452">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a1323-453">Proprietà **Name** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a1323-453">Scoping system's **Name** property.</span></span>

<span data-ttu-id="a1323-454">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1323-455">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1323-455">Remarks</span></span>

<span data-ttu-id="a1323-456">La classe **CIM \_ DiskPartition** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-456">The **CIM\_DiskPartition** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="a1323-457">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a1323-457">WMI does not implement this class.</span></span> <span data-ttu-id="a1323-458">Per le classi derivate da **CIM \_ DiskPartition**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-458">For classes derived from **CIM\_DiskPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a1323-459">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a1323-459">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a1323-460">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a1323-460">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1323-461">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1323-461">Requirements</span></span>



| <span data-ttu-id="a1323-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1323-462">Requirement</span></span> | <span data-ttu-id="a1323-463">Valore</span><span class="sxs-lookup"><span data-stu-id="a1323-463">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1323-464">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1323-464">Minimum supported client</span></span><br/> | <span data-ttu-id="a1323-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1323-465">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1323-466">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1323-466">Minimum supported server</span></span><br/> | <span data-ttu-id="a1323-467">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1323-467">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1323-468">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a1323-468">Namespace</span></span><br/>                | <span data-ttu-id="a1323-469">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a1323-469">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1323-470">MOF</span><span class="sxs-lookup"><span data-stu-id="a1323-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1323-471"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1323-471"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1323-472">DLL</span><span class="sxs-lookup"><span data-stu-id="a1323-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1323-473"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1323-473"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1323-474">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1323-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1323-475">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a1323-475">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 


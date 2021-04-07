---
description: La \_ classe CIM disco logico rappresenta un intervallo contiguo di blocchi logici identificabili da un file System tramite il campo DeviceID (Key) del disco.
ms.assetid: 1c2fd0bf-a1e3-4706-9f84-5dd4d371a167
ms.tgt_platform: multiple
title: Classe CIM_LogicalDisk (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.Access
- CIM_LogicalDisk.Availability
- CIM_LogicalDisk.BlockSize
- CIM_LogicalDisk.Caption
- CIM_LogicalDisk.ConfigManagerErrorCode
- CIM_LogicalDisk.ConfigManagerUserConfig
- CIM_LogicalDisk.CreationClassName
- CIM_LogicalDisk.Description
- CIM_LogicalDisk.DeviceID
- CIM_LogicalDisk.ErrorCleared
- CIM_LogicalDisk.ErrorDescription
- CIM_LogicalDisk.ErrorMethodology
- CIM_LogicalDisk.FreeSpace
- CIM_LogicalDisk.InstallDate
- CIM_LogicalDisk.LastErrorCode
- CIM_LogicalDisk.Name
- CIM_LogicalDisk.NumberOfBlocks
- CIM_LogicalDisk.PNPDeviceID
- CIM_LogicalDisk.PowerManagementCapabilities
- CIM_LogicalDisk.PowerManagementSupported
- CIM_LogicalDisk.Purpose
- CIM_LogicalDisk.Size
- CIM_LogicalDisk.Status
- CIM_LogicalDisk.StatusInfo
- CIM_LogicalDisk.SystemCreationClassName
- CIM_LogicalDisk.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd28ab0b9982606278e65705273a9965cfb9b396
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747959"
---
# <a name="cim_logicaldisk-class-cimwin32-wmi-providers"></a><span data-ttu-id="797b7-103">Classe CIM_LogicalDisk (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="797b7-103">CIM_LogicalDisk class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="797b7-104">La classe **CIM \_ disco logico** rappresenta un intervallo contiguo di blocchi logici identificabili da un file System tramite il campo **DeviceID** (Key) del disco.</span><span class="sxs-lookup"><span data-stu-id="797b7-104">The **CIM\_LogicalDisk** class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="797b7-105">Ad esempio, in un ambiente Windows, il campo **DeviceID** contiene una lettera di unità; in un ambiente UNIX, contiene il percorso di accesso; e in un ambiente NetWare contiene il nome del volume.</span><span class="sxs-lookup"><span data-stu-id="797b7-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="797b7-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="797b7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="797b7-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="797b7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="797b7-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="797b7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="797b7-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="797b7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="797b7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="797b7-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C539-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
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
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="797b7-111">Members</span><span class="sxs-lookup"><span data-stu-id="797b7-111">Members</span></span>

<span data-ttu-id="797b7-112">La classe **CIM \_ disco logico** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="797b7-112">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="797b7-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="797b7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="797b7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="797b7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="797b7-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="797b7-115">Methods</span></span>

<span data-ttu-id="797b7-116">La classe **CIM \_ disco logico** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="797b7-116">The **CIM\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="797b7-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="797b7-117">Method</span></span>                                                                 | <span data-ttu-id="797b7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="797b7-118">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="797b7-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="797b7-119">**Reset**</span></span>](reset-method-in-class-cim-logicaldisk.md)                 | <span data-ttu-id="797b7-120">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="797b7-121">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="797b7-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="797b7-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="797b7-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldisk.md) | <span data-ttu-id="797b7-123">Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="797b7-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="797b7-124">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="797b7-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="797b7-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="797b7-125">Properties</span></span>

<span data-ttu-id="797b7-126">La classe **CIM \_ disco logico** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="797b7-126">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="797b7-127">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="797b7-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="797b7-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-130">Descrive se i supporti sono leggibili, scrivibili o entrambi, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="797b7-130">Describes whether the media is readable, writable, or both, for example.</span></span> <span data-ttu-id="797b7-131">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="797b7-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="797b7-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-133">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="797b7-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="797b7-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="797b7-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-135">Leggibile.</span><span class="sxs-lookup"><span data-stu-id="797b7-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="797b7-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="797b7-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-137">Scrivibile.</span><span class="sxs-lookup"><span data-stu-id="797b7-137">Writable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="797b7-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="797b7-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-139">Lettura/scrittura supportata.</span><span class="sxs-lookup"><span data-stu-id="797b7-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="797b7-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="797b7-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-141">Scrivere una sola volta.</span><span class="sxs-lookup"><span data-stu-id="797b7-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="797b7-142">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="797b7-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="797b7-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-145">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="797b7-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-146">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-146">Availability and status of the device.</span></span>

<span data-ttu-id="797b7-147">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="797b7-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="797b7-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="797b7-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="797b7-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="797b7-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="797b7-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="797b7-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="797b7-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="797b7-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="797b7-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="797b7-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="797b7-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="797b7-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="797b7-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="797b7-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="797b7-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="797b7-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="797b7-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="797b7-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="797b7-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="797b7-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="797b7-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="797b7-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="797b7-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="797b7-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="797b7-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-161">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="797b7-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="797b7-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="797b7-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-163">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="797b7-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="797b7-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="797b7-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-165">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="797b7-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="797b7-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="797b7-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="797b7-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="797b7-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-168">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="797b7-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="797b7-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="797b7-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-170">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="797b7-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="797b7-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="797b7-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-172">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="797b7-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="797b7-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="797b7-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-174">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="797b7-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="797b7-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="797b7-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-176">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="797b7-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="797b7-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="797b7-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-178">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="797b7-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-180">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="797b7-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-181">Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="797b7-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="797b7-182">Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="797b7-182">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="797b7-183">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1.</span><span class="sxs-lookup"><span data-stu-id="797b7-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="797b7-184">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="797b7-185">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="797b7-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-186">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="797b7-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-189">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="797b7-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-190">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="797b7-190">Short textual description of the object.</span></span>

<span data-ttu-id="797b7-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-192">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="797b7-192">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="797b7-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-195">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="797b7-195">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-196">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="797b7-196">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="797b7-197">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-197">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="797b7-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="797b7-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="797b7-199"> (0)</span><span class="sxs-lookup"><span data-stu-id="797b7-199">(0)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-200">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="797b7-200">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="797b7-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="797b7-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="797b7-202">(1)</span><span class="sxs-lookup"><span data-stu-id="797b7-202">(1)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-203">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="797b7-203">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="797b7-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="797b7-205">(2)</span><span class="sxs-lookup"><span data-stu-id="797b7-205">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="797b7-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="797b7-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="797b7-207">(3)</span><span class="sxs-lookup"><span data-stu-id="797b7-207">(3)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-208">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="797b7-208">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="797b7-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="797b7-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="797b7-210">(4)</span><span class="sxs-lookup"><span data-stu-id="797b7-210">(4)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-211">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="797b7-211">Device is not working properly.</span></span> <span data-ttu-id="797b7-212">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="797b7-212">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="797b7-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="797b7-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="797b7-214">(5)</span><span class="sxs-lookup"><span data-stu-id="797b7-214">(5)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-215">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="797b7-215">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="797b7-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="797b7-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="797b7-217"> (6)</span><span class="sxs-lookup"><span data-stu-id="797b7-217">(6)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-218">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="797b7-218">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="797b7-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="797b7-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="797b7-220">(7)</span><span class="sxs-lookup"><span data-stu-id="797b7-220">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="797b7-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="797b7-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="797b7-222">(8)</span><span class="sxs-lookup"><span data-stu-id="797b7-222">(8)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-223">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="797b7-223">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="797b7-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="797b7-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="797b7-225">(9)</span><span class="sxs-lookup"><span data-stu-id="797b7-225">(9)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-226">Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-226">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="797b7-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="797b7-228">(10)</span><span class="sxs-lookup"><span data-stu-id="797b7-228">(10)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-229">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-229">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="797b7-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="797b7-231">(11)</span><span class="sxs-lookup"><span data-stu-id="797b7-231">(11)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-232">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-232">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="797b7-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="797b7-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="797b7-234">12</span><span class="sxs-lookup"><span data-stu-id="797b7-234">(12)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-235">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="797b7-235">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="797b7-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="797b7-237">(13)</span><span class="sxs-lookup"><span data-stu-id="797b7-237">(13)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-238">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-238">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="797b7-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="797b7-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="797b7-240">(14)</span><span class="sxs-lookup"><span data-stu-id="797b7-240">(14)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-241">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="797b7-241">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="797b7-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="797b7-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="797b7-243">(15)</span><span class="sxs-lookup"><span data-stu-id="797b7-243">(15)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-244">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="797b7-244">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="797b7-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="797b7-246">(16)</span><span class="sxs-lookup"><span data-stu-id="797b7-246">(16)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-247">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-247">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="797b7-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="797b7-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="797b7-249">(17)</span><span class="sxs-lookup"><span data-stu-id="797b7-249">(17)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-250">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="797b7-250">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="797b7-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="797b7-252">(18)</span><span class="sxs-lookup"><span data-stu-id="797b7-252">(18)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-253">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-253">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="797b7-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="797b7-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="797b7-255">(19)</span><span class="sxs-lookup"><span data-stu-id="797b7-255">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="797b7-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="797b7-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="797b7-257">(20)</span><span class="sxs-lookup"><span data-stu-id="797b7-257">(20)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-258">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="797b7-258">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="797b7-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="797b7-260">(21)</span><span class="sxs-lookup"><span data-stu-id="797b7-260">(21)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-261">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="797b7-261">System failure.</span></span> <span data-ttu-id="797b7-262">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="797b7-262">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="797b7-263">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-263">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="797b7-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="797b7-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="797b7-265">(22)</span><span class="sxs-lookup"><span data-stu-id="797b7-265">(22)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-266">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="797b7-266">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="797b7-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="797b7-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="797b7-268">(23)</span><span class="sxs-lookup"><span data-stu-id="797b7-268">(23)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-269">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="797b7-269">System failure.</span></span> <span data-ttu-id="797b7-270">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="797b7-270">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="797b7-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="797b7-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="797b7-272">(24)</span><span class="sxs-lookup"><span data-stu-id="797b7-272">(24)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-273">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="797b7-273">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="797b7-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="797b7-275">(25)</span><span class="sxs-lookup"><span data-stu-id="797b7-275">(25)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-276">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="797b7-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="797b7-278">(26)</span><span class="sxs-lookup"><span data-stu-id="797b7-278">(26)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-279">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-279">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="797b7-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="797b7-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="797b7-281">(27)</span><span class="sxs-lookup"><span data-stu-id="797b7-281">(27)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-282">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="797b7-282">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="797b7-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="797b7-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="797b7-284">(28)</span><span class="sxs-lookup"><span data-stu-id="797b7-284">(28)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-285">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="797b7-285">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="797b7-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="797b7-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="797b7-287">(29)</span><span class="sxs-lookup"><span data-stu-id="797b7-287">(29)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-288">Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="797b7-288">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="797b7-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="797b7-290">(30)</span><span class="sxs-lookup"><span data-stu-id="797b7-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-291">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797b7-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="797b7-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="797b7-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="797b7-293">31</span><span class="sxs-lookup"><span data-stu-id="797b7-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-294">Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="797b7-294">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="797b7-295">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="797b7-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-296">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="797b7-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-298">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="797b7-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-299">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="797b7-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="797b7-300">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-301">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="797b7-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-304">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="797b7-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="797b7-305">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="797b7-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="797b7-306">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="797b7-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="797b7-307">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-308">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="797b7-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-311">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="797b7-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-312">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="797b7-312">Textual description of the object.</span></span>

<span data-ttu-id="797b7-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="797b7-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-317">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="797b7-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="797b7-318">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="797b7-319">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="797b7-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-321">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="797b7-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-323">Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="797b7-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="797b7-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="797b7-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-328">Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.</span><span class="sxs-lookup"><span data-stu-id="797b7-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="797b7-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-330">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="797b7-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-333">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="797b7-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="797b7-334">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-334">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-335">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="797b7-335">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-336">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="797b7-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-338">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="797b7-338">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-339">Spazio disponibile, in byte, sul disco logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-339">Available free space, in bytes, on the logical disk.</span></span>

<span data-ttu-id="797b7-340">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="797b7-340">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-341">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="797b7-341">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-342">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="797b7-342">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-344">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="797b7-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-345">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="797b7-345">Date and time the object was installed.</span></span> <span data-ttu-id="797b7-346">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="797b7-346">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="797b7-347">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-348">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="797b7-348">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-349">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="797b7-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-351">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-351">Last error code reported by the logical device.</span></span>

<span data-ttu-id="797b7-352">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-353">**Nome**</span><span class="sxs-lookup"><span data-stu-id="797b7-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-354">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-356">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="797b7-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-357">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="797b7-357">Label by which the object is known.</span></span> <span data-ttu-id="797b7-358">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="797b7-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="797b7-359">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-360">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="797b7-360">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-361">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="797b7-361">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-363">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="797b7-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-364">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="797b7-364">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form the storage extent.</span></span> <span data-ttu-id="797b7-365">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="797b7-365">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="797b7-366">Se il valore della proprietà **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="797b7-366">If the value of the **BlockSize** property is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="797b7-367">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-367">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="797b7-368">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="797b7-368">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-369">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="797b7-369">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-370">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-372">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="797b7-372">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-373">Win32 Plug and Play identificatore dispositivo del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-373">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="797b7-374">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="797b7-375">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="797b7-375">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="797b7-376">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="797b7-376">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-377">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="797b7-377">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="797b7-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-379">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-379">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="797b7-380">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="797b7-380">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="797b7-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="797b7-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="797b7-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="797b7-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="797b7-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="797b7-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="797b7-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="797b7-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-385">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="797b7-385">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="797b7-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="797b7-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-387">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="797b7-387">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="797b7-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="797b7-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-389">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="797b7-389">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="797b7-390">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="797b7-390">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="797b7-391">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="797b7-391">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="797b7-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="797b7-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-393">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="797b7-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="797b7-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="797b7-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="797b7-395">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="797b7-395">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="797b7-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="797b7-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-397">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="797b7-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-399">Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="797b7-399">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="797b7-400">Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="797b7-400">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="797b7-401">Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate.</span><span class="sxs-lookup"><span data-stu-id="797b7-401">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="797b7-402">Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="797b7-402">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="797b7-403">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-404">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="797b7-404">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-405">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-406">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="797b7-407">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="797b7-407">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="797b7-408">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-408">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-409">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="797b7-409">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-410">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="797b7-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-412">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="797b7-412">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-413">Dimensioni, in byte, del disco logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-413">Size of the logical disk, in bytes.</span></span>

<span data-ttu-id="797b7-414">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="797b7-414">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-415">**Status**</span><span class="sxs-lookup"><span data-stu-id="797b7-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-416">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-418">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="797b7-418">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-419">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="797b7-419">Current status of the object.</span></span>

<span data-ttu-id="797b7-420">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-420">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="797b7-421">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="797b7-421">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="797b7-422">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="797b7-422">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="797b7-423">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="797b7-423">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="797b7-424">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="797b7-424">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="797b7-425">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="797b7-425">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="797b7-426">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="797b7-426">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="797b7-427">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="797b7-427">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="797b7-428">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="797b7-428">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="797b7-429">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="797b7-429">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="797b7-430">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="797b7-430">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="797b7-431">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="797b7-431">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="797b7-432">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="797b7-432">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="797b7-433">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="797b7-433">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="797b7-434">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="797b7-434">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-435">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="797b7-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-437">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="797b7-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="797b7-438">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="797b7-438">State of the logical device.</span></span> <span data-ttu-id="797b7-439">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="797b7-439">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="797b7-440">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="797b7-441">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="797b7-441">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="797b7-442">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="797b7-442">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="797b7-443">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="797b7-443">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="797b7-444">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="797b7-444">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="797b7-445">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="797b7-445">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="797b7-446">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="797b7-446">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-447">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-449">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="797b7-449">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="797b7-450">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="797b7-450">Scoping system's creation class name.</span></span>

<span data-ttu-id="797b7-451">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="797b7-452">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="797b7-452">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b7-453">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="797b7-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="797b7-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="797b7-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b7-455">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="797b7-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="797b7-456">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="797b7-456">Scoping system's name.</span></span>

<span data-ttu-id="797b7-457">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="797b7-458">Commenti</span><span class="sxs-lookup"><span data-stu-id="797b7-458">Remarks</span></span>

<span data-ttu-id="797b7-459">La classe **CIM \_ disco logico** è derivata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-459">The **CIM\_LogicalDisk** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="797b7-460">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="797b7-460">WMI does not implement this class.</span></span> <span data-ttu-id="797b7-461">Per le classi derivate da **CIM \_ disco logico**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="797b7-461">For classes derived from **CIM\_LogicalDisk**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="797b7-462">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="797b7-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="797b7-463">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="797b7-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="797b7-464">Requisiti</span><span class="sxs-lookup"><span data-stu-id="797b7-464">Requirements</span></span>



| <span data-ttu-id="797b7-465">Requisito</span><span class="sxs-lookup"><span data-stu-id="797b7-465">Requirement</span></span> | <span data-ttu-id="797b7-466">Valore</span><span class="sxs-lookup"><span data-stu-id="797b7-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="797b7-467">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="797b7-467">Minimum supported client</span></span><br/> | <span data-ttu-id="797b7-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="797b7-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="797b7-469">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="797b7-469">Minimum supported server</span></span><br/> | <span data-ttu-id="797b7-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="797b7-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="797b7-471">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="797b7-471">Namespace</span></span><br/>                | <span data-ttu-id="797b7-472">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="797b7-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="797b7-473">MOF</span><span class="sxs-lookup"><span data-stu-id="797b7-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="797b7-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="797b7-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="797b7-475">DLL</span><span class="sxs-lookup"><span data-stu-id="797b7-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="797b7-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="797b7-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="797b7-477">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="797b7-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="797b7-478">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="797b7-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 


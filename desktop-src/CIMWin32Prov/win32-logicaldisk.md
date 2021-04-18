---
description: Rappresenta un'origine dati che viene risolta in un dispositivo di archiviazione locale effettivo in un computer in cui è in esecuzione Windows.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304474"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="ee00e-103">Win32 \_ disco logico (classe)</span><span class="sxs-lookup"><span data-stu-id="ee00e-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="ee00e-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ disco logico di Win32** rappresenta un'origine dati che viene risolta in un dispositivo di archiviazione locale effettivo in un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="ee00e-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="ee00e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ee00e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ee00e-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ee00e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee00e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee00e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="ee00e-108">Members</span><span class="sxs-lookup"><span data-stu-id="ee00e-108">Members</span></span>

<span data-ttu-id="ee00e-109">La classe **Win32 \_ disco logico** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee00e-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="ee00e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee00e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee00e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee00e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee00e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee00e-112">Methods</span></span>

<span data-ttu-id="ee00e-113">La classe **Win32 \_ disco logico** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ee00e-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="ee00e-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee00e-114">Method</span></span>                                                                             | <span data-ttu-id="ee00e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee00e-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee00e-116">**CHKDSK**</span><span class="sxs-lookup"><span data-stu-id="ee00e-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="ee00e-117">Richiama l'operazione [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) sul disco.</span><span class="sxs-lookup"><span data-stu-id="ee00e-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ee00e-118">**ExcludeFromAutochk**</span><span class="sxs-lookup"><span data-stu-id="ee00e-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="ee00e-119">Esclude i dischi dall'operazione [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) da eseguire al riavvio successivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="ee00e-120">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="ee00e-120">**Reset**</span></span>                                                                          | <span data-ttu-id="ee00e-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-121">Not implemented.</span></span> <span data-ttu-id="ee00e-122">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ disco logico**](cim-logicaldisk.md) per la documentazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="ee00e-123">**ScheduleAutoChk**</span><span class="sxs-lookup"><span data-stu-id="ee00e-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="ee00e-124">Pianifica l'esecuzione di [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) al riavvio successivo se è stato impostato il bit modificato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="ee00e-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ee00e-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="ee00e-126">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-126">Not implemented.</span></span> <span data-ttu-id="ee00e-127">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ disco logico**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="ee00e-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee00e-128">Properties</span></span>

<span data-ttu-id="ee00e-129">La classe **Win32 \_ disco logico** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee00e-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee00e-130">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="ee00e-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee00e-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-133">Tipo di accesso ai supporti disponibile.</span><span class="sxs-lookup"><span data-stu-id="ee00e-133">Type of media access available.</span></span>

<span data-ttu-id="ee00e-134">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00e-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ee00e-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="ee00e-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="ee00e-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-138">Scrivibile</span><span class="sxs-lookup"><span data-stu-id="ee00e-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="ee00e-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="ee00e-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-141">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="ee00e-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee00e-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="ee00e-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-145">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-145">Availability and status of the device.</span></span>

<span data-ttu-id="ee00e-146">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee00e-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00e-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ee00e-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-150">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="ee00e-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ee00e-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ee00e-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="ee00e-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ee00e-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="ee00e-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ee00e-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="ee00e-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ee00e-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="ee00e-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-156">Offline</span><span class="sxs-lookup"><span data-stu-id="ee00e-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ee00e-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ee00e-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ee00e-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="ee00e-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ee00e-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="ee00e-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ee00e-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="ee00e-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ee00e-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="ee00e-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-162">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ee00e-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="ee00e-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-164">Il dispositivo è in uno stato di risparmio energia, ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="ee00e-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ee00e-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ee00e-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-166">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ee00e-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="ee00e-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ee00e-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="ee00e-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-169">Il dispositivo è in uno stato di avviso, ma anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="ee00e-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ee00e-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="ee00e-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-171">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="ee00e-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ee00e-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="ee00e-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-173">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ee00e-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="ee00e-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-175">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ee00e-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="ee00e-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-177">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="ee00e-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="ee00e-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-179">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee00e-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-181">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="ee00e-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-182">Dimensioni, in byte, dei blocchi che formano questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="ee00e-183">Se è sconosciuto o se un concetto di blocco non è valido (ad esempio per extent di aggregazione, memoria o dischi logici), immettere 1.</span><span class="sxs-lookup"><span data-stu-id="ee00e-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="ee00e-184">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="ee00e-185">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ee00e-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-186">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ee00e-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-189">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ee00e-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-190">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="ee00e-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="ee00e-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-192">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="ee00e-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-193">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-195">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ vol \_ is \_ compresso")</span><span class="sxs-lookup"><span data-stu-id="ee00e-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-196">Se **true**, il volume logico esiste come una singola entità compressa, ad esempio un volume DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="ee00e-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="ee00e-197">Se è supportata la compressione basata su file, ad esempio in NTFS, questa proprietà è **false**.</span><span class="sxs-lookup"><span data-stu-id="ee00e-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-198">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ee00e-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-199">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee00e-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-201">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee00e-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-202">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ee00e-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="ee00e-203">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ee00e-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ee00e-205"> (0)</span><span class="sxs-lookup"><span data-stu-id="ee00e-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-206">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ee00e-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ee00e-208">(1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-209">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ee00e-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ee00e-211">(2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ee00e-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ee00e-213">(3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-214">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="ee00e-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ee00e-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ee00e-216">(4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-217">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-217">Device is not working properly.</span></span> <span data-ttu-id="ee00e-218">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ee00e-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ee00e-220">(5)</span><span class="sxs-lookup"><span data-stu-id="ee00e-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-221">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="ee00e-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ee00e-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ee00e-223"> (6)</span><span class="sxs-lookup"><span data-stu-id="ee00e-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-224">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ee00e-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ee00e-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ee00e-226">(7)</span><span class="sxs-lookup"><span data-stu-id="ee00e-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ee00e-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ee00e-228">(8)</span><span class="sxs-lookup"><span data-stu-id="ee00e-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-229">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="ee00e-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ee00e-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ee00e-231">(9)</span><span class="sxs-lookup"><span data-stu-id="ee00e-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-232">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-232">Device is not working properly.</span></span> <span data-ttu-id="ee00e-233">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ee00e-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ee00e-235">(10)</span><span class="sxs-lookup"><span data-stu-id="ee00e-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-236">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ee00e-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ee00e-238">(11)</span><span class="sxs-lookup"><span data-stu-id="ee00e-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-239">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ee00e-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ee00e-241">12</span><span class="sxs-lookup"><span data-stu-id="ee00e-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-242">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="ee00e-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ee00e-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ee00e-244">(13)</span><span class="sxs-lookup"><span data-stu-id="ee00e-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-245">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ee00e-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ee00e-247">(14)</span><span class="sxs-lookup"><span data-stu-id="ee00e-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-248">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ee00e-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ee00e-250">(15)</span><span class="sxs-lookup"><span data-stu-id="ee00e-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-251">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ee00e-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ee00e-253">(16)</span><span class="sxs-lookup"><span data-stu-id="ee00e-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-254">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ee00e-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ee00e-256">(17)</span><span class="sxs-lookup"><span data-stu-id="ee00e-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-257">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ee00e-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ee00e-259">(18)</span><span class="sxs-lookup"><span data-stu-id="ee00e-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-260">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ee00e-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ee00e-262">(19)</span><span class="sxs-lookup"><span data-stu-id="ee00e-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ee00e-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ee00e-264">(20)</span><span class="sxs-lookup"><span data-stu-id="ee00e-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-265">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ee00e-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ee00e-267">(21)</span><span class="sxs-lookup"><span data-stu-id="ee00e-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-268">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ee00e-268">System failure.</span></span> <span data-ttu-id="ee00e-269">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ee00e-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ee00e-270">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ee00e-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ee00e-272">(22)</span><span class="sxs-lookup"><span data-stu-id="ee00e-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-273">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ee00e-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ee00e-275">(23)</span><span class="sxs-lookup"><span data-stu-id="ee00e-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-276">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ee00e-276">System failure.</span></span> <span data-ttu-id="ee00e-277">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ee00e-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ee00e-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ee00e-279">(24)</span><span class="sxs-lookup"><span data-stu-id="ee00e-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-280">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="ee00e-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ee00e-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ee00e-282">(25)</span><span class="sxs-lookup"><span data-stu-id="ee00e-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-283">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ee00e-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ee00e-285">(26)</span><span class="sxs-lookup"><span data-stu-id="ee00e-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-286">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ee00e-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ee00e-288">(27)</span><span class="sxs-lookup"><span data-stu-id="ee00e-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-289">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="ee00e-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ee00e-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ee00e-291">(28)</span><span class="sxs-lookup"><span data-stu-id="ee00e-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-292">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="ee00e-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ee00e-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ee00e-294">(29)</span><span class="sxs-lookup"><span data-stu-id="ee00e-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-295">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-295">Device is disabled.</span></span> <span data-ttu-id="ee00e-296">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="ee00e-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ee00e-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ee00e-298">(30)</span><span class="sxs-lookup"><span data-stu-id="ee00e-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-299">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ee00e-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="ee00e-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ee00e-301">31</span><span class="sxs-lookup"><span data-stu-id="ee00e-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-302">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-302">Device is not working properly.</span></span> <span data-ttu-id="ee00e-303">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="ee00e-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-304">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ee00e-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-305">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-307">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee00e-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-308">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ee00e-309">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-310">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee00e-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-311">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-313">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ee00e-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-314">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="ee00e-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ee00e-315">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ee00e-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ee00e-316">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-317">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ee00e-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-320">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ee00e-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-321">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-321">Description of the object.</span></span>

<span data-ttu-id="ee00e-322">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-323">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ee00e-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-326">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="ee00e-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-327">Identificatore univoco del disco logico di altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ee00e-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="ee00e-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ee00e-329">Per un esempio di codice che recupera questa proprietà, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee00e-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="ee00e-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-331">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee00e-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-333">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| filefunctions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="ee00e-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-334">Valore numerico che corrisponde al tipo di unità disco rappresentata da questo disco logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00e-335">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ee00e-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="ee00e-336">**Nessuna directory radice** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="ee00e-337">**Disco rimovibile** (2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="ee00e-338">**Disco locale** (3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="ee00e-339">**Unità di rete** (4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="ee00e-340">**Compact Disc** (5)</span><span class="sxs-lookup"><span data-stu-id="ee00e-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="ee00e-341">**Disco RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="ee00e-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-342">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ee00e-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-343">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-345">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="ee00e-346">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ee00e-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-350">Altre informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="ee00e-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="ee00e-351">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-352">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="ee00e-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-355">Tipo di rilevamento e correzione degli errori supportato da questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="ee00e-356">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-357">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="ee00e-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-360">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="ee00e-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-361">File System sul disco logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-361">File system on the logical disk.</span></span>

<span data-ttu-id="ee00e-362">Esempio: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="ee00e-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="ee00e-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-364">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee00e-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-366">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="ee00e-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-367">Spazio, in byte, disponibile sul disco logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="ee00e-368">Questa proprietà viene ereditata da [**CIM \_ disco logico**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="ee00e-369">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ee00e-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ee00e-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-371">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee00e-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-373">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ee00e-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-374">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-374">Date and time the object was installed.</span></span> <span data-ttu-id="ee00e-375">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ee00e-376">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ee00e-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-378">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee00e-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-380">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ee00e-381">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-382">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="ee00e-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-383">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee00e-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-385">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="ee00e-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-386">Lunghezza massima di un componente filename supportato dall'unità Windows.</span><span class="sxs-lookup"><span data-stu-id="ee00e-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="ee00e-387">Un componente filename è la parte di un nome di file tra le barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="ee00e-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="ee00e-388">Il valore può essere utilizzato per indicare che i nomi lunghi sono supportati dal file system specificato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="ee00e-389">Ad esempio, per un file system FAT che supporta nomi lunghi, la funzione archivia il valore 255, anziché l'indicatore 8,3 precedente.</span><span class="sxs-lookup"><span data-stu-id="ee00e-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="ee00e-390">I nomi lunghi possono inoltre essere supportati nei sistemi che utilizzano il file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="ee00e-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="ee00e-391">Esempio: 255</span><span class="sxs-lookup"><span data-stu-id="ee00e-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-392">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="ee00e-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-393">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee00e-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-395">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and Output functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="ee00e-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-396">Tipo di file multimediali attualmente presenti nell'unità logica.</span><span class="sxs-lookup"><span data-stu-id="ee00e-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="ee00e-397">Questo valore sarà uno dei valori dell'enumerazione del tipo di supporto \_ definita in winioctl. h.</span><span class="sxs-lookup"><span data-stu-id="ee00e-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="ee00e-398">Il valore potrebbe non essere esatto per le unità rimovibili se attualmente non è presente alcun supporto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="ee00e-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="ee00e-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Formato sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ee00e-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-401">Disco floppy da 5 1/4 pollici-1,2 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-403">Disco floppy da 3 1/2 pollici-1,44 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-405">Disco floppy da 3 1/2 pollici-2,88 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-407">Disco floppy da 3 1/2 pollici-20,8 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (5)</span><span class="sxs-lookup"><span data-stu-id="ee00e-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-409">Disco floppy da 3 1/2 pollici-720 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (6)</span><span class="sxs-lookup"><span data-stu-id="ee00e-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-411">Disco floppy da 5 1/4 pollici-360 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (7)</span><span class="sxs-lookup"><span data-stu-id="ee00e-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-413">Disco floppy da 5 1/4 pollici-320 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (8)</span><span class="sxs-lookup"><span data-stu-id="ee00e-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-415">Disco floppy da 5 1/4 pollici-320 KB-1024 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (9)</span><span class="sxs-lookup"><span data-stu-id="ee00e-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-417">Disco floppy da 5 1/4 pollici-180 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (10)</span><span class="sxs-lookup"><span data-stu-id="ee00e-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-419">Disco floppy da 5 1/4 pollici-160 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="ee00e-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Supporti rimovibili diversi da floppy** (11)</span><span class="sxs-lookup"><span data-stu-id="ee00e-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="ee00e-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Supporti disco rigido fissi** (12)</span><span class="sxs-lookup"><span data-stu-id="ee00e-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (13)</span><span class="sxs-lookup"><span data-stu-id="ee00e-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-423">Disco floppy da 3 1/2 pollici-120 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (14)</span><span class="sxs-lookup"><span data-stu-id="ee00e-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-425">Disco floppy da 3 1/2 pollici-640 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (15)</span><span class="sxs-lookup"><span data-stu-id="ee00e-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-427">Disco floppy da 5 1/4 pollici-640 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (16)</span><span class="sxs-lookup"><span data-stu-id="ee00e-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-429">Disco floppy da 5 1/4 pollici-720 KB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (17)</span><span class="sxs-lookup"><span data-stu-id="ee00e-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-431">Disco floppy da 3 1/2 pollici-1,2 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (18)</span><span class="sxs-lookup"><span data-stu-id="ee00e-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-433">Disco floppy da 3 1/2 pollici-1,23 MB-1024 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disco floppy da 5 pollici** (19)</span><span class="sxs-lookup"><span data-stu-id="ee00e-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-435">Disco floppy da 5 1/4 pollici-1,23 MB-1024 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (20)</span><span class="sxs-lookup"><span data-stu-id="ee00e-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-437">Disco floppy da 3 1/2 pollici-128 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disco floppy da 3 pollici** (21)</span><span class="sxs-lookup"><span data-stu-id="ee00e-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-439">Disco floppy da 3 1/2 pollici-230 MB-512 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="ee00e-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**disco floppy da 8 pollici** (22)</span><span class="sxs-lookup"><span data-stu-id="ee00e-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-441">Disco floppy da 8 pollici-256 KB-128 byte/settore</span><span class="sxs-lookup"><span data-stu-id="ee00e-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-442">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ee00e-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-443">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-445">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ee00e-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-446">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-446">Label by which the object is known.</span></span> <span data-ttu-id="ee00e-447">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="ee00e-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ee00e-448">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="ee00e-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-450">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee00e-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-452">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="ee00e-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-453">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="ee00e-454">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee00e-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="ee00e-455">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="ee00e-456">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="ee00e-457">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ee00e-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ee00e-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-459">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-461">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ee00e-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-462">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="ee00e-463">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ee00e-464">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ee00e-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-465">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ee00e-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-466">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee00e-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-468">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ee00e-469">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="ee00e-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00e-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ee00e-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ee00e-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ee00e-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ee00e-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-474">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="ee00e-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ee00e-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-476">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="ee00e-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ee00e-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ee00e-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-478">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ee00e-479">Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="ee00e-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="ee00e-480">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="ee00e-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ee00e-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="ee00e-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-482">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="ee00e-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ee00e-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="ee00e-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ee00e-484">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="ee00e-484">Timed Power-On Supported</span></span>

<span data-ttu-id="ee00e-485">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-486">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ee00e-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-487">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-489">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="ee00e-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="ee00e-490">Questa proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="ee00e-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="ee00e-491">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="ee00e-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-493">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-494">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-495">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows Networking Functions \| WNetGetConnection")</span><span class="sxs-lookup"><span data-stu-id="ee00e-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-496">Percorso di rete del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-497">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="ee00e-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-498">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-500">Stringa in formato libero che descrive i supporti e il relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="ee00e-501">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-502">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="ee00e-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-503">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-504">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-505">Indica che la gestione delle quote non è abilitata (TRUE) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ee00e-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-506">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="ee00e-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-507">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-508">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-509">Indica che la gestione delle quote è stata utilizzata ma è stata disabilitata (**true**).</span><span class="sxs-lookup"><span data-stu-id="ee00e-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="ee00e-510">Incompleto si riferisce alle informazioni rimaste nella file system dopo che la gestione delle quote è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ee00e-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-511">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="ee00e-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-512">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-514">Se **true**, indica che il file System è nel processo attivo di compilazione delle informazioni e impostazione del disco per la gestione delle quote.</span><span class="sxs-lookup"><span data-stu-id="ee00e-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-515">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="ee00e-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-516">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-517">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-518">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="ee00e-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-519">Dimensioni dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="ee00e-519">Size of the disk drive.</span></span>

<span data-ttu-id="ee00e-520">Questa proprietà viene ereditata da [**CIM \_ disco logico**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="ee00e-521">Per un esempio di codice che recupera questa proprietà, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee00e-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="ee00e-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-525">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ee00e-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-526">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee00e-526">Current status of the object.</span></span> <span data-ttu-id="ee00e-527">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="ee00e-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ee00e-528">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="ee00e-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ee00e-529">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="ee00e-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ee00e-530">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="ee00e-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ee00e-531">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="ee00e-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ee00e-532">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ee00e-533">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee00e-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ee00e-534">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ee00e-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ee00e-535">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ee00e-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ee00e-536">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ee00e-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00e-537">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ee00e-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ee00e-538">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ee00e-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ee00e-539">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ee00e-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ee00e-540">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ee00e-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ee00e-541">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ee00e-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ee00e-542">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ee00e-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ee00e-543">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ee00e-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ee00e-544">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ee00e-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ee00e-545">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ee00e-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ee00e-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-547">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee00e-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-549">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ee00e-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-550">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-550">State of the logical device.</span></span> <span data-ttu-id="ee00e-551">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="ee00e-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ee00e-552">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ee00e-553">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ee00e-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ee00e-554">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ee00e-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ee00e-555">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ee00e-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ee00e-556">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="ee00e-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ee00e-557">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="ee00e-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee00e-558">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="ee00e-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-559">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-560">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-561">Se **true**, questo volume supporta le quote disco.</span><span class="sxs-lookup"><span data-stu-id="ee00e-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-562">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="ee00e-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-563">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-564">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-565">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API file \| System functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ file \_ Compression")</span><span class="sxs-lookup"><span data-stu-id="ee00e-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-566">Se **true**, la partizione disco logico supporta la compressione basata su file, ad esempio il caso del file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="ee00e-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="ee00e-567">Questa proprietà è **false** quando la proprietà **compressa** è **true**.</span><span class="sxs-lookup"><span data-stu-id="ee00e-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-568">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee00e-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-569">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-570">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-571">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ee00e-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-572">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="ee00e-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="ee00e-573">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-574">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ee00e-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-575">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-576">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-577">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ee00e-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-578">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ee00e-578">Name of the scoping system.</span></span>

<span data-ttu-id="ee00e-579">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-580">**VolumeDirty**</span><span class="sxs-lookup"><span data-stu-id="ee00e-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-581">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee00e-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-582">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-583">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL \_ is \_ volume \_ Dirty")</span><span class="sxs-lookup"><span data-stu-id="ee00e-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-584">Se **true**, il disco richiede l'esecuzione di [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) al riavvio successivo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="ee00e-585">Questa proprietà è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer.</span><span class="sxs-lookup"><span data-stu-id="ee00e-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="ee00e-586">Non è applicabile alle unità logiche mappate.</span><span class="sxs-lookup"><span data-stu-id="ee00e-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-587">**NomeVolume**</span><span class="sxs-lookup"><span data-stu-id="ee00e-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-588">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-589">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ee00e-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-590">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="ee00e-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-591">Nome del volume del disco logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="ee00e-592">Vincoli: massimo 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ee00e-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="ee00e-593">Per un esempio di codice che recupera questa proprietà, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee00e-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="ee00e-594">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ee00e-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee00e-595">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee00e-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-596">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee00e-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee00e-597">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file System functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="ee00e-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="ee00e-598">Numero di serie del volume del disco logico.</span><span class="sxs-lookup"><span data-stu-id="ee00e-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="ee00e-599">Vincoli: massimo 11 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ee00e-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="ee00e-600">Esempio: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="ee00e-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee00e-601">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee00e-601">Remarks</span></span>

<span data-ttu-id="ee00e-602">La classe **Win32 \_ disco logico** è derivata da [**CIM \_ disco logico**](cim-logicaldisk.md) che deriva da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="ee00e-603">La classe **CIM \_ StorageExtent** è derivata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ee00e-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ee00e-604">Un'unità disco fisica è l'elemento fondamentale di qualsiasi sistema di gestione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="ee00e-605">Tuttavia, dopo l'installazione di un'unità disco fisica, né gli utenti né gli amministratori di sistema in genere gestiscono direttamente l'hardware.</span><span class="sxs-lookup"><span data-stu-id="ee00e-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="ee00e-606">Al contrario, gli utenti e gli amministratori di sistema interagiscono con le unità logiche create sul disco.</span><span class="sxs-lookup"><span data-stu-id="ee00e-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="ee00e-607">Un'unità logica è una suddivisione di una partizione a cui è stata assegnata una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="ee00e-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="ee00e-608">È possibile che sia presente una partizione a cui non è stata assegnata una lettera di unità. Quando si parla di unità C o unità D, si fa riferimento a un'unità logica anziché a un'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="ee00e-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="ee00e-609">Analogamente, quando si salva un documento nell'unità E, questo viene salvato nell'unità logica.</span><span class="sxs-lookup"><span data-stu-id="ee00e-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="ee00e-610">I dischi fisici costituiscono l'hardware che compone un'unità, inclusi componenti quali intestazioni, settori e cilindri.</span><span class="sxs-lookup"><span data-stu-id="ee00e-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="ee00e-611">Le unità logiche, al contrario, dispongono di proprietà quali spazio su disco, spazio su disco disponibile e lettere di unità.</span><span class="sxs-lookup"><span data-stu-id="ee00e-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="ee00e-612">La classe **Win32 \_ disco logico** può essere utilizzata solo per enumerare le proprietà delle unità disco locali.</span><span class="sxs-lookup"><span data-stu-id="ee00e-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="ee00e-613">Tuttavia, è possibile utilizzare la classe [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md) per enumerare le proprietà delle unità di rete mappate.</span><span class="sxs-lookup"><span data-stu-id="ee00e-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ee00e-614">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee00e-614">Examples</span></span>

<span data-ttu-id="ee00e-615">È possibile trovare altri esempi di utilizzo di **Win32 \_ disco logico** per ottenere i dati del disco o del volume nell'argomento [attività WMI: dischi e file System](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .</span><span class="sxs-lookup"><span data-stu-id="ee00e-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="ee00e-616">Nell'esempio di codice VBScript [Information Retriever WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) della raccolta TechNet viene utilizzata la classe **Win32 \_ disco logico** per recuperare informazioni sull'hardware da un numero di computer remoti.</span><span class="sxs-lookup"><span data-stu-id="ee00e-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="ee00e-617">[Ottenere informazioni sul disco utilizzando WMI/CIM...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) Nell'esempio di codice PowerShell nella raccolta TechNet viene usato **Win32 \_ disco logico** per recuperare **DeviceID**, **VolumeName** e **size** da un dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ee00e-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="ee00e-618">In particolare, in questo esempio viene inclusa la rigorosa gestione delle eccezioni e viene restituito un singolo oggetto per computer anziché per ogni disco.</span><span class="sxs-lookup"><span data-stu-id="ee00e-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="ee00e-619">Lo scripting aziendale implica spesso la configurazione di hardware e software su computer remoti. a sua volta, è necessario che il tipo di unità disco installato in un computer sia in anticipo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="ee00e-620">Ad esempio, uno script che installa un'applicazione nell'unità E funziona solo se l'unità E è un disco rigido.</span><span class="sxs-lookup"><span data-stu-id="ee00e-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="ee00e-621">Se l'unità E viene eseguita per rappresentare un disco floppy o un'unità CD-ROM, lo script avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ee00e-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="ee00e-622">Il codice seguente identifica le unità e i tipi di unità installati in un computer</span><span class="sxs-lookup"><span data-stu-id="ee00e-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="ee00e-623">Gli esempi seguenti enumerano lo spazio libero su tutte le unità disco rigido di un computer.</span><span class="sxs-lookup"><span data-stu-id="ee00e-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="ee00e-624">Nell'esempio di codice seguente viene restituito il tipo di file system (FAT, NTFS, FAT32 e così via) utilizzato in ogni unità di un computer.</span><span class="sxs-lookup"><span data-stu-id="ee00e-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="ee00e-625">Nell'esempio di codice PowerShell seguente vengono recuperate informazioni aggiuntive sui dischi locali logici.</span><span class="sxs-lookup"><span data-stu-id="ee00e-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="ee00e-626">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee00e-626">Requirements</span></span>



| <span data-ttu-id="ee00e-627">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee00e-627">Requirement</span></span> | <span data-ttu-id="ee00e-628">Valore</span><span class="sxs-lookup"><span data-stu-id="ee00e-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee00e-629">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee00e-629">Minimum supported client</span></span><br/> | <span data-ttu-id="ee00e-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee00e-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee00e-631">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee00e-631">Minimum supported server</span></span><br/> | <span data-ttu-id="ee00e-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee00e-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee00e-633">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ee00e-633">Namespace</span></span><br/>                | <span data-ttu-id="ee00e-634">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ee00e-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee00e-635">MOF</span><span class="sxs-lookup"><span data-stu-id="ee00e-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee00e-636"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee00e-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee00e-637">DLL</span><span class="sxs-lookup"><span data-stu-id="ee00e-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee00e-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee00e-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee00e-639">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee00e-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee00e-640">**\_Disco logico CIM**</span><span class="sxs-lookup"><span data-stu-id="ee00e-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="ee00e-641">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ee00e-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ee00e-642">Attività WMI: dischi e file System</span><span class="sxs-lookup"><span data-stu-id="ee00e-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 


---
description: Rappresenta le funzionalità e la capacità di gestione di un'area partizionata di un disco fisico in un sistema di computer che esegue Windows.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Classe Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878153"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="33fe8-103">Win32 \_ DiskPartition (classe)</span><span class="sxs-lookup"><span data-stu-id="33fe8-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="33fe8-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskPartition Win32** rappresenta le funzionalità e la capacità di gestione di un'area partizionata di un disco fisico in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="33fe8-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="33fe8-105">Esempio: disco \# 0, partizione \# 1.</span><span class="sxs-lookup"><span data-stu-id="33fe8-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="33fe8-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="33fe8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="33fe8-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="33fe8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="33fe8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33fe8-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="33fe8-109">Members</span><span class="sxs-lookup"><span data-stu-id="33fe8-109">Members</span></span>

<span data-ttu-id="33fe8-110">La classe **Win32 \_ DiskPartition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33fe8-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="33fe8-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="33fe8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="33fe8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33fe8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="33fe8-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="33fe8-113">Methods</span></span>

<span data-ttu-id="33fe8-114">La classe **Win32 \_ DiskPartition** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="33fe8-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="33fe8-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="33fe8-115">Method</span></span>                                                     | <span data-ttu-id="33fe8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33fe8-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33fe8-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="33fe8-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="33fe8-118">Richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="33fe8-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="33fe8-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="33fe8-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="33fe8-120">Imposta lo stato di alimentazione desiderato per un dispositivo logico e quando deve essere inserito un dispositivo in tale stato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="33fe8-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33fe8-121">Properties</span></span>

<span data-ttu-id="33fe8-122">La classe **Win32 \_ DiskPartition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="33fe8-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33fe8-123">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="33fe8-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-124">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33fe8-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-126">Accesso ai supporti disponibile.</span><span class="sxs-lookup"><span data-stu-id="33fe8-126">Media access available.</span></span>

<span data-ttu-id="33fe8-127">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="33fe8-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="33fe8-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="33fe8-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="33fe8-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="33fe8-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-131">Scrivibile</span><span class="sxs-lookup"><span data-stu-id="33fe8-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="33fe8-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="33fe8-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="33fe8-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="33fe8-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="33fe8-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-135">Tipo di dati: **unit16**</span><span class="sxs-lookup"><span data-stu-id="33fe8-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-136">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="33fe8-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-137">Disponibilità e stato aggiuntive del dispositivo, oltre a quello specificato nella proprietà Availability.</span><span class="sxs-lookup"><span data-stu-id="33fe8-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="33fe8-138">La proprietà **Availability** indica lo stato primario e la disponibilità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="33fe8-139">In alcuni casi, non sarà sufficiente indicare lo stato completo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="33fe8-140">In questi casi, è possibile usare la proprietà **AdditionalAvailability** per fornire ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="33fe8-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="33fe8-141">Ad esempio, la **disponibilità** primaria di un dispositivo potrebbe essere offline (valore = 8), ma potrebbe anche essere in uno stato di basso consumo (valore **AdditonalAvailability** = 14) oppure il dispositivo potrebbe eseguire la diagnostica (valore **AdditionalAvailability** = 5, in test) ".</span><span class="sxs-lookup"><span data-stu-id="33fe8-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="33fe8-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="33fe8-143">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="33fe8-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-144">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="33fe8-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="33fe8-145">**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="33fe8-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="33fe8-146">**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="33fe8-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="33fe8-147">**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="33fe8-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="33fe8-148">**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="33fe8-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="33fe8-149">**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="33fe8-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="33fe8-150">**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="33fe8-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="33fe8-151">**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="33fe8-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="33fe8-152">**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="33fe8-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="33fe8-153">**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="33fe8-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="33fe8-154">**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="33fe8-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="33fe8-155">**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="33fe8-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="33fe8-156">**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="33fe8-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="33fe8-157">**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="33fe8-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="33fe8-158">**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="33fe8-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="33fe8-159">**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="33fe8-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="33fe8-160">In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="33fe8-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="33fe8-161">**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="33fe8-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="33fe8-162">**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="33fe8-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="33fe8-163">**Mettere in stato** (21)</span><span class="sxs-lookup"><span data-stu-id="33fe8-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-164">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="33fe8-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33fe8-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-167">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="33fe8-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-168">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-168">Availability and status of the device.</span></span>

<span data-ttu-id="33fe8-169">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="33fe8-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="33fe8-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="33fe8-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="33fe8-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="33fe8-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="33fe8-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="33fe8-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="33fe8-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="33fe8-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="33fe8-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="33fe8-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="33fe8-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="33fe8-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="33fe8-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="33fe8-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="33fe8-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="33fe8-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="33fe8-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="33fe8-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="33fe8-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="33fe8-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="33fe8-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="33fe8-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="33fe8-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="33fe8-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-183">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="33fe8-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="33fe8-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-185">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="33fe8-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="33fe8-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="33fe8-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-187">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="33fe8-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="33fe8-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="33fe8-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="33fe8-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="33fe8-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-190">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="33fe8-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="33fe8-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="33fe8-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-192">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="33fe8-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="33fe8-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="33fe8-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-194">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="33fe8-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="33fe8-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-196">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="33fe8-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="33fe8-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-198">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="33fe8-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="33fe8-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-200">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-202">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="33fe8-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-203">Dimensioni in byte dei blocchi che formano questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="33fe8-204">Se è sconosciuto o se un concetto di blocco non è valido (ad esempio per extent di aggregazione, memoria o dischi logici), immettere 1.</span><span class="sxs-lookup"><span data-stu-id="33fe8-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="33fe8-205">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="33fe8-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="33fe8-206">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-207">**Avviabile**</span><span class="sxs-lookup"><span data-stu-id="33fe8-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-208">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-210">Indica se il computer può essere avviato da questa partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="33fe8-211">Questa proprietà viene ereditata da [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-212">**BootPartition**</span><span class="sxs-lookup"><span data-stu-id="33fe8-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-213">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-215">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="33fe8-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-216">Partition è la partizione attiva.</span><span class="sxs-lookup"><span data-stu-id="33fe8-216">Partition is the active partition.</span></span> <span data-ttu-id="33fe8-217">Il sistema operativo utilizza la partizione attiva quando si esegue l'avvio da un disco rigido.</span><span class="sxs-lookup"><span data-stu-id="33fe8-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-218">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="33fe8-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-219">Tipo di dati: **String.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-221">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="33fe8-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-222">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-222">Short description of the object.</span></span>

<span data-ttu-id="33fe8-223">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="33fe8-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-225">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fe8-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-227">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="33fe8-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-228">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="33fe8-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="33fe8-229">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="33fe8-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="33fe8-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="33fe8-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-232">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="33fe8-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="33fe8-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="33fe8-234">(1)</span><span class="sxs-lookup"><span data-stu-id="33fe8-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="33fe8-235">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="33fe8-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="33fe8-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="33fe8-237">(2)</span><span class="sxs-lookup"><span data-stu-id="33fe8-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="33fe8-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="33fe8-239">(3)</span><span class="sxs-lookup"><span data-stu-id="33fe8-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="33fe8-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="33fe8-241">(4)</span><span class="sxs-lookup"><span data-stu-id="33fe8-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="33fe8-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="33fe8-243">(5)</span><span class="sxs-lookup"><span data-stu-id="33fe8-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="33fe8-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="33fe8-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="33fe8-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="33fe8-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="33fe8-247">(7)</span><span class="sxs-lookup"><span data-stu-id="33fe8-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="33fe8-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="33fe8-249">(8)</span><span class="sxs-lookup"><span data-stu-id="33fe8-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="33fe8-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="33fe8-251">(9)</span><span class="sxs-lookup"><span data-stu-id="33fe8-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="33fe8-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="33fe8-253">(10)</span><span class="sxs-lookup"><span data-stu-id="33fe8-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="33fe8-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="33fe8-255">(11)</span><span class="sxs-lookup"><span data-stu-id="33fe8-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="33fe8-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="33fe8-257">12</span><span class="sxs-lookup"><span data-stu-id="33fe8-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="33fe8-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="33fe8-259">(13)</span><span class="sxs-lookup"><span data-stu-id="33fe8-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="33fe8-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="33fe8-261">(14)</span><span class="sxs-lookup"><span data-stu-id="33fe8-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="33fe8-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="33fe8-263">(15)</span><span class="sxs-lookup"><span data-stu-id="33fe8-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="33fe8-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="33fe8-265">(16)</span><span class="sxs-lookup"><span data-stu-id="33fe8-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="33fe8-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="33fe8-267">(17)</span><span class="sxs-lookup"><span data-stu-id="33fe8-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="33fe8-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="33fe8-269">(18)</span><span class="sxs-lookup"><span data-stu-id="33fe8-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="33fe8-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="33fe8-271">(19)</span><span class="sxs-lookup"><span data-stu-id="33fe8-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="33fe8-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="33fe8-273">(20)</span><span class="sxs-lookup"><span data-stu-id="33fe8-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="33fe8-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="33fe8-275">(21)</span><span class="sxs-lookup"><span data-stu-id="33fe8-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="33fe8-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="33fe8-277">(22)</span><span class="sxs-lookup"><span data-stu-id="33fe8-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="33fe8-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="33fe8-279">(23)</span><span class="sxs-lookup"><span data-stu-id="33fe8-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="33fe8-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="33fe8-281">(24)</span><span class="sxs-lookup"><span data-stu-id="33fe8-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="33fe8-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="33fe8-283">(25)</span><span class="sxs-lookup"><span data-stu-id="33fe8-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="33fe8-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="33fe8-285">(26)</span><span class="sxs-lookup"><span data-stu-id="33fe8-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="33fe8-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="33fe8-287">(27)</span><span class="sxs-lookup"><span data-stu-id="33fe8-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="33fe8-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="33fe8-289">(28)</span><span class="sxs-lookup"><span data-stu-id="33fe8-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="33fe8-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="33fe8-291">(29)</span><span class="sxs-lookup"><span data-stu-id="33fe8-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="33fe8-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="33fe8-293">(30)</span><span class="sxs-lookup"><span data-stu-id="33fe8-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="33fe8-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="33fe8-295">31</span><span class="sxs-lookup"><span data-stu-id="33fe8-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="33fe8-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-297">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-299">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="33fe8-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-300">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="33fe8-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="33fe8-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="33fe8-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-303">Tipo di dati: **String.**</span><span class="sxs-lookup"><span data-stu-id="33fe8-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-305">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="33fe8-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-306">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="33fe8-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="33fe8-307">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="33fe8-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="33fe8-308">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-309">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="33fe8-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-312">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="33fe8-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-313">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-313">Description of the object.</span></span>

<span data-ttu-id="33fe8-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="33fe8-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-318">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="33fe8-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-319">Identificatore univoco dell'unità disco e della partizione, dal resto del sistema.</span><span class="sxs-lookup"><span data-stu-id="33fe8-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="33fe8-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-321">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fe8-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-323">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="33fe8-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-324">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="33fe8-325">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="33fe8-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="33fe8-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-327">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-329">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="33fe8-330">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="33fe8-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-334">Informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="33fe8-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="33fe8-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-336">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="33fe8-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-339">Tipo di rilevamento e correzione degli errori supportato da questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="33fe8-340">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-341">**HiddenSectors**</span><span class="sxs-lookup"><span data-stu-id="33fe8-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-342">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fe8-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-344">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span><span class="sxs-lookup"><span data-stu-id="33fe8-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-345">Numero di settori nascosti nella partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="33fe8-346">Esempio: 63</span><span class="sxs-lookup"><span data-stu-id="33fe8-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="33fe8-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-348">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="33fe8-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-350">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci della matrice OtherIdentifyingInfo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="33fe8-351">Si noti che ogni voce di questa matrice è correlata alla voce in OtherIdentifyingInfo che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="33fe8-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="33fe8-352">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="33fe8-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-354">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fe8-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-356">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="33fe8-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-357">Numero di indice della partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-357">Index number of the partition.</span></span>

<span data-ttu-id="33fe8-358">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="33fe8-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="33fe8-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-360">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="33fe8-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-362">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="33fe8-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-363">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-363">Date the object was installed.</span></span> <span data-ttu-id="33fe8-364">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="33fe8-365">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-366">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="33fe8-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-367">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fe8-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-369">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="33fe8-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="33fe8-370">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-371">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="33fe8-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-372">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-374">Qualificatori: **depricated**</span><span class="sxs-lookup"><span data-stu-id="33fe8-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-375">Tempo massimo in millisecondi durante il quale un dispositivo può essere eseguito in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="33fe8-376">Lo stato di un dispositivo viene definito nelle proprietà Availability e AdditionalAvailability, in cui inattivo viene trasmesso dal valore 21.</span><span class="sxs-lookup"><span data-stu-id="33fe8-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="33fe8-377">Ciò che si verifica alla fine del limite di tempo è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="33fe8-378">Il dispositivo può riattivare, può essere offline o eseguire altre azioni.</span><span class="sxs-lookup"><span data-stu-id="33fe8-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="33fe8-379">Il valore 0 indica che un dispositivo può rimanere inattivo per un periodo illimitato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="33fe8-380">"La proprietà MaxQuiesceTime è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="33fe8-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="33fe8-381">Quando si valuta l'uso di mettere in stato, è stato determinato che questa singola proprietà non è adatta per la descrizione del momento in cui un dispositivo uscirà automaticamente da uno stato di riposo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="33fe8-382">In realtà, lo scenario più probabile per un dispositivo di uscire da uno stato di riposo è stato determinato in base al numero di richieste in attesa in coda anziché a un tempo massimo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="33fe8-383">Questa operazione verrà nuovamente valutata e riposizionata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="33fe8-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="33fe8-384">\\n</span><span class="sxs-lookup"><span data-stu-id="33fe8-384">\\n</span></span>

 

<span data-ttu-id="33fe8-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-386">**Nome**</span><span class="sxs-lookup"><span data-stu-id="33fe8-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-389">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="33fe8-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-390">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-390">Label by which the object is known.</span></span> <span data-ttu-id="33fe8-391">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="33fe8-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="33fe8-392">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="33fe8-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-394">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-396">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="33fe8-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-397">Numero totale di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce questo extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="33fe8-398">Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="33fe8-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="33fe8-399">Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="33fe8-400">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="33fe8-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="33fe8-401">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="33fe8-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-403">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-405">Matrice che acquisisce dati aggiuntivi, oltre alle informazioni di DeviceID, che possono essere usati per identificare un LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="33fe8-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="33fe8-406">Un esempio è quello di contenere il nome descrittivo dell'utente del sistema operativo per il dispositivo in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="33fe8-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="33fe8-407">La lunghezza massima è 256.</span><span class="sxs-lookup"><span data-stu-id="33fe8-407">Maximum length is 256.</span></span>

<span data-ttu-id="33fe8-408">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="33fe8-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-410">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-412">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="33fe8-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-413">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="33fe8-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="33fe8-414">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="33fe8-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="33fe8-415">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-416">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="33fe8-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-417">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33fe8-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-419">Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="33fe8-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="33fe8-420">I valori della matrice, 0 = "Unknown", 1 = "not supported" e 2 = "disabled" sono autoesplicativi.</span><span class="sxs-lookup"><span data-stu-id="33fe8-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="33fe8-421">Il valore 3 = "Enabled" indica che le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="33fe8-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="33fe8-422">"Le modalità di risparmio energia immesse automaticamente" (4) descrivono che un dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="33fe8-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="33fe8-423">"Lo stato di alimentazione impostabile" (5) indica che il metodo SetPowerState è supportato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="33fe8-424">"Power Cycling supported" (6) indica che il metodo SetPowerState può essere richiamato con la variabile di input PowerState impostata su 5 ("ciclo di alimentazione").</span><span class="sxs-lookup"><span data-stu-id="33fe8-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="33fe8-425">"Tempo di accensione supportato" (7) indica che il metodo SetPowerState può essere richiamato con la variabile di input PowerState impostata su 5 ("ciclo di alimentazione") e il parametro ora impostato su una data e un'ora specifiche, o un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="33fe8-426">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-427">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="33fe8-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="33fe8-428">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="33fe8-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="33fe8-429">**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="33fe8-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="33fe8-430">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="33fe8-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="33fe8-431">**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="33fe8-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="33fe8-432">**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="33fe8-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="33fe8-433">**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="33fe8-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="33fe8-434">**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="33fe8-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="33fe8-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-436">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-438">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="33fe8-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="33fe8-439">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="33fe8-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="33fe8-440">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-441">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="33fe8-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-442">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-444">Il numero di ore consecutive in cui il dispositivo è stato alimentato, dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="33fe8-445">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-446">**Partizione primaria**</span><span class="sxs-lookup"><span data-stu-id="33fe8-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-447">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-449">Se **true**, si tratta della partizione primaria.</span><span class="sxs-lookup"><span data-stu-id="33fe8-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="33fe8-450">Questa proprietà viene ereditata da [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-451">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="33fe8-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-452">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-454">Descrizione del supporto e del relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-454">Description of the media and its use.</span></span>

<span data-ttu-id="33fe8-455">Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-456">**RewritePartition**</span><span class="sxs-lookup"><span data-stu-id="33fe8-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-457">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fe8-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-459">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| device input and output Structure \| [**\_ Information**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RewritePartition")</span><span class="sxs-lookup"><span data-stu-id="33fe8-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-460">Se **true**, le informazioni sulla partizione sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="33fe8-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="33fe8-461">Quando si modifica una partizione (con [**il \_ \_ layout dell' \_ unità \_ del set di dischi IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), il sistema utilizza questa proprietà per determinare quali partizioni sono state modificate ed è necessario riscrivere le relative informazioni.</span><span class="sxs-lookup"><span data-stu-id="33fe8-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="33fe8-462">Se **true**, la partizione deve essere riscritta.</span><span class="sxs-lookup"><span data-stu-id="33fe8-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-463">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="33fe8-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-464">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-466">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="33fe8-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-467">Dimensioni totali della partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-467">Total size of the partition.</span></span>

<span data-ttu-id="33fe8-468">Esempio: 1059045376</span><span class="sxs-lookup"><span data-stu-id="33fe8-468">Example: 1059045376</span></span>

<span data-ttu-id="33fe8-469">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="33fe8-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-470">**StartingOffset**</span><span class="sxs-lookup"><span data-stu-id="33fe8-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-471">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-473">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="33fe8-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-474">Offset iniziale (in byte) della partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="33fe8-475">Esempio: 32256</span><span class="sxs-lookup"><span data-stu-id="33fe8-475">Example: 32256</span></span>

<span data-ttu-id="33fe8-476">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="33fe8-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-477">**Status**</span><span class="sxs-lookup"><span data-stu-id="33fe8-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-478">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-479">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-480">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="33fe8-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-481">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33fe8-481">Current status of the object.</span></span> <span data-ttu-id="33fe8-482">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="33fe8-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="33fe8-483">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="33fe8-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="33fe8-484">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="33fe8-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="33fe8-485">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="33fe8-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="33fe8-486">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="33fe8-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="33fe8-487">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="33fe8-488">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="33fe8-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="33fe8-489">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="33fe8-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="33fe8-490">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="33fe8-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="33fe8-491">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="33fe8-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-492">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="33fe8-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="33fe8-493">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="33fe8-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="33fe8-494">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="33fe8-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="33fe8-495">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="33fe8-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="33fe8-496">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="33fe8-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="33fe8-497">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="33fe8-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="33fe8-498">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="33fe8-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="33fe8-499">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="33fe8-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="33fe8-500">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="33fe8-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="33fe8-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-502">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33fe8-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-503">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-504">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="33fe8-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-505">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="33fe8-505">State of the logical device.</span></span> <span data-ttu-id="33fe8-506">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="33fe8-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="33fe8-507">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="33fe8-508">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="33fe8-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-509">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="33fe8-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="33fe8-510">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="33fe8-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="33fe8-511">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="33fe8-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="33fe8-512">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="33fe8-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fe8-513">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="33fe8-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-514">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-515">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-516">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="33fe8-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-517">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="33fe8-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="33fe8-518">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-519">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="33fe8-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-520">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-521">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-522">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="33fe8-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-523">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="33fe8-523">Name of the scoping system.</span></span>

<span data-ttu-id="33fe8-524">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-525">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="33fe8-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-526">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="33fe8-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-527">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-528">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="33fe8-529">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fe8-530">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="33fe8-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fe8-531">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33fe8-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-532">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33fe8-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fe8-533">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| PartitionRecord \| dwPartitionType")</span><span class="sxs-lookup"><span data-stu-id="33fe8-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="33fe8-534">Tipo della partizione.</span><span class="sxs-lookup"><span data-stu-id="33fe8-534">Type of the partition.</span></span>

<span data-ttu-id="33fe8-535">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="33fe8-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="33fe8-536">Inutilizzati</span><span class="sxs-lookup"><span data-stu-id="33fe8-536">"Unused"</span></span></dd> <dd><span data-ttu-id="33fe8-537">"FAT a 12 bit"</span><span class="sxs-lookup"><span data-stu-id="33fe8-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="33fe8-538">"XENIX tipo 1"</span><span class="sxs-lookup"><span data-stu-id="33fe8-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="33fe8-539">"XENIX Type 2"</span><span class="sxs-lookup"><span data-stu-id="33fe8-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="33fe8-540">"FAT a 16 bit"</span><span class="sxs-lookup"><span data-stu-id="33fe8-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="33fe8-541">"Partizione estesa"</span><span class="sxs-lookup"><span data-stu-id="33fe8-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="33fe8-542">"MS-DOS V4 Huge"</span><span class="sxs-lookup"><span data-stu-id="33fe8-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="33fe8-543">"File system installabile"</span><span class="sxs-lookup"><span data-stu-id="33fe8-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="33fe8-544">"Piattaforma di riferimento PowerPC"</span><span class="sxs-lookup"><span data-stu-id="33fe8-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="33fe8-545">UNIX</span><span class="sxs-lookup"><span data-stu-id="33fe8-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="33fe8-546">NTFS</span><span class="sxs-lookup"><span data-stu-id="33fe8-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="33fe8-547">"Win95 w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="33fe8-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="33fe8-548">"Extended w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="33fe8-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="33fe8-549">"Gestione dischi logici"</span><span class="sxs-lookup"><span data-stu-id="33fe8-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="33fe8-550">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="33fe8-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="33fe8-551">Non **usato** ("non usato")</span><span class="sxs-lookup"><span data-stu-id="33fe8-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="33fe8-552">**FAT a 12 bit** ("FAT a 12 bit")</span><span class="sxs-lookup"><span data-stu-id="33fe8-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="33fe8-553">**XENIX tipo 1** ("XENIX tipo 1")</span><span class="sxs-lookup"><span data-stu-id="33fe8-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="33fe8-554">**XENIX tipo 2** ("XENIX Type 2")</span><span class="sxs-lookup"><span data-stu-id="33fe8-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="33fe8-555">**FAT a 16 bit** ("FAT a 16 bit")</span><span class="sxs-lookup"><span data-stu-id="33fe8-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="33fe8-556">**Partizione estesa** ("partizione estesa")</span><span class="sxs-lookup"><span data-stu-id="33fe8-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="33fe8-557">**MS-DOS V4 huge** ("MS-DOS V4 Huge")</span><span class="sxs-lookup"><span data-stu-id="33fe8-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="33fe8-558">**File system installabile** ("file system installabile")</span><span class="sxs-lookup"><span data-stu-id="33fe8-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="33fe8-559">**Piattaforma** di riferimento PowerPC ("piattaforma di riferimento PowerPC")</span><span class="sxs-lookup"><span data-stu-id="33fe8-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="33fe8-560">**UNIX** ("UNIX")</span><span class="sxs-lookup"><span data-stu-id="33fe8-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="33fe8-561">**NTFS** ("NTFS")</span><span class="sxs-lookup"><span data-stu-id="33fe8-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="33fe8-562">**Win95 w/int esteso 13** ("Win95 w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="33fe8-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="33fe8-563">**Extended w/Extended int 13** ("Extended w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="33fe8-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="33fe8-564">**Gestione dischi logici** (gestione dischi logici)</span><span class="sxs-lookup"><span data-stu-id="33fe8-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fe8-565">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="33fe8-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="33fe8-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="33fe8-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="33fe8-567">Commenti</span><span class="sxs-lookup"><span data-stu-id="33fe8-567">Remarks</span></span>

<span data-ttu-id="33fe8-568">La classe **Win32 \_ DiskPartition** è derivata da [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="33fe8-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="33fe8-569">Una partizione è una divisione strutturale di un'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="33fe8-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="33fe8-570">Sebbene un'unità possa contenere una singola partizione, i volumi più grandi vengono spesso divisi in più partizioni.</span><span class="sxs-lookup"><span data-stu-id="33fe8-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="33fe8-571">Questo è il motivo per cui è possibile che siano presenti unità C, D ed e anche se il computer dispone di un solo disco rigido fisico.</span><span class="sxs-lookup"><span data-stu-id="33fe8-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="33fe8-572">Windows supporta i tipi di partizione seguenti:</span><span class="sxs-lookup"><span data-stu-id="33fe8-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="33fe8-573">Partizione primaria.</span><span class="sxs-lookup"><span data-stu-id="33fe8-573">Primary partition.</span></span> <span data-ttu-id="33fe8-574">Si tratta dell'unico tipo di partizione in cui è possibile installare un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="33fe8-575">Ogni unità può avere un massimo di quattro partizioni primarie, ognuna delle quali assegna una lettera di unità diversa.</span><span class="sxs-lookup"><span data-stu-id="33fe8-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="33fe8-576">Partizione estesa.</span><span class="sxs-lookup"><span data-stu-id="33fe8-576">Extended partition.</span></span> <span data-ttu-id="33fe8-577">Partizione aggiuntiva che può essere suddivisa in più unità logiche, ciascuna delle quali assegna una lettera di unità univoca.</span><span class="sxs-lookup"><span data-stu-id="33fe8-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="33fe8-578">Un'unità può avere una sola partizione estesa. è tuttavia possibile dividere questa partizione in più unità logiche.</span><span class="sxs-lookup"><span data-stu-id="33fe8-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="33fe8-579">Questo consente a un disco di avere più di quattro partizioni primarie consentite.</span><span class="sxs-lookup"><span data-stu-id="33fe8-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="33fe8-580">Partizione di sistema.</span><span class="sxs-lookup"><span data-stu-id="33fe8-580">System partition.</span></span> <span data-ttu-id="33fe8-581">Qualsiasi partizione primaria contenente un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="33fe8-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="33fe8-582">Le partizioni possono indicare il modo in cui viene effettivamente utilizzata un'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="33fe8-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="33fe8-583">Esaminando le partizioni fisiche su un disco, è possibile determinare i tipi di elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="33fe8-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="33fe8-584">Modalità di suddivisione del disco in unità logiche.</span><span class="sxs-lookup"><span data-stu-id="33fe8-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="33fe8-585">Se sul disco è disponibile spazio non partizionato.</span><span class="sxs-lookup"><span data-stu-id="33fe8-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="33fe8-586">Questa operazione può essere determinata sottraendo le dimensioni di tutte le partizioni in un disco a partire dalle dimensioni del disco.</span><span class="sxs-lookup"><span data-stu-id="33fe8-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="33fe8-587">Se è possibile avviare il computer da tale disco (ovvero, il disco contiene una partizione di avvio).</span><span class="sxs-lookup"><span data-stu-id="33fe8-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="33fe8-588">Tutte queste domande possono essere risolte usando la classe **Win32 \_ DiskPartition** .</span><span class="sxs-lookup"><span data-stu-id="33fe8-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="33fe8-589">Esempio</span><span class="sxs-lookup"><span data-stu-id="33fe8-589">Examples</span></span>

<span data-ttu-id="33fe8-590">L'esempio di codice PowerShell seguente controlla l'allineamento dei dischi in un computer: se l'offset è frazionario, il disco non è allineato correttamente.</span><span class="sxs-lookup"><span data-stu-id="33fe8-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="33fe8-591">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33fe8-591">Requirements</span></span>



| <span data-ttu-id="33fe8-592">Requisito</span><span class="sxs-lookup"><span data-stu-id="33fe8-592">Requirement</span></span> | <span data-ttu-id="33fe8-593">Valore</span><span class="sxs-lookup"><span data-stu-id="33fe8-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33fe8-594">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33fe8-594">Minimum supported client</span></span><br/> | <span data-ttu-id="33fe8-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33fe8-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33fe8-596">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33fe8-596">Minimum supported server</span></span><br/> | <span data-ttu-id="33fe8-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33fe8-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33fe8-598">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33fe8-598">Namespace</span></span><br/>                | <span data-ttu-id="33fe8-599">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="33fe8-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33fe8-600">MOF</span><span class="sxs-lookup"><span data-stu-id="33fe8-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33fe8-601"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33fe8-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33fe8-602">DLL</span><span class="sxs-lookup"><span data-stu-id="33fe8-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33fe8-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33fe8-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33fe8-604">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33fe8-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fe8-605">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="33fe8-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="33fe8-606">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33fe8-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="33fe8-607">Attività WMI: dischi e file System</span><span class="sxs-lookup"><span data-stu-id="33fe8-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 


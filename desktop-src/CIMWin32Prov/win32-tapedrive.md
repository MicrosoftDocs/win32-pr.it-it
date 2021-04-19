---
description: La \_ classe WMI TapeDrive Win32 rappresenta un'unità nastro in un sistema di computer che esegue Windows. Le unità nastro si distinguono principalmente dal fatto che è possibile accedervi solo in modo sequenziale.
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Classe Win32_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304868"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="509d0-104">Win32 \_ TapeDrive (classe)</span><span class="sxs-lookup"><span data-stu-id="509d0-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="509d0-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TapeDrive Win32** rappresenta un'unità nastro in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="509d0-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="509d0-106">Le unità nastro si distinguono principalmente dal fatto che è possibile accedervi solo in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="509d0-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="509d0-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="509d0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="509d0-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="509d0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="509d0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="509d0-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="509d0-110">Members</span><span class="sxs-lookup"><span data-stu-id="509d0-110">Members</span></span>

<span data-ttu-id="509d0-111">La classe **Win32 \_ TapeDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="509d0-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="509d0-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="509d0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="509d0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="509d0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="509d0-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="509d0-114">Methods</span></span>

<span data-ttu-id="509d0-115">La classe **Win32 \_ TapeDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="509d0-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="509d0-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="509d0-116">Method</span></span>            | <span data-ttu-id="509d0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="509d0-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="509d0-118">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="509d0-118">**Reset**</span></span>         | <span data-ttu-id="509d0-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="509d0-119">Not implemented.</span></span> <span data-ttu-id="509d0-120">Per implementare questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="509d0-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="509d0-121">**SetPowerState**</span></span> | <span data-ttu-id="509d0-122">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="509d0-122">Not implemented.</span></span> <span data-ttu-id="509d0-123">Per implementare questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="509d0-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="509d0-124">Properties</span></span>

<span data-ttu-id="509d0-125">La classe **Win32 \_ TapeDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="509d0-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="509d0-126">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="509d0-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="509d0-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-129">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="509d0-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-130">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-130">Availability and status of the device.</span></span>

<span data-ttu-id="509d0-131">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="509d0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="509d0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="509d0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="509d0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="509d0-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="509d0-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-135">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="509d0-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="509d0-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="509d0-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="509d0-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="509d0-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="509d0-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="509d0-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="509d0-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="509d0-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="509d0-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="509d0-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="509d0-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="509d0-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="509d0-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="509d0-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="509d0-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="509d0-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="509d0-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="509d0-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="509d0-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="509d0-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-146">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="509d0-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="509d0-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="509d0-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-148">Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="509d0-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="509d0-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="509d0-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-150">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="509d0-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="509d0-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="509d0-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="509d0-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="509d0-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-153">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="509d0-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="509d0-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="509d0-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-155">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="509d0-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="509d0-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="509d0-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-157">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="509d0-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="509d0-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="509d0-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-159">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="509d0-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="509d0-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="509d0-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-161">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="509d0-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="509d0-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-163">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="509d0-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="509d0-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-165">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="509d0-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-166">Matrice di funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="509d0-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="509d0-167">Ad esempio, il dispositivo può supportare l'accesso casuale, i supporti rimovibili e la pulizia automatica.</span><span class="sxs-lookup"><span data-stu-id="509d0-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="509d0-168">In questo caso, i valori 3, 7 e 9 verranno scritti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="509d0-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="509d0-169">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="509d0-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="509d0-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="509d0-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="509d0-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="509d0-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="509d0-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="509d0-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="509d0-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="509d0-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="509d0-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="509d0-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="509d0-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="509d0-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="509d0-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="509d0-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="509d0-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-178">Supporta supporti rimovibili</span><span class="sxs-lookup"><span data-stu-id="509d0-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="509d0-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="509d0-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="509d0-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="509d0-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="509d0-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="509d0-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="509d0-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="509d0-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-183">Supporta Dual-Sided supporti</span><span class="sxs-lookup"><span data-stu-id="509d0-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="509d0-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="509d0-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="509d0-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-186">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="509d0-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="509d0-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-188">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="509d0-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-189">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità di accesso ai dispositivi indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="509d0-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="509d0-190">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="509d0-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="509d0-191">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-192">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="509d0-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-195">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="509d0-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-196">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="509d0-196">Short description of the object.</span></span>

<span data-ttu-id="509d0-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-198">**Compressione**</span><span class="sxs-lookup"><span data-stu-id="509d0-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-199">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-201">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| backup su nastro strutture \| [**nastro \_ ottenere compressione \_ \_ parametri unità**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ")</span><span class="sxs-lookup"><span data-stu-id="509d0-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-202">Se **true**, la compressione dei dati hardware è abilitata.</span><span class="sxs-lookup"><span data-stu-id="509d0-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="509d0-203"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="509d0-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="509d0-204">FALSE</span><span class="sxs-lookup"><span data-stu-id="509d0-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="509d0-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="509d0-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="509d0-206">true</span><span class="sxs-lookup"><span data-stu-id="509d0-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="509d0-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-210">Stringa in formato libero che indica l'algoritmo o lo strumento usato dal dispositivo per supportare la compressione.</span><span class="sxs-lookup"><span data-stu-id="509d0-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="509d0-211">Se non è possibile o non si desidera descrivere lo schema di compressione (probabilmente perché non è noto), utilizzare le parole seguenti: "Unknown" per indicare che non è noto se il dispositivo supporta o meno le funzionalità di compressione; "Compresso" per indicare che il dispositivo supporta le funzionalità di compressione, ma lo schema di compressione non è noto o non è stato divulgato; e "non compressi" per indicare che il dispositivo non supporta le funzionalità di compressione.</span><span class="sxs-lookup"><span data-stu-id="509d0-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="509d0-212">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="509d0-213">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="509d0-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="509d0-214">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="509d0-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="509d0-215">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="509d0-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="509d0-216">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="509d0-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="509d0-217">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="509d0-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="509d0-218">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="509d0-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="509d0-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-220">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-222">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="509d0-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-223">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="509d0-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="509d0-224">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="509d0-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="509d0-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="509d0-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="509d0-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-227">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="509d0-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="509d0-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="509d0-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="509d0-229">(1)</span><span class="sxs-lookup"><span data-stu-id="509d0-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-230">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="509d0-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="509d0-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="509d0-232">(2)</span><span class="sxs-lookup"><span data-stu-id="509d0-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="509d0-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="509d0-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="509d0-234">(3)</span><span class="sxs-lookup"><span data-stu-id="509d0-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-235">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="509d0-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="509d0-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="509d0-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="509d0-237">(4)</span><span class="sxs-lookup"><span data-stu-id="509d0-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-238">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="509d0-238">Device is not working properly.</span></span> <span data-ttu-id="509d0-239">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="509d0-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="509d0-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="509d0-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="509d0-241">(5)</span><span class="sxs-lookup"><span data-stu-id="509d0-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-242">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="509d0-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="509d0-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="509d0-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="509d0-244"> (6)</span><span class="sxs-lookup"><span data-stu-id="509d0-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-245">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="509d0-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="509d0-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="509d0-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="509d0-247">(7)</span><span class="sxs-lookup"><span data-stu-id="509d0-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="509d0-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="509d0-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="509d0-249">(8)</span><span class="sxs-lookup"><span data-stu-id="509d0-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-250">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="509d0-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="509d0-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="509d0-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="509d0-252">(9)</span><span class="sxs-lookup"><span data-stu-id="509d0-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-253">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="509d0-253">Device is not working properly.</span></span> <span data-ttu-id="509d0-254">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="509d0-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="509d0-256">(10)</span><span class="sxs-lookup"><span data-stu-id="509d0-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-257">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="509d0-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="509d0-259">(11)</span><span class="sxs-lookup"><span data-stu-id="509d0-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-260">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="509d0-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="509d0-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="509d0-262">12</span><span class="sxs-lookup"><span data-stu-id="509d0-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-263">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="509d0-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="509d0-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="509d0-265">(13)</span><span class="sxs-lookup"><span data-stu-id="509d0-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-266">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="509d0-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="509d0-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="509d0-268">(14)</span><span class="sxs-lookup"><span data-stu-id="509d0-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-269">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="509d0-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="509d0-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="509d0-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="509d0-271">(15)</span><span class="sxs-lookup"><span data-stu-id="509d0-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-272">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="509d0-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="509d0-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="509d0-274">(16)</span><span class="sxs-lookup"><span data-stu-id="509d0-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-275">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="509d0-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="509d0-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="509d0-277">(17)</span><span class="sxs-lookup"><span data-stu-id="509d0-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-278">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="509d0-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="509d0-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="509d0-280">(18)</span><span class="sxs-lookup"><span data-stu-id="509d0-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-281">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="509d0-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="509d0-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="509d0-283">(19)</span><span class="sxs-lookup"><span data-stu-id="509d0-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="509d0-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="509d0-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="509d0-285">(20)</span><span class="sxs-lookup"><span data-stu-id="509d0-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-286">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="509d0-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="509d0-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="509d0-288">(21)</span><span class="sxs-lookup"><span data-stu-id="509d0-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-289">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="509d0-289">System failure.</span></span> <span data-ttu-id="509d0-290">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="509d0-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="509d0-291">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="509d0-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="509d0-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="509d0-293">(22)</span><span class="sxs-lookup"><span data-stu-id="509d0-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-294">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="509d0-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="509d0-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="509d0-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="509d0-296">(23)</span><span class="sxs-lookup"><span data-stu-id="509d0-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-297">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="509d0-297">System failure.</span></span> <span data-ttu-id="509d0-298">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="509d0-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="509d0-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="509d0-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="509d0-300">(24)</span><span class="sxs-lookup"><span data-stu-id="509d0-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-301">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="509d0-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="509d0-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="509d0-303">(25)</span><span class="sxs-lookup"><span data-stu-id="509d0-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-304">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="509d0-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="509d0-306">(26)</span><span class="sxs-lookup"><span data-stu-id="509d0-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-307">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="509d0-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="509d0-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="509d0-309">(27)</span><span class="sxs-lookup"><span data-stu-id="509d0-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-310">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="509d0-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="509d0-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="509d0-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="509d0-312">(28)</span><span class="sxs-lookup"><span data-stu-id="509d0-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-313">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="509d0-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="509d0-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="509d0-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="509d0-315">(29)</span><span class="sxs-lookup"><span data-stu-id="509d0-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-316">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="509d0-316">Device is disabled.</span></span> <span data-ttu-id="509d0-317">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="509d0-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="509d0-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="509d0-319">(30)</span><span class="sxs-lookup"><span data-stu-id="509d0-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-320">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="509d0-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="509d0-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="509d0-322">31</span><span class="sxs-lookup"><span data-stu-id="509d0-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-323">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="509d0-323">Device is not working properly.</span></span> <span data-ttu-id="509d0-324">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="509d0-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-325">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="509d0-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-326">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="509d0-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-328">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="509d0-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-329">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="509d0-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="509d0-330">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-331">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="509d0-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-332">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-334">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="509d0-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="509d0-335">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="509d0-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="509d0-336">Se utilizzata con le altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="509d0-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="509d0-337">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-338">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="509d0-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-339">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="509d0-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-341">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="509d0-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-342">Dimensioni del blocco predefinite, in byte, per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="509d0-343">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="509d0-344">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-345">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="509d0-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-348">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="509d0-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-349">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="509d0-349">Description of the object.</span></span>

<span data-ttu-id="509d0-350">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="509d0-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-354">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| file functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="509d0-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-355">Identificatore univoco dell'unità nastro con altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="509d0-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="509d0-356">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="509d0-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-358">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-360">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API di \| backup su nastro su \| [**nastro \_ ottenere i \_ \_ parametri di unità**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ecc")</span><span class="sxs-lookup"><span data-stu-id="509d0-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-361">Se **true**, il dispositivo supporta la correzione degli errori hardware.</span><span class="sxs-lookup"><span data-stu-id="509d0-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="509d0-362">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="509d0-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="509d0-363">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="509d0-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-364">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="509d0-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-365">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-367">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="509d0-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-368">Dimensioni della zona per l'avviso di fine del nastro (EOT).</span><span class="sxs-lookup"><span data-stu-id="509d0-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="509d0-369">Questa proprietà viene ereditata da [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-370">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="509d0-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-371">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="509d0-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-373">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="509d0-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="509d0-374">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="509d0-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-378">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="509d0-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="509d0-379">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-380">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="509d0-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-383">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="509d0-384">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-385">**FeaturesHigh**</span><span class="sxs-lookup"><span data-stu-id="509d0-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-386">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-388">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API nastri di backup su nastro \| \| [**nastro \_ get \_ unità \_ parametri**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesHigh")</span><span class="sxs-lookup"><span data-stu-id="509d0-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-389">32 bit di ordine superiore del flag delle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="509d0-390">**FeaturesLow**</span><span class="sxs-lookup"><span data-stu-id="509d0-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-391">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-393">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API nastri di backup su nastro \| \| [**nastro \_ get \_ unità \_ parametri**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesLow")</span><span class="sxs-lookup"><span data-stu-id="509d0-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-394">32 bit di ordine inferiore del flag delle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="509d0-395">**Id**</span><span class="sxs-lookup"><span data-stu-id="509d0-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-396">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-398">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funzioni file Win32API")</span><span class="sxs-lookup"><span data-stu-id="509d0-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-399">Nome di identificazione del produttore dell'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="509d0-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="509d0-400">Esempio: "PLEXTOR CD-ROM PX-12CS 1,01"</span><span class="sxs-lookup"><span data-stu-id="509d0-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="509d0-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="509d0-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-402">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="509d0-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-404">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="509d0-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-405">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="509d0-405">Date and time the object was installed.</span></span> <span data-ttu-id="509d0-406">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="509d0-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="509d0-407">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-408">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="509d0-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-409">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-411">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="509d0-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="509d0-412">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-413">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="509d0-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-414">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-416">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="509d0-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-417">Produttore dell'unità CD-ROM di Windows.</span><span class="sxs-lookup"><span data-stu-id="509d0-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="509d0-418">Esempio: "PLEXTOR"</span><span class="sxs-lookup"><span data-stu-id="509d0-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="509d0-419">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="509d0-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-420">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="509d0-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-422">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="509d0-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-423">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="509d0-424">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="509d0-425">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-426">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="509d0-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-427">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="509d0-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-429">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="509d0-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-430">Dimensioni massime, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="509d0-431">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="509d0-432">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="509d0-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-434">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-436">Numero massimo di partizioni per l'unità nastro.</span><span class="sxs-lookup"><span data-stu-id="509d0-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="509d0-437">Questa proprietà viene ereditata da [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-438">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="509d0-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-441">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ TapeDrive \| mediaType \| Tape Drive")</span><span class="sxs-lookup"><span data-stu-id="509d0-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-442">Tipo di supporto usato dal dispositivo o a cui si accede da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="509d0-443">In questo caso, è impostato su "unità nastro".</span><span class="sxs-lookup"><span data-stu-id="509d0-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="509d0-444">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="509d0-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-445">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="509d0-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-447">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="509d0-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-448">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="509d0-449">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="509d0-450">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-451">**Nome**</span><span class="sxs-lookup"><span data-stu-id="509d0-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-452">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-454">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="509d0-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-455">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="509d0-455">Label by which the object is known.</span></span> <span data-ttu-id="509d0-456">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="509d0-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="509d0-457">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-458">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="509d0-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-459">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="509d0-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-461">Se **true**, il dispositivo di accesso multimediale deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="509d0-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="509d0-462">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="509d0-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="509d0-463">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-464">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="509d0-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-465">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-467">Numero massimo di supporti singoli che possono essere supportati o inseriti nel dispositivo di accesso multimediale (se supportato).</span><span class="sxs-lookup"><span data-stu-id="509d0-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="509d0-468">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-469">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="509d0-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-470">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-471">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-472">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="509d0-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-473">Numero di byte inseriti tra blocchi su un supporto a nastro.</span><span class="sxs-lookup"><span data-stu-id="509d0-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="509d0-474">Questa proprietà viene ereditata da [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="509d0-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-476">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-478">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="509d0-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-479">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="509d0-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="509d0-480">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="509d0-481">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="509d0-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="509d0-482">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="509d0-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-483">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="509d0-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="509d0-484">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-485">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="509d0-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="509d0-486">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="509d0-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="509d0-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="509d0-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="509d0-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="509d0-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-489">Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509d0-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="509d0-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="509d0-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="509d0-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="509d0-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-492">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="509d0-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="509d0-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="509d0-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-494">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="509d0-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="509d0-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="509d0-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-496">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="509d0-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="509d0-497">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="509d0-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="509d0-498">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="509d0-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="509d0-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-500">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="509d0-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="509d0-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="509d0-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="509d0-502">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="509d0-502">Timed Power-On Supported</span></span>

<span data-ttu-id="509d0-503">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="509d0-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-504">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="509d0-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-505">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="509d0-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-506">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="509d0-507">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="509d0-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="509d0-508">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="509d0-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="509d0-509">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-510">**ReportSetMarks**</span><span class="sxs-lookup"><span data-stu-id="509d0-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-511">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="509d0-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-512">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-513">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API nastri di backup su nastro \| \| [**nastro \_ get \_ unità \_ parametri**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ReportSetmarks")</span><span class="sxs-lookup"><span data-stu-id="509d0-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-514">Se il valore è **true**, la creazione di report è abilitata.</span><span class="sxs-lookup"><span data-stu-id="509d0-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="509d0-515">Per la creazione di report viene utilizzato un elemento registrato specializzato che non contiene dati utente.</span><span class="sxs-lookup"><span data-stu-id="509d0-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="509d0-516">Questo elemento registrato viene usato per fornire uno schema di segmentazione gerarchicamente superiore ai filemark.</span><span class="sxs-lookup"><span data-stu-id="509d0-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="509d0-517">I contrassegni consentono un posizionamento più veloce sui nastri ad alta capacità.</span><span class="sxs-lookup"><span data-stu-id="509d0-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="509d0-518"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="509d0-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="509d0-519">FALSE</span><span class="sxs-lookup"><span data-stu-id="509d0-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="509d0-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="509d0-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="509d0-521">true</span><span class="sxs-lookup"><span data-stu-id="509d0-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="509d0-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-523">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-524">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-525">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="509d0-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-526">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="509d0-526">Current status of the object.</span></span> <span data-ttu-id="509d0-527">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="509d0-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="509d0-528">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="509d0-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="509d0-529">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="509d0-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="509d0-530">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="509d0-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="509d0-531">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="509d0-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="509d0-532">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="509d0-533">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="509d0-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="509d0-534">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="509d0-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="509d0-535">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="509d0-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="509d0-536">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="509d0-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="509d0-537">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="509d0-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="509d0-538">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="509d0-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="509d0-539">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="509d0-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="509d0-540">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="509d0-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="509d0-541">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="509d0-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="509d0-542">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="509d0-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="509d0-543">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="509d0-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="509d0-544">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="509d0-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="509d0-545">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="509d0-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="509d0-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-547">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="509d0-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-548">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-549">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="509d0-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="509d0-550">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="509d0-550">State of the logical device.</span></span> <span data-ttu-id="509d0-551">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="509d0-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="509d0-552">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="509d0-553">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="509d0-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="509d0-554">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="509d0-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="509d0-555">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="509d0-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="509d0-556">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="509d0-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="509d0-557">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="509d0-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="509d0-558">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="509d0-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-559">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-560">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-561">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="509d0-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="509d0-562">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="509d0-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="509d0-563">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="509d0-564">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="509d0-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="509d0-565">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="509d0-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="509d0-566">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="509d0-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="509d0-567">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="509d0-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="509d0-568">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="509d0-568">Name of the scoping system.</span></span>

<span data-ttu-id="509d0-569">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="509d0-570">Commenti</span><span class="sxs-lookup"><span data-stu-id="509d0-570">Remarks</span></span>

<span data-ttu-id="509d0-571">La classe **Win32 \_ TapeDrive** è derivata da [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="509d0-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="509d0-572">Requisiti</span><span class="sxs-lookup"><span data-stu-id="509d0-572">Requirements</span></span>



| <span data-ttu-id="509d0-573">Requisito</span><span class="sxs-lookup"><span data-stu-id="509d0-573">Requirement</span></span> | <span data-ttu-id="509d0-574">Valore</span><span class="sxs-lookup"><span data-stu-id="509d0-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="509d0-575">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="509d0-575">Minimum supported client</span></span><br/> | <span data-ttu-id="509d0-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="509d0-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="509d0-577">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="509d0-577">Minimum supported server</span></span><br/> | <span data-ttu-id="509d0-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="509d0-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="509d0-579">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="509d0-579">Namespace</span></span><br/>                | <span data-ttu-id="509d0-580">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="509d0-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="509d0-581">MOF</span><span class="sxs-lookup"><span data-stu-id="509d0-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="509d0-582"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="509d0-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="509d0-583">DLL</span><span class="sxs-lookup"><span data-stu-id="509d0-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="509d0-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="509d0-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="509d0-585">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="509d0-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509d0-586">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="509d0-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="509d0-587">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="509d0-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

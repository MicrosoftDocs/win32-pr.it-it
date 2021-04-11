---
description: La \_ classe WMI Win32 FloppyDrive gestisce le funzioni di un'unità disco floppy.
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Classe Win32_FloppyDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127331"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="0c986-103">Win32 \_ FloppyDrive (classe)</span><span class="sxs-lookup"><span data-stu-id="0c986-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="0c986-104">\[**Win32 \_ FloppyDrive** non è più disponibile per l'uso a partire da Windows 10 e Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="0c986-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="0c986-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ FloppyDrive** gestisce le funzioni di un'unità disco floppy.</span><span class="sxs-lookup"><span data-stu-id="0c986-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="0c986-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0c986-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0c986-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0c986-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c986-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c986-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
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
  string   Manufacturer;
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

## <a name="members"></a><span data-ttu-id="0c986-109">Members</span><span class="sxs-lookup"><span data-stu-id="0c986-109">Members</span></span>

<span data-ttu-id="0c986-110">La classe **Win32 \_ FloppyDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0c986-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="0c986-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0c986-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c986-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c986-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c986-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="0c986-113">Methods</span></span>

<span data-ttu-id="0c986-114">La classe **Win32 \_ FloppyDrive** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0c986-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="0c986-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="0c986-115">Method</span></span>            | <span data-ttu-id="0c986-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c986-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c986-117">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="0c986-117">**Reset**</span></span>         | <span data-ttu-id="0c986-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0c986-118">Not implemented.</span></span> <span data-ttu-id="0c986-119">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) in [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="0c986-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0c986-120">**SetPowerState**</span></span> | <span data-ttu-id="0c986-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0c986-121">Not implemented.</span></span> <span data-ttu-id="0c986-122">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0c986-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c986-123">Properties</span></span>

<span data-ttu-id="0c986-124">La classe **Win32 \_ FloppyDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c986-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c986-125">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="0c986-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c986-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0c986-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-129">Stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-129">Status of the device.</span></span>

<span data-ttu-id="0c986-130">Questa proprietà viene ereditata da [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0c986-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c986-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c986-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c986-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0c986-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0c986-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0c986-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-134">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="0c986-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0c986-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0c986-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0c986-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="0c986-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0c986-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="0c986-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0c986-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="0c986-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0c986-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="0c986-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0c986-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="0c986-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0c986-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="0c986-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0c986-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="0c986-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0c986-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="0c986-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0c986-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="0c986-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-145">Risparmio energia-sconosciuto</span><span class="sxs-lookup"><span data-stu-id="0c986-145">Power Save - Unknown</span></span>

<span data-ttu-id="0c986-146">Il dispositivo in modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0c986-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0c986-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="0c986-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-148">Risparmio energia-modalità a basso consumo</span><span class="sxs-lookup"><span data-stu-id="0c986-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="0c986-149">Il dispositivo è in uno stato di risparmio energia, ma funziona ancora e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="0c986-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0c986-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="0c986-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-151">Risparmio energia-standby</span><span class="sxs-lookup"><span data-stu-id="0c986-151">Power Save - Standby</span></span>

<span data-ttu-id="0c986-152">Il dispositivo non funziona, ma può essere ripristinato rapidamente a potenza intera.</span><span class="sxs-lookup"><span data-stu-id="0c986-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0c986-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="0c986-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0c986-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0c986-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-155">Risparmio energia-avviso</span><span class="sxs-lookup"><span data-stu-id="0c986-155">Power Save - Warning</span></span>

<span data-ttu-id="0c986-156">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="0c986-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0c986-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0c986-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-158">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="0c986-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0c986-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0c986-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-160">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="0c986-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0c986-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="0c986-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-162">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="0c986-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0c986-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="0c986-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-164">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="0c986-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-165">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="0c986-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-166">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c986-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c986-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-168">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="0c986-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-169">Matrice di funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c986-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="0c986-170">Ad esempio, il dispositivo può supportare l'accesso casuale, i supporti rimovibili e la pulizia automatica.</span><span class="sxs-lookup"><span data-stu-id="0c986-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="0c986-171">In questo caso, i valori 3, 7 e 9 verranno scritti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="0c986-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="0c986-172">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c986-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0c986-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c986-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c986-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="0c986-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="0c986-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="0c986-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="0c986-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="0c986-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="0c986-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="0c986-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="0c986-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="0c986-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="0c986-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="0c986-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="0c986-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-181">Supporta supporti rimovibili</span><span class="sxs-lookup"><span data-stu-id="0c986-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="0c986-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="0c986-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="0c986-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="0c986-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="0c986-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="0c986-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="0c986-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="0c986-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-186">Supporta Dual-Sided supporti</span><span class="sxs-lookup"><span data-stu-id="0c986-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="0c986-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="0c986-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-188">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0c986-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-189">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c986-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c986-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-191">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="0c986-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-192">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità del controller seriale indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="0c986-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="0c986-193">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="0c986-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="0c986-194">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-195">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0c986-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-198">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0c986-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-199">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c986-199">Short description of the object.</span></span>

<span data-ttu-id="0c986-200">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-201">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="0c986-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-204">Stringa in formato libero che indica l'algoritmo o lo strumento usato dal dispositivo per supportare la compressione.</span><span class="sxs-lookup"><span data-stu-id="0c986-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="0c986-205">Se non è possibile o non si desidera descrivere lo schema di compressione (probabilmente perché non è noto), usare "Unknown" per indicare che non è noto se il dispositivo supporta o meno le funzionalità di compressione; "Compresso" per indicare che il dispositivo supporta le funzionalità di compressione, ma lo schema di compressione non è noto o non è stato divulgato; e "non compressi" per indicare che il dispositivo non supporta le funzionalità di compressione.</span><span class="sxs-lookup"><span data-stu-id="0c986-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="0c986-206">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="0c986-207">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0c986-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="0c986-208">Lo schema di compressione è sconosciuto o non è descritto.</span><span class="sxs-lookup"><span data-stu-id="0c986-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="0c986-209">("Compresso")</span><span class="sxs-lookup"><span data-stu-id="0c986-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="0c986-210">Il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto</span><span class="sxs-lookup"><span data-stu-id="0c986-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="0c986-211">("Non compresso")</span><span class="sxs-lookup"><span data-stu-id="0c986-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="0c986-212">Se il file logico non è compresso</span><span class="sxs-lookup"><span data-stu-id="0c986-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0c986-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-214">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c986-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-216">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0c986-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-217">Codice di errore di Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0c986-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="0c986-218">Questa proprietà viene ereditata da [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0c986-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0c986-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="0c986-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0c986-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="0c986-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-221">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c986-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0c986-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="0c986-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0c986-223">(1)</span><span class="sxs-lookup"><span data-stu-id="0c986-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-224">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c986-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0c986-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0c986-226">(2)</span><span class="sxs-lookup"><span data-stu-id="0c986-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0c986-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="0c986-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0c986-228">(3)</span><span class="sxs-lookup"><span data-stu-id="0c986-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-229">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="0c986-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0c986-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="0c986-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0c986-231">(4)</span><span class="sxs-lookup"><span data-stu-id="0c986-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-232">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c986-232">Device is not working properly.</span></span> <span data-ttu-id="0c986-233">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0c986-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0c986-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="0c986-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0c986-235">(5)</span><span class="sxs-lookup"><span data-stu-id="0c986-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-236">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="0c986-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0c986-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="0c986-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0c986-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="0c986-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-239">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0c986-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0c986-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="0c986-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0c986-241">(7)</span><span class="sxs-lookup"><span data-stu-id="0c986-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0c986-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="0c986-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0c986-243">(8)</span><span class="sxs-lookup"><span data-stu-id="0c986-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-244">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="0c986-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0c986-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="0c986-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0c986-246">(9)</span><span class="sxs-lookup"><span data-stu-id="0c986-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-247">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c986-247">Device is not working properly.</span></span> <span data-ttu-id="0c986-248">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0c986-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0c986-250">(10)</span><span class="sxs-lookup"><span data-stu-id="0c986-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-251">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0c986-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0c986-253">(11)</span><span class="sxs-lookup"><span data-stu-id="0c986-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-254">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0c986-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="0c986-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0c986-256">12</span><span class="sxs-lookup"><span data-stu-id="0c986-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-257">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="0c986-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0c986-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0c986-259">(13)</span><span class="sxs-lookup"><span data-stu-id="0c986-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-260">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0c986-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="0c986-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0c986-262">(14)</span><span class="sxs-lookup"><span data-stu-id="0c986-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-263">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="0c986-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0c986-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="0c986-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0c986-265">(15)</span><span class="sxs-lookup"><span data-stu-id="0c986-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-266">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="0c986-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0c986-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0c986-268">(16)</span><span class="sxs-lookup"><span data-stu-id="0c986-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-269">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0c986-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="0c986-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0c986-271">(17)</span><span class="sxs-lookup"><span data-stu-id="0c986-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-272">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0c986-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0c986-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0c986-274">(18)</span><span class="sxs-lookup"><span data-stu-id="0c986-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-275">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0c986-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="0c986-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0c986-277">(19)</span><span class="sxs-lookup"><span data-stu-id="0c986-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0c986-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="0c986-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0c986-279">(20)</span><span class="sxs-lookup"><span data-stu-id="0c986-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-280">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0c986-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0c986-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0c986-282">(21)</span><span class="sxs-lookup"><span data-stu-id="0c986-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-283">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0c986-283">System failure.</span></span> <span data-ttu-id="0c986-284">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0c986-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0c986-285">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0c986-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="0c986-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0c986-287">(22)</span><span class="sxs-lookup"><span data-stu-id="0c986-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-288">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0c986-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0c986-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="0c986-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0c986-290">(23)</span><span class="sxs-lookup"><span data-stu-id="0c986-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-291">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="0c986-291">System failure.</span></span> <span data-ttu-id="0c986-292">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="0c986-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0c986-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="0c986-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0c986-294">(24)</span><span class="sxs-lookup"><span data-stu-id="0c986-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-295">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="0c986-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0c986-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0c986-297">(25)</span><span class="sxs-lookup"><span data-stu-id="0c986-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-298">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0c986-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0c986-300">(26)</span><span class="sxs-lookup"><span data-stu-id="0c986-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-301">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0c986-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="0c986-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0c986-303">(27)</span><span class="sxs-lookup"><span data-stu-id="0c986-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-304">La configurazione del log del dispositivo non è valida.</span><span class="sxs-lookup"><span data-stu-id="0c986-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0c986-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="0c986-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0c986-306">(28)</span><span class="sxs-lookup"><span data-stu-id="0c986-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-307">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="0c986-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0c986-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="0c986-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0c986-309">(29)</span><span class="sxs-lookup"><span data-stu-id="0c986-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-310">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0c986-310">Device is disabled.</span></span> <span data-ttu-id="0c986-311">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="0c986-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0c986-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0c986-313">(30)</span><span class="sxs-lookup"><span data-stu-id="0c986-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-314">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0c986-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0c986-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0c986-316">31</span><span class="sxs-lookup"><span data-stu-id="0c986-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-317">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c986-317">Device is not working properly.</span></span> <span data-ttu-id="0c986-318">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="0c986-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0c986-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-320">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0c986-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-322">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0c986-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-323">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0c986-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0c986-324">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-325">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c986-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-328">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c986-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c986-329">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="0c986-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0c986-330">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="0c986-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0c986-331">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-332">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="0c986-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-333">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c986-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-335">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="0c986-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-336">Dimensioni del blocco predefinite, in byte, per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="0c986-337">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0c986-338">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0c986-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-339">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0c986-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-342">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0c986-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-343">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c986-343">Description of the object.</span></span>

<span data-ttu-id="0c986-344">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0c986-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-348">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c986-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c986-349">Identificatore univoco dell'unità disco floppy con altri dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0c986-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="0c986-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0c986-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-352">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0c986-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-354">Se **true**, l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="0c986-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0c986-355">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0c986-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-357">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-359">Stringa in formato libero che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="0c986-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="0c986-360">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-361">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="0c986-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-362">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-364">Stringa in formato libero che descrive il tipo di rilevamento e correzione degli errori supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="0c986-365">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0c986-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-367">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c986-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-369">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="0c986-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-370">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c986-370">Date and time the object was installed.</span></span> <span data-ttu-id="0c986-371">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="0c986-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0c986-372">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-373">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0c986-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-374">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c986-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-376">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0c986-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0c986-377">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-378">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="0c986-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-381">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="0c986-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-382">Nome del produttore dell'unità disco floppy.</span><span class="sxs-lookup"><span data-stu-id="0c986-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="0c986-383">Esempio: "Acme"</span><span class="sxs-lookup"><span data-stu-id="0c986-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="0c986-384">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="0c986-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-385">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c986-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-387">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="0c986-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-388">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="0c986-389">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0c986-390">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0c986-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-391">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="0c986-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-392">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c986-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-394">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di accesso sequenziale DMTF \| 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="0c986-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-395">Dimensioni massime, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="0c986-396">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0c986-397">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0c986-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-398">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="0c986-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-399">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c986-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-401">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte")</span><span class="sxs-lookup"><span data-stu-id="0c986-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-402">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c986-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="0c986-403">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0c986-404">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0c986-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-405">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0c986-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-408">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0c986-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-409">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="0c986-409">Label by which the object is known.</span></span> <span data-ttu-id="0c986-410">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="0c986-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0c986-411">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-412">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="0c986-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-413">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0c986-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-415">Se **true**, il dispositivo di accesso ai supporti richiede la pulizia.</span><span class="sxs-lookup"><span data-stu-id="0c986-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="0c986-416">Se la pulizia manuale o automatica è possibile, è indicata nella proprietà **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="0c986-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="0c986-417">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-418">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="0c986-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-419">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c986-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-421">Numero massimo di supporti singoli che possono essere supportati o inseriti nel dispositivo di accesso multimediale (se supportato).</span><span class="sxs-lookup"><span data-stu-id="0c986-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="0c986-422">Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0c986-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-426">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0c986-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-427">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0c986-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0c986-428">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0c986-429">Esempio: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0c986-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0c986-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0c986-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-431">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c986-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c986-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-433">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0c986-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0c986-434">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="0c986-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c986-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0c986-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0c986-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="0c986-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0c986-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="0c986-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0c986-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0c986-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-439">Abilitato</span><span class="sxs-lookup"><span data-stu-id="0c986-439">Enabled</span></span>

<span data-ttu-id="0c986-440">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="0c986-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0c986-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0c986-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-442">Modalità di risparmio energia immesse automaticamente</span><span class="sxs-lookup"><span data-stu-id="0c986-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="0c986-443">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="0c986-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0c986-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="0c986-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-445">Stato di alimentazione impostabile</span><span class="sxs-lookup"><span data-stu-id="0c986-445">Power State Settable</span></span>

<span data-ttu-id="0c986-446">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="0c986-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0c986-447">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="0c986-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0c986-448">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0c986-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0c986-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="0c986-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-450">Power Cycling supportato</span><span class="sxs-lookup"><span data-stu-id="0c986-450">Power Cycling Supported</span></span>

<span data-ttu-id="0c986-451">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="0c986-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0c986-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="0c986-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0c986-453">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="0c986-453">Timed Power-On Supported</span></span>

<span data-ttu-id="0c986-454">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="0c986-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-455">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0c986-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-456">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0c986-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c986-458">Se **true**, il dispositivo può essere gestito dal risparmio di energia (può essere impostato in modalità di sospensione e così via).</span><span class="sxs-lookup"><span data-stu-id="0c986-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="0c986-459">La proprietà non indica che le funzionalità di risparmio energia sono attualmente abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="0c986-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="0c986-460">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c986-461">**Status**</span><span class="sxs-lookup"><span data-stu-id="0c986-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-462">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-463">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-464">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0c986-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-465">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c986-465">Current status of the object.</span></span> <span data-ttu-id="0c986-466">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="0c986-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0c986-467">Gli stati operativi includono: "OK", "danneggiato" e "errore predazione" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, può funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="0c986-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="0c986-468">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="0c986-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0c986-469">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="0c986-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0c986-470">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="0c986-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0c986-471">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0c986-472">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="0c986-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0c986-473">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0c986-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0c986-474">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="0c986-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0c986-475">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="0c986-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c986-476">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0c986-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0c986-477">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="0c986-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0c986-478">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="0c986-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0c986-479">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="0c986-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0c986-480">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="0c986-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0c986-481">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="0c986-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0c986-482">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="0c986-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0c986-483">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="0c986-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0c986-484">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="0c986-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0c986-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-486">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c986-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-488">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0c986-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0c986-489">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0c986-489">State of the logical device.</span></span> <span data-ttu-id="0c986-490">Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="0c986-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="0c986-491">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0c986-492">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c986-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0c986-493">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0c986-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0c986-494">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0c986-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0c986-495">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="0c986-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0c986-496">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="0c986-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c986-497">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c986-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-498">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-499">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-500">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c986-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c986-501">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="0c986-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="0c986-502">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0c986-503">Questa proprietà viene ereditata da [ **CIM \_ LogicalDevice**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0c986-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="0c986-504">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0c986-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c986-505">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c986-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c986-506">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c986-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c986-507">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0c986-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0c986-508">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="0c986-508">Name of the scoping system.</span></span>

<span data-ttu-id="0c986-509">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c986-510">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c986-510">Remarks</span></span>

<span data-ttu-id="0c986-511">La classe **Win32 \_ FloppyDrive** è derivata da [**CIM \_ DisketteDrive**](cim-diskettedrive.md) che deriva da [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="0c986-512">La classe **CIM \_ MediaAccessDevice** deriva da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0c986-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c986-513">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c986-513">Requirements</span></span>



| <span data-ttu-id="0c986-514">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c986-514">Requirement</span></span> | <span data-ttu-id="0c986-515">Valore</span><span class="sxs-lookup"><span data-stu-id="0c986-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c986-516">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c986-516">Minimum supported client</span></span><br/> | <span data-ttu-id="0c986-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c986-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c986-518">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c986-518">Minimum supported server</span></span><br/> | <span data-ttu-id="0c986-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c986-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c986-520">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0c986-520">End of client support</span></span><br/>    | <span data-ttu-id="0c986-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0c986-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="0c986-522">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0c986-522">End of server support</span></span><br/>    | <span data-ttu-id="0c986-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0c986-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="0c986-524">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c986-524">Namespace</span></span><br/>                | <span data-ttu-id="0c986-525">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0c986-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c986-526">MOF</span><span class="sxs-lookup"><span data-stu-id="0c986-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c986-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c986-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c986-528">DLL</span><span class="sxs-lookup"><span data-stu-id="0c986-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c986-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c986-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c986-530">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c986-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c986-531">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="0c986-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="0c986-532">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="0c986-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

